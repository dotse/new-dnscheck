## DNSSEC02: DS must match a DNSKEY in the designated zone

### Test case identifier
**DNSSEC02** DS must match a DNSKEY in the designated zone

### Objective

DNS delegations from a parent to a child are secured with DNSSEC by
publishing one or several Delgation Signer (DS) records in the parent
zone, along with the NS records for the delegation. For the secure
delegation to work, the DS record must match at least one DNSKEY record
in the child zone.

The method for authentication a DNS response is described in section 5 of
[RFC 4035](https://tools.ietf.org/html/rfc4035#section-5). The DS record
is described in section 5 of [RFC 4034]
(https://tools.ietf.org/html/rfc4034#section-5) and the DNSKEY record is
described in section 2 of [RFC 4034]
(https://tools.ietf.org/html/rfc4034#section-2).

The IANA registry of DNSKEY algorithm numbers is in the [dns-sec-alg-numbers]
(https://www.iana.org/assignments/dns-sec-alg-numbers/dns-sec-alg-numbers.xml).
The allowed Digest Algorithms in a DS record published by the parent are
published by IANA in [Delegation Signer (DS) Resource Record (RR) Type
Digest Algorithms](https://www.iana.org/assignments/ds-rr-types/ds-rr-types.xml). 

The Key Tag is only an indicator for a resolver or application to enable
a quicker matching of the keys. This is however not a reliable method for
identifiying keys. A description of this is found in section 5.2 of
[RFC 4035](https://tools.ietf.org/html/rfc4035#section-5.2).

Section 3 of [RFC 4509](https://tools.ietf.org/html/rfc4509#section-3) states
that Validator implementations SHOULD ignore DS RRs containing SHA-1 digests
if DS RRs with SHA-256 digests are present in the DS RRset. The algorithms
are tested separately.

### Inputs

The domain name to be tested.

### Ordered description of steps to be taken to execute the test case

1. Retrieve the DS RR set from the parent zone. If there are no DS RR
   present, exit the test
2. Retrieve the DNSKEY RR set from the child zone. If there are no
   DNSKEY RR present, then the test case fails
3. If no Key Tag from the DS RR matches any Key Tag from the DNSKEY RR,
   this test case fails.
4. Match all DS RR with type digest algorithm “2” with DNSKEY RR from the
   child. If no DS RRs with algorithm 2 matches a DNSKEY RR from the child,
   this test case fails.
5. Match all DS RR with type digest algorithm “1” with DNSKEY RR from the
   child. If no DS RRs with algorithm 1 matches a DNSKEY RR from the child,
   this test case fails.

### Outcome(s)

If none of the DS RR from the parent zone matches any DNSKEY RR from the
child zone, this test case fails.

### Special procedural requirements

See the [level document](level.md) about DNSSEC algorithms.

Test case is only performed if DS records are found.

### Intercase dependencies

None.

-------

Copyright (c) 2013, 2014, 2015, IIS (The Internet Infrastructure Foundation)  
Copyright (c) 2013, 2014, 2015, AFNIC  
Creative Commons Attribution 4.0 International License

You should have received a copy of the license along with this
work.  If not, see <https://creativecommons.org/licenses/by/4.0/>.

## Report on Requirements to Test Case mapping

|Req|Requirement desription|Level     |Test Case ID|Test Description|
|:--|:---------------------|:---------|:-----------|:---------------|
|R01|       UDP connectivity|[Connectivity-TP](Connectivity-TP/README.md)|[CONNECTIVITY01](.//Connectivity-TP/connectivity01.md)| UDP connectivity|
|R02|       TCP connectivity|[Connectivity-TP](Connectivity-TP/README.md)|[CONNECTIVITY02](.//Connectivity-TP/connectivity02.md)| TCP connectivity|
|R03|Address in a private network|[Address-TP](Address-TP/README.md)|[ADDRESS01](.//Address-TP/address01.md)|Name server address must be globally routable|
|R04|Address should not be part of a bogon prefix|[Address-TP](Address-TP/README.md)|[ADDRESS01](.//Address-TP/address01.md)|Name server address must be globally routable|
|R05|Illegal symbols in domain name|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX01](.//Syntax-TP/syntax01.md)|No illegal characters in the domain name|
|R06|Dash ('-') at start or beginning of domain name|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX02](.//Syntax-TP/syntax02.md)|No hyphen ('-') at the start or end of the domain name|
|R07|Double dash in domain name|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX03](.//Syntax-TP/syntax03.md)|There must be no double hyphen ('--') in position 3 and 4 of the domain name|
|R08|The child domain has atleast one working name server|[  Basic-TP](Basic-TP/README.md)|[BASIC02](.//Basic-TP/basic02.md)|The domain must have at least one working name server|
|R09|At least two nameservers for the domain|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION01](.//Delegation-TP/delegation01.md)|Minimum number of name servers   |
|R10|    Identical addresses|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION02](.//Delegation-TP/delegation02.md)|Name servers must have distinct IP addresses|
|R11|Nameserver addresses on same subnet|[Connectivity-TP](Connectivity-TP/README.md)|[CONNECTIVITY03](.//Connectivity-TP/connectivity03.md)|     AS Diversity|
|R12|Nameserver addresses are all on the same subnet|[Connectivity-TP](Connectivity-TP/README.md)|[CONNECTIVITY03](.//Connectivity-TP/connectivity03.md)|     AS Diversity|
|R13|Delegation response fit in a 512 byte UDP packet|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION03](.//Delegation-TP/delegation03.md)|No truncation of referrals|
|R14|Delegation response with additional fit in a 512 byte UDP packet|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION03](.//Delegation-TP/delegation03.md)|No truncation of referrals|
|R15|      NS record present|[  Basic-TP](Basic-TP/README.md)|[BASIC02](.//Basic-TP/basic02.md)|The domain must have at least one working name server|
|R16|NS authoritative answer|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION04](.//Delegation-TP/delegation04.md)|Name server is authoritative|
|R17|NS name has a valid domain/hostname syntax|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX04](.//Syntax-TP/syntax04.md)|The NS name must have a valid domain/hostname|
|R18|     NS is not an alias|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION05](.//Delegation-TP/delegation05.md)|NS RR does not point to CNAME alias|
|R19|     NS can be resolved|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER06](.//Nameserver-TP/nameserver06.md)|NS can be resolved|
|R20|     SOA record present|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION06](.//Delegation-TP/delegation06.md)| Existence of SOA|
|R21|SOA authoritative answer|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION06](.//Delegation-TP/delegation06.md)| Existence of SOA|
|R22|Missused '@' characters in SOA contact name|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX05](.//Syntax-TP/syntax05.md)|Misuse of '@' character in the SOA RNAME field|
|R23|Illegal characters in SOA contact name|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX06](.//Syntax-TP/syntax06.md)|No illegal characters in the SOA RNAME field|
|R24|Illegal characters in SOA master nameserver|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX07](.//Syntax-TP/syntax07.md)|No illegal characters in the SOA MNAME field|
|R25|Fully qualified master nameserver in SOA|[   Zone-TP](Zone-TP/README.md)|[ZONE01](.//Zone-TP/zone01.md)|Fully qualified master nameserver in SOA|
|R26|SOA 'refresh' at least 6 hours|[   Zone-TP](Zone-TP/README.md)|[ZONE02](.//Zone-TP/zone02.md)|SOA 'refresh' minimum value|
|R27|SOA 'retry' lower than 'refresh'|[   Zone-TP](Zone-TP/README.md)|[ZONE03](.//Zone-TP/zone03.md)|SOA 'retry' lower than 'refresh'|
|R28|SOA 'retry' at least 1 hour|[   Zone-TP](Zone-TP/README.md)|[ZONE04](.//Zone-TP/zone04.md)|SOA 'retry' at least 1 hour|
|R29|SOA 'expire' at least 7 days|[   Zone-TP](Zone-TP/README.md)|[ZONE05](.//Zone-TP/zone05.md)|SOA 'expire' minimum value|
|R31|SOA 'minimum' less than 1 day|[   Zone-TP](Zone-TP/README.md)|[ZONE06](.//Zone-TP/zone06.md)|SOA 'minimum' maximum value|
|R32|SOA master is not an alias|[   Zone-TP](Zone-TP/README.md)|[ZONE07](.//Zone-TP/zone07.md)|SOA master is not an alias|
|R33|Coherence of serial number with primary nameserver|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY01](.//Consistency-TP/consistency01.md)|SOA serial number consistency|
|R34|Coherence of administrative contact with primary nameserver|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY02](.//Consistency-TP/consistency02.md)|RNAME consistency|
|R36|Coherence of SOA with primary nameserver|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY03](.//Consistency-TP/consistency03.md)|SOA parameters consistency|
|R40|  Nameserver IP reverse|[Address-TP](Address-TP/README.md)|[ADDRESS02](.//Address-TP/address02.md)|Reverse DNS entry exists for name server IP address|
|R41|Nameserver IP reverse matching nameserver name|[Address-TP](Address-TP/README.md)|[ADDRESS03](.//Address-TP/address03.md)|Reverse DNS entry matches name server name|
|R42|Check if server is really recursive|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER01](.//Nameserver-TP/nameserver01.md)|A name server should not be a recursor|
|R43|Nameserver doesn't allow recursion|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER01](.//Nameserver-TP/nameserver01.md)|A name server should not be a recursor|
|R46|Test if server is recursive|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER01](.//Nameserver-TP/nameserver01.md)|A name server should not be a recursor|
|R47|      MX record present|[   Zone-TP](Zone-TP/README.md)|[ZONE09](.//Zone-TP/zone09.md)|MX record present|
|R49|MX syntax is valid for an hostname|[ Syntax-TP](Syntax-TP/README.md)|[SYNTAX08](.//Syntax-TP/syntax08.md)|MX name must have a valid hostname|
|R50|     MX is not an alias|[   Zone-TP](Zone-TP/README.md)|[ZONE08](.//Zone-TP/zone08.md)|MX is not an alias|
|R52|     MX can be resolved|[   Zone-TP](Zone-TP/README.md)|[ZONE09](.//Zone-TP/zone09.md)|MX record present|
|R53|Behaviour against AAAA query (RFC 4074)|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER05](.//Nameserver-TP/nameserver05.md)|Behaviour against AAAA query|
|R54|Nameservers belong all to the same AS|[Connectivity-TP](Connectivity-TP/README.md)|[CONNECTIVITY03](.//Connectivity-TP/connectivity03.md)|     AS Diversity|
|R58|Legal values for the DS hash digest algorithm|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC01](.//DNSSEC-TP/dnssec01.md)|Legal values for the DS hash digest algorithm|
|R59|DS must match a DNSKEY in the designated zone|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC02](.//DNSSEC-TP/dnssec02.md)|DS must match a DNSKEY in the designated zone|
|R60|Check for too many NSEC3 iterations|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC03](.//DNSSEC-TP/dnssec03.md)|Check for too many NSEC3 iterations|
|R61|Check for too short or too long RRSIG lifetimes|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC04](.//DNSSEC-TP/dnssec04.md)|Check for too short or too long RRSIG lifetimes|
|R62|Check for invalid DNSKEY algorithms|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC05](.//DNSSEC-TP/dnssec05.md)|Check for invalid DNSKEY algorithms|
|R63|Verify DNSSEC additional processing|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC06](.//DNSSEC-TP/dnssec06.md)|Verify DNSSEC additional processing|
|R64|If there exists DNSKEY at child, the parent should have a DS|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC07](.//DNSSEC-TP/dnssec07.md)|If DNSKEY at child, parent should have DS|
|R65|RRSIG(DNSKEY) must be valid and created by a valid DNSKEY|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC08](.//DNSSEC-TP/dnssec08.md)|RRSIG(DNSKEY) must be valid and created by a valid DNSKEY|
|R66|RRSIG(SOA) must be valid and created by a valid DNSKEY|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC09](.//DNSSEC-TP/dnssec09.md)|RRSIG(SOA) must be valid and created by a valid DNSKEY|
|R67|There must be NS records for the zone being tested on the parent side|[  Basic-TP](Basic-TP/README.md)|[BASIC01](.//Basic-TP/basic01.md)|The domain must have a parent domain|
|R68|The child domain must have at least one working nameserver|[  Basic-TP](Basic-TP/README.md)|[BASIC02](.//Basic-TP/basic02.md)|The domain must have at least one working name server|
|R69|NS records from parent exists, but the child does not have NS but answers for A|[  Basic-TP](Basic-TP/README.md)|[BASIC03](.//Basic-TP/basic03.md)|The _Broken but functional_ test|
|R70|Coherence of all other SOA-fields where SOA Serial is the same|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY03](.//Consistency-TP/consistency03.md)|SOA parameters consistency|
|R71|Total mismatch between child and parent NS records, delegation works due to same IP|[Delegation-TP](Delegation-TP/README.md)|[DELEGATION07](.//Delegation-TP/delegation07.md)|Parent glue name records present in child|
|R72|  Test of EDNS0 support|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER02](.//Nameserver-TP/nameserver02.md)|Test of EDNS0 support|
|R73|Test availability of zone transfer (AXFR)|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER03](.//Nameserver-TP/nameserver03.md)|Test availability of zone transfer (AXFR)|
|R74|Answer from name server came from an IP address other than expected (wrong source IP)|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER04](.//Nameserver-TP/nameserver04.md)|Same source address|
|R76|Zone contains NSEC or NSEC3 records|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC10](.//DNSSEC-TP/dnssec10.md)|Zone contains NSEC or NSEC3 records|
|R77|Perform input validation on the domain name|[  Basic-TP](Basic-TP/README.md)|[BASIC00](.//Basic-TP/basic00.md)|Domain name must be valid|
|R78|All authoritative nameservers reply with same set|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY04](.//Consistency-TP/consistency04.md)|Name server NS consistency|
|R79|If DS at parent, child zone must be signed|[ DNSSEC-TP](DNSSEC-TP/README.md)|[DNSSEC11](.//DNSSEC-TP/dnssec11.md)|Delegation from parent to child is properly signed|
|R80|Test QNAME case sensitivity|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER09](.//Nameserver-TP/nameserver09.md)|Testing QNAME case sensitivity|
|R81|   Test Upward referral|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER07](.//Nameserver-TP/nameserver07.md)|To check whether authoritative name servers return an upward referral|
|R82|Test QNAME Case insensitivity|[Nameserver-TP](Nameserver-TP/README.md)|[NAMESERVER08](.//Nameserver-TP/nameserver08.md)|Testing QNAME case insensitivity  |
|R83|Consistency between glue and authoritative data|[Consistency-TP](Consistency-TP/README.md)|[CONSISTENCY05](.//Consistency-TP/consistency05.md)|Consistency between glue and authoritative data|
|R84|Test for DNSSEC Algorithm Completeness (DS->DNSKEY->RRSIG)|[ DNSSEC-TP](DNSSEC-TP/README.md)|[missing](.//DNSSEC-TP/dnssec12.md)|          missing|

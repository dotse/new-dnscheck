## SYNTAX04: The NS name must have a valid domain/hostname

### Test case identifier
**SYNTAX04** The NS name must have a valid domain/hostname

### Objective

The Name Server name must be a valid hostname according to the rules defined
in [RFC 952](https://tools.ietf.org/html/rfc952),
in section 2.1 in [RFC 1123](https://tools.ietf.org/html/rfc1123#section-2.1),
section 11 in [RFC 2182](https://tools.ietf.org/html/rfc2181#section-11) and
section 2 and 5 in [RFC 3696](https://tools.ietf.org/html/rfc3696#section-2).
Newer RFCs may override some rules defined in earlier documents.

### Inputs

The hostname to be tested. The hostnames comes from all the nameservers
used, from both the parent and the zone itself.

### Ordered description of steps to be taken to execute the test case

1. Obtain the list of name server hostnames from [Method2](../Methods.md) and
   [Method3](../Methods.md)
   (This is all the name servers from the parent delegation, and all the
   name servers in the apex of the zone itself.)
2. Each label of the hostname of the test object is used as the input
   for the validation.
3. If any label in the hostname does not contain a-z or 0-9 this test case
   fails.
4. If the rightmost label (the TLD) contains only digits, this test case
   fails.
5. If there is a hyphen ('-') in position 3 and 4 of the label, and the prefix
   is not xn (used for internationalization), this test case fails.

### Outcome(s)

If any of the steps 3 to 5 in the ordered description of this test case fails,
the whole test case fails.

### Special procedural requirements

None.

### Intercase dependencies

None.

-------

Copyright (c) 2013, 2014, 2015, IIS (The Internet Infrastructure Foundation)  
Copyright (c) 2013, 2014, 2015, AFNIC  
Creative Commons Attribution 4.0 International License

You should have received a copy of the license along with this
work.  If not, see <https://creativecommons.org/licenses/by/4.0/>.

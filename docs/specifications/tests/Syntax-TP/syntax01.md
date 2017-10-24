## SYNTAX01: No illegal characters in the domain name

### Test case identifier
**SYNTAX01** No illegal characters in the domain name

### Objective

There must be no illegal characters used in the domain name.
The domain name must follow the rules defined in section 2.3.1 of
[RFC 1035](https://tools.ietf.org/rfc/rfc1035.txt),
section 2.1 of [RFC 1123](https://tools.ietf.org/html/rfc1123#section-2.1),
section 11 of
[RFC 2182](https://tools.ietf.org/html/rfc2181#section-11) and section 2 of
[RFC 3696](https://tools.ietf.org/html/rfc3696#section-2).

### Inputs

The domain name to be tested.

### Ordered description of steps to be taken to execute the test case

1. The domain name of the test object is used as the input for the
   validation.
2. Check for characters that are not allowed in the domain name according
   to the rules defined in section 2.3.1 of
   [RFC 1035](https://tools.ietf.org/rfc/rfc1035.txt).

### Outcome(s)

If there are any invalid characters in the domain name, this test case fails.

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

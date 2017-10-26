## NAMESERVER08: Testing QNAME case insensitivity  

### Test case identifier
NAMESERVER08 Verify whether the authoritative nameserver response match the 
case of every letter in the query name


### Objective
The DNS standards require that nameservers treat names with case insensitivity.
That is, the names example.com and EXAMPLE.COM should resolve to the same IP
address. However, in the response, most nameservers echo back the name as it
appeared in the request, preserving the original case.

Therefore, another way to add entropy to requests is to randomly vary the case
of letters in domain names queried. This technique, also known as "0x20" because
bit 0x20 is used to set the case of of US-ASCII letters, was first proposed in
the [IETF internet draft](https://tools.ietf.org/html/draft-vixie-dnsext-dns0x20-00) Use of Bit 0x20 in DNS Labels to Improve Transaction
Identity. With this technique, the nameserver response must match not only the
query name, but the case of every letter in the name string; for example,
wWw.eXaMpLe.CoM or WwW.ExamPLe.COm. This may add little or no entropy to queries
for the top-level and root domains, but it's effective for most hostnames.

### Inputs
The domain name to be tested.

### Ordered description of steps to be taken to execute the test case
1. Retrieve all address records for all the name servers using [Method 
   4](../Methods.md) and [Method 5](../Methods.md).
2. A random query with mixed case (e.G Www.iETf.Org) is sent to each unique name
   server IP address found in step 1.
3. Remember the case of the QNAME in the query sent.
4. Compare the QNAME in the question section of the response with the string in    step3. 
5. If the string in step3 and step4 are not equal with respect to case in
   sensitivity, the test fails.


### Outcome(s)
The test case is Ok only if there are no responses in the authority section 

### Special procedural requirements
None.

### Intercase dependencies
None.

-------

Copyright (c) 2013, 2014, 2015, IIS (The Internet Infrastructure
Foundation) Copyright (c) 2013, 2014, 2015, AFNIC Creative Commons Attribution
4.0 International License

You should have received a copy of the license along with this work. If not,
see <https://creativecommons.org/licenses/by/4.0/>.

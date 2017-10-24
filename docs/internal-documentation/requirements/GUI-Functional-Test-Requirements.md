GUI - Functional Test requirements
======================================

Objective
----------
The objective of this document is to run functional tests for the Web GUI.

Scope
------
The scope of the testing will limited to the follows:
   * GUI testing : Test if the objects in the interface are displayed exactly
   how they are supposed to display
   * Functionality testing : Validation of actual functionality of controls
   after giving input to certain fields in the application
 
Security and Performance testing are not included.

|Req| Test requirement                           |How Verified|Status|
|:--|:-------------------------------------------|------------|------|
|GR01|Supports Swedish language|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR01-test-swedish-language.js)| KO - noJS |
|GR02|Supports French language|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR02-test-french-language.js)| KO - noJS|
|GR03|Supports English language |[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR03-english-language-support.js)| Ok |
|GR04|On launching the URL opens with a default simple view | [Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR04-main-page.js)| OK |
|GR05|The simple view should look the same in latest version of different browsers such as Firefox, Internet Explorer, Chrome, Safari etc.   | ToDo |
|GR06|The simple view should support an advanced view expanding when the checkbox is enabled|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR06-basic-view-advanced-options.js)|K0 - No advance option in the "nojs" |
|GR07|The advanced view should support the possibility of enabling or disabling IPv4 or IPv6 |[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR07-advanced-checkbox-verification.js)|OK|
|GR08|The advanced view should support the possibility of choosing a profile from multiple profiles|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR08-advanced-profile-verification.js)|OK|            
|GR09|The advanced view should look the same in latest version of different browsers such as Firefox, Internet Explorer, Chrome, Safari etc.   |   ToDo         |
|GR11|The undelegated view must inherit all of the advanced view options |Manually|OK|
|GR12|The undelegated view should look the same in latest version of different browsers such as Firefox, Internet Explorer, Chrome, Safari etc.   | ToDo    |
|GR13|The undelegated view should have a text describing what undelegated means? |Manually|KO|
|GR14|The undelegated view should have a shortcut to simple view and FAQ|Manually|KO - noJS|
|GR15|A Home button that sends the user to the default simple view |Manually|KO - noJS|
|GR16|All menus should be clickable in latest version of different browsers such as Firefox, IE, Chrome, Safari etc. |  ToDo  |
|GR17|All buttons should be clickable in latest version of different browsers such as Firefox, IE, Chrome, Safari etc. |  ToDo      |
|GR18|All appropriate fields (both simple and undelegated) should be writable |Manually|OK|
|GR19|Capable to enable and disable checkboxes in advanced option|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR19-advanced-checkbox-verification.js)|OK|
|GR20|Capable to select one of the drop down menu in the advanced option|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR19-advanced-checkbox-verification.js)|OK|
|GR21|Check the existence of broken links|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR21-check-broken-links.js)|OK|
|GR22|Check the display of appropriate content on clicking each link |[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR22-link-content.js)|OK|
|GR23|Check the tool displays the client IP address  |Manually|OK|
|GR24|Able to specify delegation parameters  |Manually|OK|
|GR25|Able to specify to stop the test on a fatal error | For release 1.1 |Wishlist|
|GR26|Check all the terms (such as menus, input fields) are appropriate   | Manually |OK|
|GR27|Afnic and IIS logo in the main page|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR27-logo-verification.js)|KO|   
|GR28|Check the existence of correct title for the web site|[Script](https://github.com/dotse/zonemaster-gui/blob/master/FunctionalTests/GR27-logo-verification.js)|OK|
|FR01|Identifies the preference of connected user's language |Manually|OK|
|FR02|Presence of a default fallback language |Manually|OK|
|FR03|Support IDN2.0 domains as input |Manually|OK|
|FR04|Once a language is chosen, all other links should open in that respective language |Manually|KO|
|FR05|On running a test from the simple view, the errors and warning should be highlighted in the same page |Manually|OK|
|FR06|Able to provide a summarized result of the test being run (possibility in different colours for error, warning, success etc.) |Manually|OK|
|FR07|Provide the possibility to see more information about encountered errors within the simple view |Manually|OK|
|FR08|Provide a list of previous runs for the domain and should be paginated |Manually|KO|
|FR09|The list of previous runs should contain links to the previous tests | Manually |OK|
|FR10|The list of previous runs should clearly differentiate that the source of test has been normal, or undelegated |Manually|KO|
|FR11|For delegated zones, the GUI should be able to run tests by just providing the domain name |Manually|OK|
|FR12|For undelegated zones, the GUI should be able to run the test with atleast one name server as input |Manually|OK|
|FR13|For undelegated zones, the user must be able to submit one or more DS record(s) for use with DNSSEC | Manually |OK |
|FR14|Verify the GUI runs with different test profiles|Manually| KO - No test profiles created (Issue https://github.com/dotse/zonemaster/issues/167)|
|FR15|Should be able to export the result in HTML format|Manually|KO|
|FR16|Should be able to export the result in TEXT format|Manually|OK|
|FR17|Should be able to show a progress bar with a rough estimate of the total test progress|Manually|OK|
|FR18|Should be able to tell the user what specific test it is currently running near to the progress bar|Manually|KO|
|FR19|Check whether the input field in the simple view is actually a valid delegated domain name |Manually|OK|
|FR20|Check for illegal characters as in SQL injections and illegal double dashes etc.  |Tested by Security Audit|OK|
|FR21|Check label length not greater than 64  |Manually|OK|
|FR22|Check domain length not greater than 256  |Manually|OK|
|FR23|Check whether a default "test profile"  is mandatorily selected in the advanced view |Manually|KO|
|FR24|Compare the results of a well configured domain name with ZC and DC |Inconsistent for iis.se|KO|  
|FR25|Compare the results of different broken  domain names with ZC and DC |Manually with some broken domains|OK|
|FR26|In the undelegated domain check whether IP fields autocomplete when the associated NS field is added |Manually|OK|


#Responsible party contact info

**Purpose**: Name and contact email to a responsible party must be given for every responsible organization in the metadata.

**Prerequisites**

**Test method**

The test first checks if there is at least one element at gmd:identificationInfo/\*/gmd:pointOfContact. Furthermore, the following checks are performed
*	There must not be an [empty characterstring](./README#emptychar) at ./gmd:organisationName
*	There must not be an [empty characterstring](./README#emptychar) at ./gmd:contactInfo/\*/gmd:address/\*/gmd:electronicMailAddress. Check [electronicMailAddress](#electronicMailAddress) with the regular expresion ^[A-Z0-9._%+-]+@[A-Z0-9.-]+.[A-Z]{2,}$.
If the string does not match the regular expression, the test fails (note: regex built for case insensitive match).

**Reference(s)**	 

* [TG MD](./README#ref_TG_MD) 2.10.1, Req 35 & 36

**Test type**: Automated

**Notes**

In the ETS, an updated regex '^[a-zA-Z0-9\._%\+-]+@[a-zA-Z0-9\.-]+\.[a-zA-Z]{2,}$' has been used (regex are case sensitive and special characters like "." and "+" have to be escaped).

##Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="CI_ResponsibleParty"></a> CI_ResponsibleParty   | ./gmd:identificationInfo/\*/gmd:pointOfContact/\*/gmd:CI_ResponsibleParty
<a name="organisationName"></a> Organisation Name |./gmd:organisationName
<a name="electronicMailAddress"></a> Electronic Mail Address  |./gmd:contactInfo//gmd:address//gmd:electronicMailAddress

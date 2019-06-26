# Service linkage

**Purpose**: If a linkage for a service is available, the Resource Locator shall be a
valid URL providing one of the following:
* a link to a web with further instructions
* a link to a service capabilities document
* a link to the service WSDL document (SOAP Binding)
* a link to a client application that directly accesses the service

**Prerequisites**

* [Hierarchy](./hierarchy) 

**Test method**

This test case only applies to records with a [hierarchyLevel](#hierarchyLevel) value 'service'.

The test first checks if a linkage is provided. If none is given, the test will complete successfully.

If one or more are provided: For each linkage the test checks, if the linkage element contains an element of type gmd:URL. Retrieve the resource at the URL using HTTP GET.

The metadata validator should accept 'text/xml', 'application/xml', 'application/vnd.ogc.*' and 'application/atom' as a media type for distribution.

If the response indicates a linkage is a service capabilities or WSDL document consistent with an INSPIRE technical guidance, some basic parameters in the service response are analysed as described in the next paragraph. Else a final manual test is suggested to the tester (to test if any of the linkages points to a webpage with further instructions or a client application that directly accesses the service).

Any service response should be checked if it provides proper linkage. The service wsdl or capabilities document should have a featuretype that shares the resource unique identification. If WMS/WMTS/WFS, the link is in //layer[identifier={id}&&@authority={codespace}] if Atom, the link is in //feed[@uuidhref={id}&&@namespace={codespace}].

**Reference(s)**	 

* [TG MD](./README.md#ref_TG_MD), 2.2.4, Req 4

**Test type**: Automated/Manual

**Notes**

The ETS does not take WSDL files into account, since there can be no WSDL document consistent with an INSPIRE technical guidance.

The specification of how to perform the detailed test is insufficient. The following aspect has not been fully implemented yet in the ETS (it is not yet part of the ETS): "The service wsdl or capabilities document should have a featuretype that shares the resource unique identification. If WMS/WMTS/WFS, the link is in //layer[identifier={id}&&@authority={codespace}] if Atom, the link is in //feed[@uuidhref={id}&&@namespace={codespace}]."

The depencency to [Hierarchy](./hierarchy) has not been implemented in the ETS as it still seems reasonable to test the available service metadata records.  

Since WCS and SOS are now also supported by technical guidance documents, the ETS also accepts these service types.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                   |  XPath expression (relative to gmd:MD_Metadata)
-----------------------------------------------| -------------------------------------------------------------------------
<a name="hierarchyLevel"></a> hierarchyLevel | gmd:hierarchyLevel/gmd:MD_ScopeCode/@codeListValue
<a name="linkage"></a> Linkage   | distributionInfo/\*/transferOptions/\*/onLine/\*/linkage

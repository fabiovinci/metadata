# INSPIRE Invocable Spatial Data Services metadata

Conformance Class 5 of the implementation of "INSPIRE dataset and service metadata based on ISO/TS 19139:2007" [INSPIRE Metadata](../README.md) based on the corresponding technical guidance [TG MD](#ref_TG_MD).

*Note*: It is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

## Standardization target type

 ISO/TS 19139:2007 Geographic information Metadata XML schema implementation.

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| INSPIRE Metadata | [Conformance Class 3](../sds/README.md) | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| INSPIRE Metadata | [Common Requirements](../common/README.md) | n/a |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| INT SDS <a name="ref_INT_SDS"></a> | [Commission Regulation (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| INT SDS AMD <a name="ref_INT_SDS_AMD"></a> | [Commission Regulation (EU) No 1312/2014 of 10 December 2014 amending Regulation (EU) No 1089/2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1312&from=EN)
| IR MD <a name="ref_IR_MD"></a>  | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [INSPIRE Metadata Technical Guidance version 1.3](http://inspire.jrc.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR NS AMD <a name="ref_IR_NS_AMD"></a> | [Commission Regulation (EU) No 1311/2014 of 10 December 2014 amending Regulation (EC) No 976/2009 as regards the definition of an INSPIRE metadata element](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32014R1311&from=EN)
| TG MD <a name="ref_TG_MD"></a> | [Technical Guidance for the implementation of INSPIRE dataset and service metadata based on ISO/TS 19139:2007, version 2.0](https://inspire.ec.europa.eu/sites/default/files/documents/metadata/inspire-tg-metadata-iso19139-2.0.1.pdf)
| SDS ALT <a name="ref_SDS_alt"></a> | Alternative approaches to implement Metadata for Spatial data services (not published?)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)

## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 5.1      | Spatial Data Service Type | [sds-type](./sds-type.md) | |
| 5.2      | Resource Locator Access Point | [access-point](./access-point.md) | |
| 5.3      | Data Quality Conformity | [conformity](./conformity.md) | |
| 5.4      | Spatial Data Service Category | [sds-category](./sds-category.md) | |
| 5.5      | Conformity to Technical Specifications | [conformity-to-technical-specifications](./conformity-to-technical-specifications.md) | |


## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [sds-type](./sds-type.md) | Ready for review  |
| [access-point](./access-point.md) | Ready for review  |
| [conformity](./conformity.md) | Ready for review  |
| [sds-category](./sds-category.md) | Ready for review  |
| [conformity-to-technical-specifications](./conformity-to-technical-specifications.md) | Ready for review  |


## Open issues


## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
gmd | http://www.isotc211.org/2005/gmd
srv | http://www.isotc211.org/2005/srv
inspire\_sds_gmd | [missing]
xlink          | http://www.w3.org/1999/xlink

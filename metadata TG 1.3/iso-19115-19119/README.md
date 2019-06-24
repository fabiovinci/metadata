# Conformance class: INSPIRE Profile based on EN ISO 19115 and EN ISO 19119 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE Metadata Technical Guidance](http://inspire.ec.europa.eu/id/ats/metadata/1.3).

## Standardization target type

ISO 19115/19119 metadata record

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the metadata record, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ISO 19115](#ref_ISO_19115) | n/a | n/a |
| [ISO 19119](#ref_ISO_19119) | n/a | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119](#ref_TG_MD) | [XML encoding](http://inspire.ec.europa.eu/id/ats/metadata/1.3/xml-encoding) | XML document (MD_Metadata) |  `encoding` = `ISO/TS 19139` or `CSW ISO AP 1.0.0` |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| IR MD <a name="ref_IR_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119, version 1.3](http://inspire.jrc.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
| REG <a name="ref_REG"></a> | [INSPIRE Registry](http://inspire.ec.europa.eu/registry/)
| ISO 19115 <a name="ref_ISO_19115"></a> | [ISO 19115:2003 Geographic information - Metadata](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26020)
| ISO 19119 <a name="ref_ISO_19119"></a> | [ISO 19119:2005 Geographic information - Services](http://www.iso.org/iso/catalogue_detail.htm?csnumber=39890)
| ISO 19108 <a name="ref_ISO_19108"></a> | [ISO 19108:2002 Geographic information -- Temporal schema](http://www.iso.org/iso/catalogue_detail.htm?csnumber=26013)
| ISO 8601 <a name="ref_ISO_8601"></a> | [ISO 8601:2004 Data elements and interchange formats -- Information interchange -- Representation of dates and times](http://www.iso.org/iso/catalogue_detail?csnumber=40874)


## TG Requirement coverage

Based on requirement numbering in [TG MD](#ref_TG_MD).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | hierachyLevel mandated               | [Hierarchy](./hierarchy) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1 |
| 2      | MD_ScopeCode values                  | [Hierarchy](./hierarchy) |[IR MD](#ref_IR_MD), Part B 1.3, Part D 1  |
| 3      | Resource Locator for data linkage    | [Dataset linkage](./ds-linkage) |[IR MD](#ref_IR_MD), Part B 1.4 |
| 4      | Resource Locator for service linkage | [Service linkage](./srv-linkage) | [IR MD](#ref_IR_MD), Part B 1.4 |
| 5      | Unique Resource Identifier code is mandatory | [Dataset identification](./ds-identification)|[IR MD](#ref_IR_MD) Part B 1.5 |
| 6      | Use RS_Identifier if URI codeSpace provided |[Dataset identification](./ds-identification) | [IR MD](#ref_IR_MD) Part B 1.5 |
| 7      | operatesOn as a reference     | [Coupled resource](./coupled-resource) | |
| 8      | Resource language is mandated        | [Dataset language](./ds-language) |[IR MD](#ref_IR_MD) Part B 1.7 |
| 9      | ISO 19139 codes used for language    | [Dataset language](./ds-language) | [IR MD](#ref_IR_MD) Part B 1.7 |
| 10     | Use MD_TopicCategoryCode values in topicCategory |[Dataset topic](./ds-topic) |[IR MD](#ref_IR_MD) Part B 2.1 |
| 11     | Use language neutral name in topicCategory | [Dataset topic](./ds-topic) |[IR MD](#ref_IR_MD) Part B 2.1|
| 12     | Use language neutral name for serviceType | [Service type](./srv-type) |[IR MD](#ref_IR_MD) Part B 2.2 |
| 13     | Provide at least one keyword         |[Keyword](./keyword) |[IR MD](#ref_IR_MD) Part B 3.1 |
| 14     | Provide at least one INSPIRE theme keyword | [Dataset keyword](./ds-keyword) |[IR MD](#ref_IR_MD) Part B 3.1  |
| 15     | Provide at least one service category keyword | [Service keyword](./srv-keyword) |[IR MD](#ref_IR_MD) Part B 1.5, Article 4, part D  |
| 16     | Use citation for other controlled keywords | [Vocabulary](./vocabulary) |[IR MD](#ref_IR_MD) Part B  3.2|
| 17     | Cite the originating controlled vocabulary |[Vocabulary](./vocabulary) |[IR MD](#ref_IR_MD) Part B 3.2|
| 18     | At least title and date for controlled vocabulary citations |[Vocabulary](./vocabulary) |[IR MD](#ref_IR_MD) Part B 3.2 |
| 19     | Group keywords from the same controlled vocabulary | [Keywords in vocabulary](./keywords-in-vocabulary) | [IR MD](#ref_IR_MD) Part B 3.2|
| 20     | Use the minimum geographic bounding box  | [Geographic bounding box](./geographic-bounding-box) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 21     | At least two decimals for coordinates | [Geographic bounding box](./geographic-bounding-box) | [IR MD](#ref_IR_MD) Part B. 4.1|
| 22     | Use at least one of INSPIRE temporal reference types | [Ds temporal](./ds-temporal) | [IR MD](#ref_IR_MD) Part B. 5.1|
| 23     | Use at least one ISO 19115 temporal reference types |[Ds temporal](./ds-temporal) |[IR MD](#ref_IR_MD) Part B. 5.1 |
| 24     | Gregorian calendar and ISO 8601 date as defaults | nothing to test, always true | [IR MD](#ref_IR_MD) Part B 5 |
| 25     | Single creation date mandatory       | [Resource creation date](./resource-creation-date) | [IR MD](#ref_IR_MD) Part B 5.4|
| 26     | Only one dataQualityInfo             | [Lineage](./lineage) |[IR MD](#ref_IR_MD) Part B. 2.6 |
| 27     | Spatial resolution as either scale or ground sample distance | [Ds spatial resolution](./ds-spatial-resolution) | [IR MD](#ref_IR_MD) Part B. 2.6|
| 28     | Degree of conformity mandatory       |[Dataset conformity](./ds-conformity) | [IR MD](#ref_IR_MD) Part B. 2.8|
| 29     | Use DQ_DomainConsistency for spec. conformity |[Ds specification](./ds-specification) | [IR MD](#ref_IR_MD) Part B. 7.2|
| 30     | Declare both limitations on "public access" and "constraints on access and use" |[Dataset public access](./ds-public-access) | [INSPIRE](#ref_INSPIRE), Article 13|
| 31     | At least one MD_Contraints even if no limitations |[Dataset public access](./ds-public-access) | n/a |
| 32     | Expressing limitations on public access |[Dataset public access](./ds-public-access) | n/a |
| 33     | No conditions and unknown conditions |[Dataset access use](./ds-access-use) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 34     | Terms and conditions either embedded or linked |[Dataset access use](./ds-access-use) | [IR MD](#ref_IR_MD) Part B. 8.2|
| 35     | Responsible organisation name and email |[Responsible party contact info](./responsible-party-contact-info) |[IR MD](#ref_IR_MD) Part B. 3.5 |
| 36     | MD_DataIdentification and SV_ServiceIdentification for responsible party info |[Responsible party contact info](./responsible-party-contact-info) | [IR MD](#ref_IR_MD) Part B. 3.5 |
| 37     | Metadata point of contact organisation name and email | [Metadata contact](./md-contact) |[IR MD](#ref_IR_MD) Part B. 10.1 |
| 38     | Metadata point of contact role code 'pointOfContact'| [Metadata contact role](./md-contact-role) | n/a |
| 39     | Metadata language is mandatory | [Language](./language) | [IR MD](#ref_IR_MD) Part B. 10.3|

## Test

This Conformance Class contains the following tests:

| Identifier                                                        | Status   |
| ----------------------------------------------------------------- | -------- |
| [Hierarchy](./hierarchy)           | Ready for review  |
| [Dataset keyword](./ds-keyword)                   | Ready for review  |
| [Service keyword](./srv-keyword)                   | Ready for review  |
| [Dataset identification](./ds-identification) | Ready for review  |
| [Dataset linkage](./ds-linkage)                   | Ready for review  |
| [Service linkage](./srv-linkage)                 | Ready for review  |
| [Dataset language](./ds-language)       | Ready for review  |
| [Dataset topic](./ds-topic)                       | Ready for review  |
| [Service type](./srv-type)                       | Ready for review  |
| [Keyword](./keyword)                         | Ready for review  |
| [Vocabulary](./vocabulary)                             | Ready for review  |
| [Keywords in vocabulary](./keywords-in-vocabulary)               | Ready for review  |
| [Geographic bounding box](./geographic-bounding-box)           | Ready for review  |
| [Dataset temporal](./ds-temporal)       | Ready for review  |
| [Lineage](./lineage)                   | Ready for review  |
| [Dataset conformity](./ds-conformity)             | Ready for review  |
| [Dataset specification](./ds-specification)       | Ready for review  |
| [Dataset public access](./ds-public-access) | Ready for review  |
| [Dataset access use](./ds-access-use)   | Ready for review  |
| [Responsible party contact info](./responsible-party-contact-info) | Ready for review  |
| [Metadata contact](./md-contact)                   | Ready for review  |
| [Metadata contact role](./md-contact-role)         | Ready for review  |
| [Language](./language)                       | Ready for review  |
| [Dataset spatial resolution](./ds-spatial-resolution) | Ready for review  |
| [Resource creation date](./resource-creation-date) | Ready for review |

Some additional metadata tests are available in the [conformance class 'Metadata for interoperability'](http://inspire.ec.europa.eu/id/ats/data/3.0rc3/Metadata-for-interoperability). These tests are separated from above because they have a different timeline for implementation.

## Vocabulary

<a name="emptychar"></a>
**Empty characterstring:** ISO/TS 19139 allows (if proper namespaces are available) to express any characterstring as either gco:CharacterString, gmd:Anchor or gmd:PT_FreeText.

To check an element for having an empty CharacterString, each of these representations should be considered. The PT_FreeText element can be used to supply multilingual values for a CharacterString.
If only PT_FreeText is used the validator should check if a value of the string is available in the main language of the document. gmx:Anchor is typically used to reference a URI on which additional information is available.
The validator could retrieve the resource at the URI in the gmx:Anchor to validate, if that content is available.

Some examples for valid string content:
```
  <gmd:keyword>
    <gco:CharacterString>Addresses</gco:CharacterString>
  </gmd:keyword>
```
  or
```
  <gmd:keyword>
    <gmx:Anchor xlink:href="http://www.eionet.europa.eu/gemet/en/inspire-theme/5297/">Addresses</gmx:Anchor>
  </gmd:keyword>
```
  or
```  
<abstract xsi:type="PT_FreeText_PropertyType">
  <gco:CharacterString>Brief narrative summary of the content of the
resource</gco:CharacterString>
  <!--== Alternative values ==-->
  <PT_FreeText>
    <textGroup>
      <LocalisedCharacterString locale="locale-fr">Résumé succint du contenu du jeu de données</LocalisedCharacterString>
    </textGroup>
    <textGroup>
      <LocalisedCharacterString locale="locale=it">
        Succinta descrizione del contenuto della risorsa
      </LocalisedCharacterString>
    </textGroup>
  </PT_FreeText>
</abstract>
```

## Open questions

* There is no explicit Implementation Requirement in [TG MD](./README#ref_TG_MD) for the following tests:
  * [Check title](./title)
  * [Check abstract](./abstract)
  * [Responsible party role](./responsible-party-role)
  
Should these be excluded or included in the ATS? Or added as requirements in the [TG MD](#ref_TG_MD)?

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix     | Namespace
---------- | -------------------------------------------------
gmd        | http://www.isotc211.org/2005/gmd
gco        | http://www.isotc211.org/2005/gco

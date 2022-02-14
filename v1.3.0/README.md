# wcia-lab-result-schema
Version control repository for the [Washington Cannabis Integrator's Alliance](https://www.cannabisintegratorsalliance.com/) Lab Result Schema.
[https://www.cannabisintegratorsalliance.com/](https://www.cannabisintegratorsalliance.com/)

### Version 1.3.0

----------------------------------------

## Lab Result Schema

* Lab Result Schema Object [(labResultSchema.json)](labResultSchema.json.json)
* Example of a Complete Result [(example.json)](example.json)

## Table of Contents

* Legend
* Fields Guide
* Resources

## Legend

```json
Ln #  Schema
----  --------------------------------------
1.    {                                      
2.      "document_name": "string",           
3.      "document_schema_version": "string", 
4.      "document_origin": "string", 
5.      "lab_name": "string", 
6.      "lab_ubi_license": "string", 
7.      "lab_ccrs_license": "string", 
8.      "labresult_id": "string",            
9.      "sample": {                          
10.       "id": "string",  
11.       "sample_source_id": "string"  
12.     },                                   
13.     "coa": "string",                     
14.     "status": "string",                  
15.     "metric_list": [                     
16.       {                                  
17.         "test_id": "string",             
18.         "test_type": "string",           
19.         "status": "nullable bool",       
20.         "metrics": [                     
21.           {                              
22.             "id": "string",              
23.             "name": "string",            
24.             "analyte_type": "string",    
25.             "qom": "string",             
26.             "uom": "string",             
27.             "status": "nullable bool"    
28.           }                              
29.         ]                                
30.       }                                  
31.     ],                                   
32.     "meta": {}                           
33.   }                                      
```

# Fields Guide

----------------------------------------

## Document Name
* _Field Name:_ **document_name**
* _Type:_ **string**
* _Description:_
    * The "title" of the document, always displaying "WCIA Lab Result Schema".
* _Legend:_ **Ln 2**

----------------------------------------

## Document Schema Version
* _Field Name:_ **document_schema_version**
* _Type:_ **string**
* _Description:_
    * The version of WCIA Lab Result Shema used for the object.
* _Legend:_ **Ln 3**

----------------------------------------

## Document Origin
* _Field Name:_ **document_origin**
* _Type:_ **string**
* _Description:_
  * A URL referencing the document's originating source.
* _Legend:_ **Ln 4**

----------------------------------------

## Lab Name
* _Field Name:_ **lab_name**
* _Type:_ **string**
* _Description:_
  * The name of the laboratory submitting the result.
* _Legend:_ **Ln 5**

----------------------------------------

## Lab UBI License
* _Field Name:_ **lab_ubi_license**
* _Type:_ **string**
* _Description:_
  * The UBI number of the laboratory submitting the result.
* _Legend:_ **Ln 6**

----------------------------------------

## Lab CCRS License
* _Field Name:_ **lab_ccrs_license**
* _Type:_ **string**
* _Description:_
  * The WA State Traceability System: CCRS License number of the laboratory submitting the result.
* _Legend:_ **Ln 7**

----------------------------------------

## Lab Result ID
* _Field Name:_ **labresult_id**
* _Type:_ **string**
* _Description:_
    * The Laboratory-assigned identifier, this is the ID used internally by the lab.
* _Legend:_ **Ln 8**

----------------------------------------

## Sample
* _Field Name:_ **sample**
* _Type:_ **object**
* _Description:_
    * An object containing properties associated with the sample transfer.
* _Legend:_ **Ln 9**

----------------------------------------

## Sample -> ID
* _Field Name:_**id**
* _Type:_ **string**
* _Description:_
    * A property of the Sample object, ID is the identifier representing the inventory lot
      from which the sample was taken.
* _Legend:_ **Ln 11

----------------------------------------

## Sample -> Sample Source ID
* _Field Name:_**sample_source_id**
* _Type:_ **string**
* _Description:_
  * A property of the Sample object, `sample_source_id` is an identifier representing the source lot
    from which the sample was taken.
* _Legend:_ **Ln 13

----------------------------------------

## CoA
* _Field Name:_ **coa**
* _Type:_ **string**
* _Description:_
    * A URL linking to the result's Certificate of Analysis (CoA).
* _Legend:_ **Ln 14**

----------------------------------------

## Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_ ddd
* _Legend:_ **Ln 15**

----------------------------------------

## Metric List
* _Field Name:_ **metric_list**
* _Type:_ **array**
* _Description:_
* An array of metrics. Metrics in this context are assays, or lab tests, intended to
  produce one or more analytes.
* _Legend:_ **Ln 16**

----------------------------------------

## Metric -> Test ID
* _Field Name:_ **test_id**
* _Type:_ **string**
* _Description:_
    * A unique identifier used by labs to distinguish a metric / assay / test type.
* _Legend:_ **Ln 17**

----------------------------------------

## Metric -> Test Type
* _Field Name:_ **test_type**
* _Type:_ **string**
* _Description:_
    * A name describing the metric / assay / test type.
* _Legend:_ **Ln 18**

----------------------------------------

## Metric -> Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_
    * A _pass|fail_ field indicating the overall pass or failure of a metric / assay /
      test.
* _Legend:_ **Ln 19**

----------------------------------------

## Metric -> Metrics
* _Field Name:_ **metrics**
* _Type:_ **array**
* _Description:_
    * A list of metrics, or analytes, produced by a metric / assay / test.
* _Legend:_ **Ln 20**

----------------------------------------
### Metric -> Metrics -> id
* _Field Name:_ **id**
* _Type:_ **string**
* _Description:_
    * A unique identifier, assigned by the lab, to distinguish an analyte from others.
* _Legend:_ **Ln 22**

----------------------------------------

### Metric -> Metrics -> Name
* _Field Name:_ **name**
* _Type:_ **string**
* _Description:_
    * A name describing an analyte under review.
* _Legend:_ **Ln 13**

----------------------------------------

### Metric -> Metrics -> Analyte Type
* _Field Name:_ **analyte_type**
* _Type:_ **string**
* _Description:_
    * A categorical description of an analyte.
* _Legend:_ **Ln 24**

----------------------------------------

### Metric -> Metrics -> QoM
* _Field Name:_ **qom**
* _Type:_ **string**
* _Description:_
    * Quantity of Measure; the quantity, or amount, measured.
* _Legend:_ **Ln 25**

----------------------------------------

### Metric -> Metrics -> UoM
* _Field Name:_ **uom**
* _Type:_ **string**
* _Description:_
    * Unit of Measure; the standardized unit used to gauge any physical property.
* _Legend:_ **Ln 26**

----------------------------------------

### Metric -> Metrics -> Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_
    * A _PASS/FAIL_ indicating an individual analyte's pass or failure status.
* _Legend:_ **Ln 27**

----------------------------------------

## Meta
* _Field Name:_ **meta**
* _Type:_ **object**
* _Description:_
    * An object intended to include meta data regarding the Lab result object.
* _Legend:_ **Ln 32**


### Resources

* [JSON Specification (RFC 8259)](https://www.ietf.org/rfc/rfc8259.txt)
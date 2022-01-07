# wcia-lab-result-schema
Version control repository for the [Washington Cannabis Integrator's Alliance](https://www.cannabisintegratorsalliance.com/) Lab Result Schema.
[https://www.cannabisintegratorsalliance.com/](https://www.cannabisintegratorsalliance.com/)

### Version 1.1.0

----------------------------------------

## Lab Result Schema

* Lab Result Schema Object [(labResultSchema.json)](labResultSchema.json)
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
4.      "labresult_id": "string",            
5.      "sample": {                          
6.        "id": "string"                     
7.      },                                   
8.      "coa": "string",                     
9.      "status": "string",                  
10.     "metric_list": [                     
11.       {                                  
12.         "test_id": "string",             
13.         "test_type": "string",           
14.         "status": "nullable bool",       
15.         "metrics": [                     
16.           {                              
17.             "id": "string",              
18.             "name": "string",            
19.             "analyte_type": "string",    
20.             "qom": "string",             
21.             "uom": "string",             
22.             "status": "nullable bool"    
23.           }                              
24.         ]                                
25.       }                                  
26.     ],                                   
27.     "meta": {}                           
28.   }                                      
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

## Lab Result ID
* _Field Name:_ **labresult_id**
* _Type:_ **string**
* _Description:_
    * The Laboratory-assigned identifier, this is the ID used internally by the lab.
* _Legend:_ **Ln 4**

----------------------------------------

## Sample
* _Field Name:_ **sample**
* _Type:_ **object**
* _Description:_
    * An object containing properties associated with the sample transfer.
* _Legend:_ **Ln 6**

----------------------------------------

## Sample -> ID
* _Field Name:_**id**
* _Type:_ **strain**
* _Description:_
    * A property of the Sample object, ID is the identifier representing the inventory lot
      from which the sample was taken.
* _Legend:_ **Ln 7

----------------------------------------

## CoA
* _Field Name:_ **coa**
* _Type:_ **string**
* _Description:_
    * A URL linking to the result's Certificate of Analysis (CoA).
* _Legend:_ **Ln 8**

----------------------------------------

## Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_ 
    * A _pass|fail_ field indicating the overall pass or failure of the entire lab result.
* _Legend:_ **Ln 9**

----------------------------------------

## Metric List
* _Field Name:_ **metric_list**
* _Type:_ **array**
* _Description:_
    * An array of metrics. Metrics in this context are assays, or lab tests, intended to
  produce one or more analytes.
* _Legend:_ **Ln 11**

----------------------------------------

## Metric -> Test ID
* _Field Name:_ **test_id**
* _Type:_ **string**
* _Description:_
    * A unique identifier used by labs to distinguish a metric / assay / test type.
* _Legend:_ **Ln 13**

----------------------------------------

## Metric -> Test Type
* _Field Name:_ **test_type**
* _Type:_ **string**
* _Description:_
    * A name describing the metric / assay / test type.
* _Legend:_ **Ln 14**

----------------------------------------

## Metric -> Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_
    * A _pass|fail_ field indicating the overall pass or failure of a metric / assay /
      test.
* _Legend:_ **Ln 15**

----------------------------------------

## Metric -> Metrics
* _Field Name:_ **metrics**
* _Type:_ **array**
* _Description:_
    * A list of metrics, or analytes, produced by a metric / assay / test.
* _Legend:_ **Ln 16**

----------------------------------------
### Metric -> Metrics -> id
* _Field Name:_ **id**
* _Type:_ **string**
* _Description:_
    * A unique identifier, assigned by the lab, to distinguish an analyte from others.
* _Legend:_ **Ln 18**

----------------------------------------

### Metric -> Metrics -> Name
* _Field Name:_ **name**
* _Type:_ **string**
* _Description:_
    * A name describing an analyte under review.
* _Legend:_ **Ln 19**

----------------------------------------

### Metric -> Metrics -> Analyte Type
* _Field Name:_ **analyte_type**
* _Type:_ **string**
* _Description:_
    * A categorical description of an analyte.
* _Legend:_ **Ln 20**

----------------------------------------

### Metric -> Metrics -> QoM
* _Field Name:_ **qom**
* _Type:_ **string**
* _Description:_
    * Quantity of Measure; the quantity, or amount, measured.
* _Legend:_ **Ln 21**

----------------------------------------

### Metric -> Metrics -> UoM
* _Field Name:_ **uom**
* _Type:_ **string**
* _Description:_
    * Unit of Measure; the standardized unit used to gauge any physical property.
* _Legend:_ **Ln 22**

----------------------------------------

### Metric -> Metrics -> Status
* _Field Name:_ **status**
* _Type:_ **string**
* _Description:_
    * A _pass|fail_ field indicating the individual analyte's pass or failure status.
* _Legend:_ **Ln 23**

----------------------------------------

## Meta
* _Field Name:_ **meta**
* _Type:_ **object**
* _Description:_
    * An object intended to include meta data regarding the Lab result object.
* _Legend:_ **Ln 28**


### Resources

* [JSON Specification (RFC 8259)](https://www.ietf.org/rfc/rfc8259.txt)

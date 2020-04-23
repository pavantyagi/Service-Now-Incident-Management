![alt text](https://digitalexchange.blueprism.com/dpCatalogForm/renderFile/fe5c17a0-ff99-4f4c-bbe6-fc0792132f40 "Blue Prism Developer")

<!-- [Markdown Cheetsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#links) -->

<!-- Asset Name -->
## 1. ServiceNow Incident Management API Capability

<!-- Asset Pitch -->
A Blue Prism skill that implements the ServiceNow Incident Management REST API interface.

This skill enables you to retrieve, create, update, and delete incident records.


To use this API, users must have one of the following roles: admin, web_service_admin, or rest_api_explorer.


### Whats Included:
+ ServiceNow Incident Management.bpskill - Blue Prism skill


#### Documentation
+ Blue_Prism_ServiceNow_Incident_Management_Skill_User_Guide.pdf


### Pre-Requisites
- Blue Prism v6.6


## 2. Getting Started:

- Review the ServiceNow API Documentation:
  - Go to https://developer.servicenow.com/app.do#!/home > Choose API from top ribbon, select REST in dropdown, scroll down to find the Table API information. The Table API is used to manage incidents. For further reading, please see: https://docs.servicenow.com/bundle/newyork-application-development/page/integrate/inbound-rest/concept/use-REST-API-Explorer.html#t_GetStartedRetrieveExisting
  

## 3. Using the Skill
> To use the ServiceNow Incident Management skill in Blue Prism:
- Download the [skill](#using-the-skill) directly.
- Import the skill file into Blue Prism.
- Open the Web API Service (in the System tab in the Blue Prism IDE) associated with the skill and copy your instance name into the space provided *[ServiceNow Instance]* in the field for Base URL.

Below is a list of available actions from the Web API:

### 3.1 Using the Skill

---
### Retrieve Incidents:
> Retrieves existing incident records.

Input Parameter | Type | Required | Description
------------  | ------------- | ------------- | -------------
name-value pairs|Text|N|Name-value pairs to use to filter the result set. This parameter is mutually exclusive with sysparm_query.
sysparm_display_value|Text|N|Data retrieval operation for reference and choice fields.
sysparm_exclude_reference_link|Flag|N|	Flag that indicates whether to exclude Table API links for reference fields.
sysparm_fields|Text|N|Comma-separated list of field names to return in the response.
sysparm_limit|Text|N|Maximum number of records to return. Unusually large sysparm_limit values can impact system performance. For requests that exceed this number of records, use the sysparm_offset parameter to paginate record retrieval.
sysparm_offset|Text|N|	Starting record index for which to begin retrieving records. Use this value to paginate record retrieval. 
sysparm_query|Text|N|Encoded query used to filter the result set.
sysparm_query_no_domain|Flag|N|Flag that indicates whether to restrict the record search to only the domains for which the logged in user is configured.
sysparm_suppress_pagination_header|Flag|N|Flag that indicates whether to remove the Link header from the response. 
sysparm_view|Text|N|UI view for which to render the data. Determines the fields returned in the response.
&nbsp;

Output Parameter | Type | Description
------------  | ------------- | -------------
Response_Content|Text|A JSON value containing response information related to the request.
HTTP Status Code|Text|HTTP Status code returned in response.
Response Headers|Collection|Collection of headers data returned in response.
&nbsp;

---
### Retrieve Incident By SysId:
> Retrieve a specific incident.

Input Parameter | Type | Required | Description
------------  | ------------- | ------------- | -------------
sys_id|Text|Y|Unique identifier of the incidet to retrieve.
&nbsp;

Output Parameter | Type | Description
------------  | ------------- | -------------
Response_Content|Text|A JSON value containing response information related to the request.
HTTP Status Code|Text|HTTP Status code returned in response.
Response Headers|Collection|Collection of headers data returned in response.
&nbsp;

---
### Create Incident:
> Creates a new incident record with the passed-in parameters.

Input Parameter | Type | Required | Description
------------  | ------------- | ------------- | -------------
body|Text|N|Optional parameters (see Service Now API doc).
&nbsp;

Output Parameter | Type | Description
------------  | ------------- | -------------
Response_Content|Text|A JSON value containing response information related to the request.
HTTP Status Code|Text|HTTP Status code returned in response.
Response Headers|Collection|Collection of headers data returned in response.
&nbsp;

---
### Update Incident By SysId:
> Updates the specified incident record with the passed-in parameters.

Input Parameter | Type | Required | Description
------------  | ------------- | ------------- | -------------
sys_id|Text|Y|Unique identifier of the incidet to update.
body|Text|N|Optional parameters (see Service Now API doc).
&nbsp;

Output Parameter | Type | Description
------------  | ------------- | -------------
Response_Content|Text|A JSON value containing response information related to the request.
HTTP Status Code|Text|HTTP Status code returned in response.
Response Headers|Collection|Collection of headers data returned in response.
&nbsp;

---


# FHIR API HOOK by SOA Software
(http://soa.com) 
Link to product documentation and product overview page
## FHIR API 
### About the API
FHIR - is the a next generation standards framework created by HL7.  FHIR combines the best features of HL7's Version 2, Version 3 and CSA product lines while leveraging the latest web standards and applying a tight focus on implementability. 
- Home Page: FHIR - [Fast Healthcare Interoperability Resources] (http://hl7.org/fhir)
- API Documentation: [FHIR RESTful API] (http://www.hl7.org/implement/standards/fhir/http.html)
- Reference Implementation - [FHIR server] (http://fhir.healthintersections.com.au/)

### Pre-Reqs
- None

### Getting Started Instructions
#### Download and Import
##### Two Options
###### Option 1
- Simply download the FHIR.raml (https://github.com/lheritage/FHIR/tree/master/src/FHIR.raml)
- Create a physical and virtual service using this RAML document

###### Option 2
- Download FHIRAPIHook.zip (https://github.com/lheritage/FHIR/tree/master/dist)
- Login to PolicyManager  example: http://localhost:9900
- Select the parent organization you want to import the API Hook into.  The import will create a whole new organization.  Click on the "Import Package" from the Actions navigation window on the right side of the screen
  - click on button to browse for the org_SmartyStreetOrg_export.zip archive file and click Okay.

#### Verify Import
Only if you chose Option 2 above.
- Expand the organization you imported into.  You should now see a new organization called HealthcareOrg.
- Expand the services folder of the HealthcareOrg.  You should see one physical and one virtual service.
- Expand scripts.  You should see OpenAPI-Common

#### Configure Security
- No security is required to access the reference server implementation.  
- If connecting to your FHIR server implementation you will need to apply security.

#### Policy Activation
- No policy activation at this time


#### Offer an Anonymous Contract
- Click on the Virtual Service
- From the Details tab, click on Offer Contract from the Actions pane on the right
- Give a Contract Name
- In the Access Control box, select "Allow consumer (application or organization) users that do not have a contract explicitly assigned"
- Once contract is created, it will appear in the Consumers section on the Details tab with the Approval Status shown as "Draft".   We need to activate it. 
- Click on the contract you created.
- In the Contract Workflow pane over on the right, click on "Activate Contract"
- You are now done

#### Verify Connectivity
- Using your browser http://{Your HOST example: localhost:9901}/fhir/v1/patient/1

### Modify and Build
In the event you need to change the API Hook.   Here are the instructions to do so. 

### License
Put a link to an open source license

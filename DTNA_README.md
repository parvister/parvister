
# GENETAL NOTES
------------------------------------------------------------

Timeline RPQ: 3/25
3-4 days for answers to questions

Sudhar experience with DTNM
Anuragg: modeling (maybe DS)

CI/CD: Azure ML Studio (need to see integration) & Azure DevOps


# Landscape

Team, projects, status, onboarding process

Trushant: customer in PDX - enagement manager TBB (thomas build buses)
Yogi in PDX: 


## DTNM
-------------------------------------------------
Scout Darren: Database Manager for Hana - Data Warehouse
Doughlas Morphy: creates use-cases, use-case development with ROI
	- Sargent Petal
	- Supnil: non-telematic use-cases

technology: 
1. Telemtry Group >> Brett Hutton, but no analytics, completely on the cloud (cost savings!) (migrate data accisition) ASDL, HBase, EventHub, Java
	1. Wind channel ???
	1. Truck & faults - 1TB/day --- 15 electric trucks 3TB/day


Use-cases for Trucks:
1. Waranties
1. Smart alarms: false alarms, not to come to dealerships, 


Scout Darren:
mainframe, manufacturing, sales >> mainfram (DB2) >> SAP Hana (strategic data warehouse)
decomission all other data warehouses (DB2, etc)
He lives SAP Hana, everything should be complementary to SAP Hana. 
Scout use-cases
1. dashabording, 
1. **AI/ML on top of Hana**

### Interests (Hana)
They're lacking metadata management and data governance
They're interested in **data taps**
**DATA AS A PRODUCT**

on-prem.

Need help right now:
* CLUE, CI/CD
* Add my questions to the RFQ

Email, DOB


How to approach Doug:
- Architect over the top
- many teams have approach me, I can add value 
- let's speak with yogi
- anomoly detection 
- I work hands on with the team 


## Daimler Trucks

steve.sawrey@daimler.com
douglas.murphy@daimler.com


# ODBC - SAP HANA TO ADX
----------------------------------------------------

suggestions:

1. ADF COPY activity with ODBC
	- [Parrallel copy with custom partitioning](https://docs.microsoft.com/en-us/azure/data-explorer/data-factory-integration)
	- bulk template: https://docs.microsoft.com/en-us/azure/data-explorer/data-factory-template
1. Event Hub
	- Bulk load with files: ADLSv2 parquet files (1GB) **DAILY EXPORT**
		- append only tables
		- update tables
		- small tables
	- Delta in Event Hubs


# Sharing Data Externally
-----------------------------------------------------

logging and auditing: https://docs.microsoft.com/en-us/azure/security/fundamentals/log-audit

resource tagging: https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/decision-guides/resource-tagging/

tagging strategy: https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/ready/azure-best-practices/resource-tagging

Blog index tags: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-index-how-to?tabs=azure-portal

Role Based Access with Blob index tags: https://docs.microsoft.com/en-us/azure/storage/blobs/storage-manage-find-blobs?tabs=azure-portal

Using Blob Index Keys with Azure RBAC: https://docs.microsoft.com/en-us/azure/role-based-access-control/conditions-overview


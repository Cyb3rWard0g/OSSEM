# OSSEM

[![Open Source Love](https://badges.frapsoft.com/os/v3/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
![Open_Threat_Research Community](https://img.shields.io/badge/Open_Threat_Research-Community-brightgreen.svg)
[![Twitter](https://img.shields.io/twitter/follow/OSSEM_Project.svg?style=social&label=Follow)](https://twitter.com/OSSEM_Project)

The Open Source Security Events Metadata (OSSEM) is a community-led project that focuses primarily on the documentation and standardization of security event logs from diverse data sources and operating systems. Security events are documented in a dictionary format and can be used as a reference while mapping data sources to data analytics used to validate the detection of adversarial techniques. In addition, the project provides a common data model (CDM) that can be used for data engineers during data normalization procedures to allow security analysts to query and analyze data across diverse data sources. Finally, the project also provides documentation about the structure and relationships identified in specific data sources to facilitate the development of data analytics.

# Goals

* Define and share a common data model in order to improve the data standardization and transformation of security event logs
* Define and share data structures and relationships identified in security events logs
* Provide detailed information in a dictionary format about several security event logs to the community
* Learn more about security event logs (Windows, Linux, MacOS, Azure, AWS, etc)
* Have fun and think more about the data structure in your SIEM when it comes down to detection!!

# Project Structure

There are three main folders:

* **Common Data Model (CDM)**:
  * Facilitates the normalization of data sets by providing a standard way to parse security event logs.
  * It is organized by specific [schema entities](https://github.com/OTRF/OSSEM-CDM/tree/master/schemas/entities) identified in several data sources.
  * The definitions of each schema entity and its respective attributes (field names) are mostly general descriptions that could help and expedite event logs parsing procedures.
  * Besides data [schema entities](https://github.com/OTRF/OSSEM-CDM/tree/master/schemas/entities), it provides the concept of [schema tables](https://github.com/OTRF/OSSEM-CDM/tree/master/schemas/tables) to aggregate common entities that can be used to parse several data sources with similar context. For example, the HTTP,Port and User Agent entities can be used to normalize data providing context about the network traffic metadata captured in a network environment. 
* **Data Dictionaries (DD)**:
  * Contains specific information about several security event logs organized by operating system and their respective data providers
  * Each dictionary describes a single event log and its corresponding event field names
  * It provides the foundational concepts to create a data wiki in an organization.
* **Detection Data Model (DDM)**:
  * Focuses on defining the required data in form of data objects and relationships among each other needed to facilitate the creation of data analytics and validate the detection of adversary techniques
  * Developed initially to extend the definitions of ATT&CK Data Sources.
    * [MITRE ATT&CKcon 2018: Hunters ATT&CKing with the Data](https://youtu.be/QCDBjFJ_C3g)
    * [MITRE ATT&CKcon 2.0: Ready to ATT&CK? Bring Your Own Data (BYOD) and Validate Your Data Analytics!](https://youtu.be/eM0c_Gil-38)
  * Initial work in this project has been migrated to ATT&CK and improved by [@Cyb3rPandah](https://twitter.com/Cyb3rPandaH)
    * [Defining ATT&CK Data Sources, Part I: Enhancing the Current State](https://medium.com/mitre-attack/defining-attack-data-sources-part-i-4c39e581454f)
    * We are currently extending the model to map security events to the relationships identified in ATT&CK.

# Author

* Roberto Rodriguez [@Cyb3rWard0g](https://twitter.com/Cyb3rWard0g)

# Current Committers

* Jose Luis Rodriguez [@Cyb3rPandaH](https://twitter.com/Cyb3rPandaH)
* Nate Guagenti [@neu5ron](https://twitter.com/neu5ron)
* Ricardo Dias [@hxnoyd](https://twitter.com/hxnoyd)

# Projects Using OSSEM

* [HELK](https://github.com/Cyb3rWard0g/HELK)
* [Azure Sentinel Normalization](https://docs.microsoft.com/en-us/azure/sentinel/normalization-schema)

# Resources

* [Ready to hunt? First, Show me your data!](https://cyberwardog.blogspot.com/2017/12/ready-to-hunt-first-show-me-your-data.html)
* [What's new in Windows 10, versions 1507 and 1511](https://docs.microsoft.com/en-us/windows/whats-new/whats-new-windows-10-version-1507-and-1511#bkmk-lsass)
* [Download Security Audit Events for Windows (Spreadsheet)](https://www.microsoft.com/en-us/download/details.aspx?id=50034)
* [Advanced Security Audit Policy Settings](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/advanced-security-audit-policy-settings)
* [Monitoring Active Directory for Signs of Compromise](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/monitoring-active-directory-for-signs-of-compromise#audit-account-management)
* [Audit Policy Recommendations](https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/audit-policy-recommendations)
* [Use Windows Event Forwarding to help with intrusion detection](https://docs.microsoft.com/en-us/windows/security/threat-protection/use-windows-event-forwarding-to-assist-in-intrusion-detection)
* [Minimum recommended minimum audit policy](https://docs.microsoft.com/en-us/windows/security/threat-protection/use-windows-event-forwarding-to-assist-in-intrusion-detection#a-href-idbkmk-appendixaaappendix-a---minimum-recommended-minimum-audit-policy)
* [Windows ITPro Docs - Threat Protection](https://github.com/MicrosoftDocs/windows-itpro-docs/tree/master/windows/security/threat-protection)

###### \# 🧾 Saudi Retail Invoice Processing Automation (UiPath REFramework)

###### 

###### An end-to-end Enterprise RPA solution built using \*\*UiPath REFramework\*\* to automate the validation, processing, and recording of purchase invoices for the retail and supply chain sector in Saudi Arabia.

###### 

###### \---

###### 

###### \## 📌 Project Overview

###### This project processes vendor purchase invoices from input Excel files, validates data integrity against local accounting/VAT regulations, and pushes valid transactions for downstream ERP/Accounting entry while handling business exceptions gracefully.

###### 

###### \### Key Features:

###### \- \*\*Architecture:\*\* Built on UiPath Robotic Enterprise Framework (REFramework) for high reliability and scalability.

###### \- \*\*Queue Management:\*\* Utilizes UiPath Orchestrator Queues (`Shared` Folder) for transaction tracking.

###### \- \*\*Business Rule Validation:\*\*

###### &#x20; - Validates Invoice Amounts (Must be > 0).

###### &#x20; - Validates Saudi VAT Number formats and vendor metadata.

###### \- \*\*Exception Handling:\*\* Categorizes errors into `BusinessRuleException` (invalid data) and `SystemException` (app failures).

###### \- \*\*Reporting:\*\* Generates structured execution reports summarizing successful and failed invoice items.

###### 

###### \---

###### 

###### \## 🛠️ Tech Stack \& Tools

###### \- \*\*UiPath Studio\*\* (Windows / Modern Activities)

###### \- \*\*UiPath Orchestrator\*\* (Queues \& Assets)

###### \- \*\*Excel \& Workbook Automation\*\*

###### \- \*\*VB.NET\*\*

###### 

###### \---

###### 

###### \## 🏗️ Workflow Architecture

###### 

###### 1\. \*\*Initialization (`InitAllSettings.xaml`):\*\*

###### &#x20;  - Reads configuration parameters from `Data/Config.xlsx`.

###### &#x20;  - Initializes applications and sets up Orchestrator dependencies.

###### 2\. \*\*Get Transaction Data (`GetTransactionData.xaml`):\*\*

###### &#x20;  - Reads raw invoice rows and uploads them to the Orchestrator Queue on the first run.

###### &#x20;  - Fetches transaction items one by one from the Queue.

###### 3\. \*\*Process Transaction (`Process.xaml`):\*\*

###### &#x20;  - Applies business logic and VAT validation rules.

###### &#x20;  - Throws `BusinessRuleException` for invalid items without re-trying.

###### 4\. \*\*End Process (`CloseAllApplications.xaml`):\*\*

###### &#x20;  - Closes open applications and logs execution metrics.

###### 

###### \---

###### 

###### \## 🚀 How to Run

###### 1\. Clone this repository:

###### &#x20;  ```bash

###### &#x20;  git clone \[https://github.com/elbashirCode/Invoice_RPA.git](https://github.com/elbashirCode/Invoice_RPA.git)


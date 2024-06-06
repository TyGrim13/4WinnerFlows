# 4WinnerFlows
Workflows ERP

Hierarchy Structure
CEO: Tom is the Chief Executive Officer who oversees all departments.

Sales Department:
Managed by Julie. All sales people report to Julie. All managers and excalations are reported to Julie and/or Tom.
The sales team includes Enzo, Epsteine, and Tom, who also serves as the CEO.
Digital Agency Department:

Digital Agency Department:
Managed by Ty. All departments supervisors report to Ty.
Web Development is supervised by Ty.
Marketing is supervised by Luis.
Graphic Design is supervised by Jordan, with team members Alex and Roselle.
Manufacturing Department:

Production/Warehouse
Managed by Dave. All departments supervisors report to Dave.
Receiving does not have a specified supervisor.
Screen Printing is supervised by TJ, with Brandon, Juana, and Leni as team members.
Embroidery is supervised by Jessica, with Emily and Leni as a team member.
Vinyl Heat Press is supervised by Otero.
Quality Control is supervised by Juana.
Fulfillment/Shipping is supervised by Danale.

```mermaid

flowchart TD
    CEO[Tom] & Eric
    SalesDept[Sales Department]
    SalesMgr[Manager: Julie]
    Enzo[Enzo]
    Epsteine[Epsteine]
    TomAsSales[Tom as CEO and Sales]
    CEO --> SalesDept
    SalesDept --> SalesMgr
    SalesMgr --> Enzo
    SalesMgr --> Epsteine
    SalesMgr --> TomAsSales

    DigitalAgency[Digital Agency Department]
    DigitalMgr[Manager: Ty]
    WebDev[Web Development]
    WebSup[Supervisor: Ty]
    Marketing[Marketing]
    MarkSup[Supervisor: Luis]
    GraphicDesign[Graphic Design]
    GDSup[Supervisor: Jordan]
    Alex[Alex]
    Roselle[Roselle]
    CEO --> DigitalAgency
    DigitalAgency --> DigitalMgr
    DigitalMgr --> WebDev
    WebDev --> WebSup
    DigitalMgr --> Marketing
    Marketing --> MarkSup
    DigitalMgr --> GraphicDesign
    GraphicDesign --> GDSup
    GDSup --> Alex
    GDSup --> Roselle

    Manufacturing[Manufacturing Department]
    ManuMgr[Manager: Dave]
    Receiving[Receiving]
    RecSup[Supervisor: Not specified]
    ScreenPrinting[Screen Printing]
    SP[Supervisor: Brandon]
    SPTJ[TJ]
    SPJuana[Juana]
    SPLeni[Leni]
    Embroidery[Embroidery]
    EmbSup[Supervisor: Jessica]
    Emily[Emily]
    VinylHeatPress[Vinyl Heat Press]
    VHP[Supervisor: Otero]
    QualityControl[Quality Control]
    QCSup[Supervisor: Not specified]
    FulfillmentShipping[Fulfillment/Shipping]
    FulfillSup[Supervisor: Danale]
    CEO --> Manufacturing
    Manufacturing --> ManuMgr
    ManuMgr --> Receiving
    Receiving --> RecSup
    ManuMgr --> ScreenPrinting
    ScreenPrinting --> SP
    SP --> SPTJ
    SP --> SPJuana
    SP --> SPLeni
    ManuMgr --> Embroidery
    Embroidery --> EmbSup
    EmbSup --> Emily
    ManuMgr --> VinylHeatPress
    VinylHeatPress --> VHP
    ManuMgr --> QualityControl
    QualityControl --> QCSup
    ManuMgr --> FulfillmentShipping
    FulfillmentShipping --> FulfillSup


```



OVERDUE TASKS NOTIFICATION

 Notification Flowchart for Overdue Tasks
1. Task Due Date: The due date for the task is set.
2. Check if Task is Past Due:
   Task is Past Due then If the task is past due, a notification is sent to the supervisor and manager.
3. Monitor Task Status: The task status is monitored.
4. Check if Task is Overdue for 3 Days:
    Task is Overdue for 3 Days: If the task is overdue for three days, a notification is sent to the supervisor, manager, and CEO.


```mermaid

flowchart TD
    I1[Task Due Date]
    I2{Check if Task is Past Due}
    I3[Task is Past Due]
    I4[Send Notification to Supervisor and Manager]
    I5[Monitor Task Status]
    I6{Check if Task is Overdue for 3 Days}
    I7[Task is Overdue for 3 Days]
    I8[Send Notification to Supervisor, Manager, and CEO]

    I1 --> I2
    I2 -->|Yes| I3
    I2 -->|No| I5
    I3 --> I4
    I4 --> I5
    I5 --> I6
    I6 -->|Yes| I7
    I6 -->|No| I1
    I7 --> I8

```
SALES WORKFLOW

1. Lead Generation: The process starts with generating leads through various marketing and outreach efforts.
2. Initial Contact FollowUp Date: A followup date is set for the initial contact with the lead.
3. Check Contact Made by FollowUp Date:
    Contact Made: If contact is made, update the lead status and set the next followup.
    No Contact Made: If no contact is made, notify the sales rep.
    Check Contact Made in 3 Days: If no contact is made within three days, notify the sales manager.
4. Lead Status Update: Update the lead status accordingly.
    Send Next FollowUp: Send the next followup message.
    Lead Conversion: If the lead converts, notify the sales manager, update the CRM system, and notify relevant departments.
5. Monitor Stale Leads:
    Check Lead Contact/Update in 30 Days: If the lead has not been updated in 30 days, take action.
      Lead Updated: If the lead is updated, continue with the normal process.
      Lead Not Updated: If the lead is not updated, notify the sales rep.
      Check Action in 3 Days: If no action is taken in three days, notify the sales manager.

```mermaid

flowchart TD
    A1[Lead Generation]
    A2[Initial Contact FollowUp Date]
    A3{Check Contact Made by FollowUp Date}
    A3a[Contact Made]
    A3b[No Contact Made]
    A3c[Notify Sales Rep]
    A3d{Check Contact Made in 3 Days}
    A3e[No Contact Made in 3 Days]
    A3f[Notify Sales Manager]
    A4[Lead Status Update]
    A4a[Send Next FollowUp]
    A4b[Lead Conversion]
    A4c[Notify Sales Manager]
    A4d[Update CRM System]
    A4e[Notify Relevant Departments]
    A5[Monitor Stale Leads]
    A5a{Check Lead Contact/Update in 30 Days}
    A5b[Lead Updated]
    A5c[Normal Process]
    A5d[Lead Not Updated]
    A5e[Notify Sales Rep]
    A5f{Check Action in 3 Days}
    A5g[No Action Taken]
    A5h[Notify Sales Manager]

    A1 --> A2
    A2 --> A3
    A3 -->|Yes| A3a
    A3 -->|No| A3b
    A3a --> A4
    A3b --> A3c
    A3c --> A3d
    A3d -->|Yes| A4
    A3d -->|No| A3e
    A3e --> A3f
    A4 --> A4a
    A4a --> A4b
    A4b --> A4c
    A4b --> A4d
    A4b --> A4e
    A5 --> A5a
    A5a -->|Yes| A5b
    A5a -->|No| A5d
    A5b --> A5c
    A5d --> A5e
    A5e --> A5f
    A5f -->|No| A5g
    A5g --> A5h

```

DIGITAL AGENCY WORKFLOW

1. Project Initiation: The project begins with initiation.
2. Project Planning: Detailed planning of the project occurs.
3. Task Assignment: Tasks are assigned to team members.
4. Task Execution: Team members execute the assigned tasks.
5. Quality Assurance: The quality of the tasks is assured.
    Client Approval: The client reviews the deliverables.
       Revisions Needed: If revisions are needed, they are made and tasks are executed again.
6. Project Completion: The project is completed.
7. Project Delivery: The project deliverables are handed over to the client.
8. PostProject Review: A review of the project is conducted to identify lessons learned.
```mermaid
flowchart TD
    B1[Project Initiation]
    B2[Project Planning]
    B3[Task Assignment]
    B4[Task Execution]
    B5[Quality Assurance]
    B5a{Client Approval}
    B5b[Revisions Needed]
    B5c[Revisions]
    B5d[Task Execution]
    B6[Project Completion]
    B7[Project Delivery]
    B8[PostProject Review]

    B1 --> B2
    B2 --> B3
    B3 --> B4
    B4 --> B5
    B5 --> B5a
    B5a -->|Yes| B6
    B5a -->|No| B5b
    B5b --> B5c
    B5c --> B5d
    B6 --> B7
    B7 --> B8


```

GRAPHIC DESIGN WORKFLOW

1. Design Request Reception: Design requests are received.
2. Initial Design Variations: Initial design variations are created.
3. Client Feedback: Client provides feedback on the designs.
4. Design Finalization: The final design is prepared based on feedback.
5. Design Submission for Approval:
    Revisions Needed: If revisions are needed, they are made.
6. Final Approval: The final design is approved by the client.
7. Design Delivery: The approved design is delivered to the client.
```mermaid
flowchart TD
    E0[Design request for filed out buy client on website]
    E1[Design Request Reception by manager]
    E2[Initial Design Variations]
    E3[Client Feedback]
    E4[Design Finalization]
    E5[Design Submission for Approval]
    E5a{Revisions Needed}
    E5b[Revisions]
    E6[Final Approval]
    E7[Design Delivery]

    E0 --> E1
    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 --> E5
    E5 --> E5a
    E5a -->|Yes| E5b
    E5a -->|No| E6
    E5b --> E4
    E6 --> E7

```

RECIEVING/INVENTORY WORKFLOW

1. Order Placement and Notification: Orders are placed and notifications are sent.
2. Receiving Shipment: The shipment is received.
3. Inspection and Quality Control:
    Items Fail Inspection: If items fail inspection, they are returned to the supplier or marked for rework.
4. Inventory Update: The inventory is updated.
5. Storage Allocation: Allocate storage space for the items.
6. PutAway Process: The items are put away in their designated storage locations.
7. Inventory Tracking: The inventory is tracked.
8. Order Fulfillment: Orders are fulfilled from the inventory.

```mermaid
flowchart TD

    C1[Order Placement and Notification]
    C2[Receiving Shipment]
    C3[Inspection and Quality Control]
    C3a{Items Fail Inspection}
    C3b[Return to Supplier/Mark for Rework]
    C4[Inventory Update]
    C5[Storage Allocation]
    C6[PutAway Process]
    C7[Inventory Tracking]
    C8[Order Fulfillment]

    C1 --> C2
    C2 --> C3
    C3 --> C3a
    C3a -->|Yes| C3b
    C3a -->|No| C4
    C4 --> C5
    C5 --> C6
    C6 --> C7
    C7 --> C8

```

SCREEN PRINTING WORKFLOW

1. Order Reception: Orders are received.
2. Material Collection: Materials required for the order are collected.
3. Screen Preparation: Screens are prepared for printing.
4. Press Setup: The press is set up for printing.
5. Printing: The printing process is executed.
6. Drying: Printed items are dried.
7. Quality Check: Quality of the printed items is checked.
    Rework Needed: If rework is needed, the items are sent back for rework.
8. Packaging and Fulfillment: Items are packaged and fulfilled.

```mermaid
flowchart TD
    D1[Order Reception]
    D2[Material Collection]
    D3[Screen Preparation]
    D4[Press Setup]
    D5[Printing]
    D6[Drying]
    D7[Quality Check]
    D7a{Rework Needed}
    D7b[Rework Process]
    D8[Packaging and Fulfillment]
    D9[Damages Report]
    D10[Update Inventory]
    D11[Account for Tax Write-Off]

    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> D5
    D5 --> D6
    D6 --> D7
    D7 --> D7a
    D7a -->|Yes| D7b
    D7a -->|No| D8
    D7a -->|Damaged| D9
    D9 --> D10
    D10 --> D11
    D7b --> D5
    D8

```
EMBROIDERY WORKFLOW

1. Order Reception: Orders are received.
2. Material Collection: Materials required for the order are collected.
3. Design Setup: Design is set up for embroidery.
4. Embroidery Process (Start Job Timer): Embroidery process starts, and the job timer is initiated.
5. Quality Check: The quality of the embroidered items is checked.
    Rework Needed: If rework is needed, the items are sent back for rework.
6. Packaging and Fulfillment: Embroidered items are packaged and fulfilled.
7. 
```mermaid
flowchart TD
    F1[Order Reception]
    F2[Material Collection]
    F3[Design Setup]
    F4[Embroidery Process Start Timer]
    F5[Quality Check]
    F5a{Rework Needed}
    F5b[Rework Process]
    F6[Packaging and Fulfillment]
    F7[Damages Report]
    F8[Update Inventory]
    F9[Account for Tax Write-Off]

    F1 --> F2
    F2 --> F3
    F3 --> F4
    F4 --> F5
    F5 --> F5a
    F5a -->|Yes| F5b
    F5a -->|No| F6
    F5a -->|Damaged| F7
    F7 --> F8
    F8 --> F9
    F5b --> F4
    F6



```

HEATTRANSFER WORKFLOW

1. Order Reception: Orders are received.
2. Material Collection: Materials required for the order are collected.
3. Design Setup: Design is set up for the vinyl heat press.
4. Vinyl Heat Press Process (Start Job Timer): The vinyl heat press process starts, and the job timer is initiated.
5. Quality Check: The quality of the heatpressed items is checked.
    Rework Needed: If rework is needed, the items are sent back for rework.
6. Packaging and Fulfillment: Heatpressed items are packaged and fulfilled.
```mermaid
flowchart TD
    %% Vinyl Heat Press Department Flowchart %%
    G1[Order Reception]
    G2[Material Collection]
    G3[Design Setup]
    G4[Vinyl Heat Press Process Start Timer]
    G5[Quality Check]
    G5a{Rework Needed}
    G5b[Rework Process]
    G6[Packaging and Fulfillment]

    G1 --> G2
    G2 --> G3
    G3 --> G4
    G4 --> G5
    G5 --> G5a
    G5a -->|Yes| G5b
    G5a -->|No| G6
    G5b --> G4
    G6



```

FULFILLMENT WORKFLOW

1. Order Reception: Orders are received.
2. Packaging Preparation: Packaging is prepared.
3. Item Packaging: Items are packaged.
4. Quality Assurance Check: The quality of the packaging is checked.
    Reproduction Needed: If reproduction is needed, the process is initiated.
5. Shipping Preparation: Items are prepared for shipping.
6. Shipping and Dispatch: Items are shipped and dispatched.
7. Customer Notification: Customers are notified of the shipment.
8. Order Completion: Orders are marked as complete.
9. Returns Handling: Returns are handled.
10. Returns Inspection: Returns are inspected.
     Reproduction Needed: If reproduction is needed, the process is initiated.
11. Communicate with Customer: Communication is maintained with the customer.
    
```mermaid
flowchart TD
    H1[Order Reception]
    H2[Packaging Preparation]
    H3[Item Packaging]
    H4[Quality Assurance Check]
    H4a{Reproduction Needed}
    H4b[Reproduction Process]
    H5[Shipping Preparation]
    H6[Shipping and Dispatch]
    H7[Customer Notification]
    H8[Order Completion]
    H9[Returns Handling]
    H10[Returns Inspection]
    H10a{Reproduction Needed}
    H10b[Reproduction Process]
    H11[Communicate with Customer]

    H1 --> H2
    H2 --> H3
    H3 --> H4
    H4 --> H4a
    H4a -->|Yes| H4b
    H4a -->|No| H5
    H4b --> H2
    H5 --> H6
    H6 --> H7
    H7 --> H8
    H8 --> H9
    H9 --> H10
    H10 --> H10a
    H10a -->|Yes| H10b
    H10a -->|No| H11
    H10b --> H2
    H11 --> H12


```

CLOSING SALES & COMMISSION PAYOUT FLOW

1. Deal Closed by Salesperson: The salesperson closes the deal with the client.
2. Client Signs All Documents and Terms: The client signs all necessary documents and terms.
3. Receive Necessary Documents and Logo Files from Client: The necessary documents and logo files are received from the client.
4. Upload Documents for Approval: The documents are uploaded for approval.
5. Are All Documents Approved?:
    Documents Approved: If all documents are approved, proceed to close the sale.
    Documents Not Approved: If documents are not approved, they are sent back to the salesperson for completion and resubmission.
6. Sale Closed: The sale is marked as closed.
7. Commission Paid Out within Specified Time: The commission is paid out to the salesperson within the specified time.
8. Send Documents Back to Salesperson for Completion: If documents are not approved, they are sent back to the salesperson for completion and resubmission.

```mermaid
flowchart TD
    A1[Deal Closed by Salesperson]
    A2[Client Signs All Documents and Terms]
    A3[Receive Necessary Documents and Logo Files from Client]
    A4[Upload Documents for Approval]
    A5{Are All Documents Approved?}
    A5a[Documents Approved]
    A5b[Documents Not Approved]
    A6[Sale Closed]
    A7[Commission Paid Out within Specified Time]
    A8[Send Documents Back to Salesperson for Completion]

    A1 --> A2
    A2 --> A3
    A3 --> A4
    A4 --> A5
    A5 -->|Yes| A5a
    A5 -->|No| A5b
    A5a --> A6
    A6 --> A7
    A5b --> A8
    A8 --> A4


```


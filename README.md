# 4WinnerFlows
Workflows ERP Docs

```mermaid
NOTIFICATIONS

OVERDUE TASK

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


SALES

flowchart TD
    A1[Lead Generation]
    A2[Initial Contact Follow-Up Date]
    A3{Check Contact Made by Follow-Up Date}
    A3a[Contact Made]
    A3b[No Contact Made]
    A3c[Notify Sales Rep]
    A3d{Check Contact Made in 3 Days}
    A3e[No Contact Made in 3 Days]
    A3f[Notify Sales Manager]
    A4[Lead Status Update]
    A4a[Send Next Follow-Up]
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

DIGITAL AGENCY

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
    B8[Post-Project Review]

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

GRAPHIC DESIGN

flowchart TD
    E1[Design Request Reception]
    E2[Initial Design Variations]
    E3[Client Feedback]
    E4[Design Finalization]
    E5[Design Submission for Approval]
    E5a{Revisions Needed}
    E5b[Revisions]
    E6[Final Approval]
    E7[Design Delivery]

    E1 --> E2
    E2 --> E3
    E3 --> E4
    E4 --> E5
    E5 --> E5a
    E5a -->|Yes| E5b
    E5a -->|No| E6
    E5b --> E4
    E6 --> E7

RECIEVING

flowchart TD
    C1[Order Placement and Notification]
    C2[Receiving Shipment]
    C3[Inspection and Quality Control]
    C3a{Items Fail Inspection}
    C3b[Return to Supplier/Mark for Rework]
    C4[Inventory Update]
    C5[Storage Allocation]
    C6[Put-Away Process]
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

SCREEN PRINTING

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

    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> D5
    D5 --> D6
    D6 --> D7
    D7 --> D7a
    D7a -->|Yes| D7b
    D7a -->|No| D8
    D7b --> D5
    D8 --> D9

EMBROIDERY

flowchart TD
    F1[Order Reception]
    F2[Material Collection]
    F3[Design Setup]
    F4[Embroidery Process (Start Job Timer)]
    F5[Quality Check]
    F5a{Rework Needed}
    F5b[Rework Process]
    F6[Packaging and Fulfillment]

    F1 --> F2
    F2 --> F3
    F3 --> F4
    F4 --> F5
    F5 --> F5a
    F5a -->|Yes| F5b
    F5a -->|No| F6
    F5b --> F4
    F6 --> F7

HEAT-TRANSFER

flowchart TD
    G1[Order Reception]
    G2[Material Collection]
    G3[Design Setup]
    G4[Vinyl Heat Press Process (Start Job Timer)]
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
    G6 --> G7

FULFILLMENT

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

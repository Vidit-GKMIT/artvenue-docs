## Data Flow Diagram - Level 0
```mermaid 
flowchart TD

%% ==== EXTERNAL ENTITIES ====
A[Artist]
V[Venue Owner]

%% ==== MAIN SYSTEM ====
S([ArtVenue Platform])

%% ==== DATA FLOWS ====
A -->|Sign Up / Login / View Events / Apply for Events| S
V -->|Sign Up / Login / Create Venue / Create Events | S

S -->|Confirmation Emails| V

```


## Data Flow Diagram - Level 1

```mermaid 
flowchart TD

%% ==== EXTERNAL ENTITIES ====
A[Artist] -->|Sign Up / Login| B1[Authentication & Authorization Module]
V[Venue Owner] -->|Sign Up / Login| B1

%% ==== SIGN UP FLOW ====
B1 -->|Sign Up| S1[Enter Details]
S1 --> S5{OTP Valid?}
S5 -->|Check Redis for OTP| R[(Redis - OTP Store)]
S5 -- Yes --> GA[Grant Access]
S5 -- No --> AD[Access Denied]

%% ==== LOGIN FLOW ====
B1 -->|Login| L1[Enter Credentials]
L1 --> L2{Valid Credentials?}
L2 -- Yes --> GA
L2 -- No --> AD

%% ==== MAIN PROCESSES ====
GA -->|Verified Access| B2[Artist]
GA -->|Verified Access| B3[Venue Owner]

B2 -->|Apply for Events| D[(PostgreSQL Database)]
B3 -->|Add / Update Events| D
B3 -->|Create Venue| D

%% ==== OUTPUT FLOWS ====
D -->|Venues / Events List| B2
D -->|Artist Profiles| B3

```
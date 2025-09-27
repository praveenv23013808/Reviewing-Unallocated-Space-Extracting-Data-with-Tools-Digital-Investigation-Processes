# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report

<img width="1919" height="1006" alt="Screenshot 2025-09-25 104859" src="https://github.com/user-attachments/assets/fec8fc41-02a4-445b-a617-94c49ff26b88" />

<img width="1001" height="923" alt="Screenshot 2025-09-25 105706" src="https://github.com/user-attachments/assets/482dda5a-e36b-4d34-a419-81801312fc6b" />

<img width="1109" height="724" alt="Screenshot 2025-09-25 105829" src="https://github.com/user-attachments/assets/8c36504e-b3cf-4f8b-87f5-57bd10c241e5" />

<img width="456" height="350" alt="Screenshot 2025-09-25 110432" src="https://github.com/user-attachments/assets/c0613558-fc92-4e22-a31b-32c47e3fe2f4" />

<img width="1689" height="883" alt="Screenshot 2025-09-25 111722" src="https://github.com/user-attachments/assets/28bd5ec2-ffc7-4522-802f-f7cca5ce696c" />

<img width="1679" height="893" alt="Screenshot 2025-09-25 112238" src="https://github.com/user-attachments/assets/8018d6ca-6e4a-4504-94b9-61ae67efcf50" />

<img width="1910" height="852" alt="Screenshot 2025-09-25 112306" src="https://github.com/user-attachments/assets/87e9eac8-49a2-4e00-b561-6694bc071751" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.


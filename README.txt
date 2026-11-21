=========================================================
UNIVERSITY CLINIC PATIENT CARE SYSTEM
Coursework 2 - Scenario 2 (University Clinic Triage System)
=========================================================

PROJECT OVERVIEW
---------------------------------------------------------
In a busy clinic, treating patients on a first-come, first-served 
basis is dangerous. This C++ application solves that problem by 
combining two core data structures:

1. Max-Heap (Priority Queue): Built from scratch. Ensures the 
   patient with the highest medical severity is always treated first.
2. Hash Table (unordered_map): Allows receptionists to instantly 
   search, update, or delete patient records by ID in O(1) time.


HOW TO COMPILE AND RUN
---------------------------------------------------------
You need a C++17 compiler (like g++ or clang++) installed.

1. Compile the program:
   Open your terminal in this folder and type:
   g++ -std=c++17 main.cpp -o clinic

2. Run the program:
   On Windows: clinic.exe
   On Mac/Linux: ./clinic


PROJECT STRUCTURE
---------------------------------------------------------
* Patient.h    - Defines the Patient struct (ID, Name, Severity).
* TriageHeap.h - The custom implementation of the Max-Heap.
* main.cpp     - Contains the Hash Table, File I/O, Input 
                 Validation, and the main menu loop.
* patients.txt - The text file where patient data is saved 
                 automatically (created when you run the program).


PROGRAM FEATURES (MAIN MENU)
---------------------------------------------------------
1. Register New Patient: 
   Adds a patient. Prompts for ID, Name, and Severity (1-10). 
   Prevents duplicate IDs and invalid severity scores.

2. Treat Most Severe Patient: 
   Extracts the patient with the highest severity from the Max-Heap 
   and removes them from the system.

3. Search Patient by ID: 
   Uses the Hash Table for an instant O(1) lookup.

4. Update Patient Severity: 
   Changes a patient's severity level and safely rebuilds the heap.

5. Generate Alphabetical Report: 
   Sorts and prints all current patients alphabetically by name.

6. Exit & Save: 
   Safely closes the program and saves all records to patients.txt.


BIG-O COMPLEXITY SUMMARY
---------------------------------------------------------
* Max-Heap Insert / Extract : O(log n)
* Hash Table Search          : O(1) average time
* File I/O (Save/Load)       : O(n)
* Report Sorting             : O(n log n)

=========================================================
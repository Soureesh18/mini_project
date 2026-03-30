Integrated Smart Healthcare System – Report
1. Introduction

The Integrated Smart Healthcare System is a C-based console application designed to assist users in basic health assessment and emergency handling. The program provides two major functionalities:

Health Analysis Module
Emergency Response Module

It aims to simulate a simplified healthcare support system that collects patient data, evaluates symptoms, calculates risk levels, and provides basic medical guidance.

2. Objectives
To register and manage patient information
To analyze symptoms and determine health risk
To provide preliminary medical advice
To assist in emergency situations with quick guidance
To demonstrate file handling and decision-making in C
3. System Modules
3.1 Health Analysis Module

This module performs patient registration and symptom-based health evaluation.

a) Patient Registration
New patients can enter:
Name
Age
Blood Group
City
Data is stored in a file named patients.txt with the current date.
b) Existing Patient Handling
Displays previously stored patient records
Allows user to re-enter name and age for analysis
c) Symptom Input

The system supports multiple symptoms:

Fever
Cough and Cold
Headache
Stomach Pain
Skin Problems
Eye Irritation
Chest Pain
Joint Pain
Breathing Difficulty
Tooth Pain

Each symptom is assigned a severity level:

1: Mild
2: Moderate
3: Severe
4: Critical
d) Risk Calculation
Risk is calculated based on severity
Critical symptoms like Chest Pain and Breathing Difficulty carry double weight
Total risk determines the health status:
Low (≤3)
Moderate (≤7)
High (>7)
e) Health Report

The system generates a report including:

Date
Patient details
Risk score and level
Medical advice:
Low: Rest and monitor
Moderate: Visit doctor soon
High: Immediate consultation
f) Case-wise Suggestions

For each symptom, the system provides:

Condition name
Suggested medicine
Recommended specialist
Room number
Precautions
3.2 Emergency Response Module

This module helps in handling urgent situations.

a) Emergency Types
Accident
Fire
Cardiac Arrest
General Emergency
Seizures
b) Severity Levels
Range: 1 to 5
c) Output
Displays emergency type
Provides immediate instructions
Assigns priority:
Low
Medium
High
Critical
d) Final Step
Confirms that emergency services have been dispatched
4. Key Features
User-friendly menu-driven interface
File handling for patient record storage
Multi-symptom input support
Risk-based health evaluation
Emergency guidance system
Structured medical suggestions
5. Technologies Used
Programming Language: C
Libraries:
stdio.h (input/output)
time.h (date handling)
6. Advantages
Simple and easy to use
Helps in basic health awareness
Demonstrates core C programming concepts
Provides quick emergency instructions
7. Limitations
Not connected to real medical databases
No validation for incorrect inputs beyond severity
Limited symptom coverage
Suggestions are generic, not personalized
No real emergency dispatch system
8. Conclusion

The Integrated Smart Healthcare System is a basic simulation of a healthcare assistant. It effectively demonstrates how programming can be used to build systems for health monitoring and emergency support. While it is not a substitute for professional medical services, it serves as a strong educational project showcasing file handling, conditional logic, and user interaction in C.
9. Test cases
Test Case 1: New Patient with Low Risk

Input:

Choice: 1
Existing Patient: n
Name: Rahul Sharma
Age: 25
Blood Group: B+
City: Mumbai
Symptom: Fever (1)
Severity: 1
Add another symptom: n

Expected Output:

Patient registered successfully
Risk = 1
Risk Level: LOW
Advice: Monitor symptoms and rest
Suggestion:
Condition: Fever
Medicine: Paracetamol
Doctor: General Physician
Test Case 2: New Patient with Moderate Risk (Multiple Symptoms)

Input:

Choice: 1
Existing Patient: n
Name: Priya Mehta
Age: 30
Blood Group: O+
City: Pune
Symptom 1: Cough and Cold (2) → Severity: 2
Add another: y
Symptom 2: Headache (3) → Severity: 2
Add another: n

Expected Output:

Risk = 4
Risk Level: MODERATE
Advice: Visit doctor soon
Suggestions for both symptoms displayed correctly
Test Case 3: High Risk Case (Critical Symptoms)

Input:

Choice: 1
Existing Patient: n
Name: Amit Verma
Age: 55
Blood Group: A+
City: Delhi
Symptom: Chest Pain (7)
Severity: 4
Add another: n

Expected Output:

Risk = 8 (double weight applied)
Risk Level: HIGH
Advice: Visit doctor immediately
Suggestion:
Condition: Chest Pain
Doctor: Cardiologist
Emergency warning displayed
Test Case 4: Existing Patient Record Retrieval

Precondition: patients.txt contains records

Input:

Choice: 1
Existing Patient: y
(System displays stored records)
Name: Rahul Sharma
Age: 25
Symptom: Tooth Pain (10)
Severity: 2
Add another: n

Expected Output:

Existing records displayed
Risk = 2
Risk Level: LOW
Advice: Monitor symptoms and rest
Suggestion:
Condition: Tooth Pain
Doctor: Dentist
Test Case 5: Invalid Severity Handling

Input:

Choice: 1
Existing Patient: n
Name: Sneha Patil
Age: 28
Blood Group: AB+
City: Nashik
Symptom: Headache (3)
Severity: 5 (invalid)
Re-enter Severity: 2
Add another: n

Expected Output:

Message: "Invalid severity."
Prompts again for correct input
Risk calculated correctly after valid input
Risk Level: LOW or MODERATE (based on valid entry)



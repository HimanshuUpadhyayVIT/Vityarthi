# Symptom Checker User Guide

## Overview
This Python project implements a simple symptom checker that identifies a possible disease based on the symptoms entered by the user. It matches user-provided symptoms to predefined rules associating symptoms with diseases.

## Features
- Accepts multiple symptoms as input, separated by commas.
- Converts and processes symptoms for case-insensitive matching.
- Uses a rule-based approach to match symptoms to the diseases: Influenza (Flu), Dengue, Heart Disease, Migraine, and Diabetes.
- Returns the most likely disease based on the symptoms or prompts to consult a doctor if no match is found.

## Installation

### Prerequisites
- Python 3.x installed on your system
- Download from: https://www.python.org/downloads/

### Steps
1. Save the symptom checker script (e.g., `symptom_checker.py`) to a preferred directory on your computer.
2. No additional dependencies are required as the script uses only built-in Python libraries.
3. Verify Python installation by running: `python --version`

## Usage

### Running the Program
1. Open a terminal or command prompt
2. Navigate to the directory where the script is saved using:
   ```
   cd path/to/your/directory
   ```
3. Run the script with the command:
   ```
   python symptom_checker.py
   ```

### Input Format
- When prompted, enter your symptoms separated by commas
- Example: `fever, cough, fatigue`
- Symptoms are case-insensitive (e.g., "Fever" and "fever" are treated the same)

### Output
- The program will display the possible disease based on matched symptoms
- If no disease matches all required symptoms, it will prompt you to consult a doctor

## Code Structure

### Main Functions

#### `identify_disease(symptoms)`
- **Purpose**: Analyzes symptoms and identifies possible diseases
- **Parameters**: `symptoms` (list of strings)
- **Returns**: String containing the disease name or message to consult a doctor
- **Process**:
  - Normalizes symptoms (strips whitespace, converts to lowercase)
  - Checks against predefined symptom-disease rules
  - Returns disease if all required symptoms match

#### `main()`
- **Purpose**: Entry point that handles user interaction
- **Process**:
  - Displays title
  - Prompts user for symptoms
  - Splits input by commas
  - Calls `identify_disease()` and displays result

### Disease Rules
The program recognizes the following diseases:
- **Influenza (Flu)**: fever, cough, fatigue
- **Dengue**: fever, rash, joint pain
- **Heart Disease**: chest pain, shortness of breath
- **Migraine**: headache, nausea, sensitivity to light
- **Diabetes**: thirst, frequent urination, weight loss

## Examples

### Example 1: Flu Detection
```
=== Symptom Checker ===
Enter symptoms separated by commas: fever, cough, fatigue
Possible Disease: Influenza (Flu)
```

### Example 2: Dengue Detection
```
=== Symptom Checker ===
Enter symptoms separated by commas: fever, rash, joint pain
Possible Disease: Dengue
```

### Example 3: Disease Not Identified
```
=== Symptom Checker ===
Enter symptoms separated by commas: sore throat, runny nose
Disease not identified. Please consult a doctor.
```

## Troubleshooting

### Issue: "python: command not found"
- **Solution**: Python is not installed or not in your system PATH
- **Fix**: Install Python from https://www.python.org/downloads/ and ensure it's added to PATH during installation

### Issue: Script doesn't run
- **Solution**: Ensure you're in the correct directory
- **Fix**: Use `cd` command to navigate to the script location

### Issue: Symptoms not recognized
- **Solution**: Symptom spelling or format might be incorrect
- **Fix**: Refer to the Disease Rules section for exact symptom names
- **Note**: All symptoms must be present for a disease to be identified

## Limitations
- This program uses basic rule-based matching and requires ALL symptoms to be present
- It recognizes only 5 diseases with predefined symptom sets
- Partial matches are not supported

## Future Enhancements
- Add more diseases and symptom combinations
- Implement weighted symptom matching (partial matches)
- Add symptom severity levels
- Integrate with medical databases for more accurate diagnosis
- Create a GUI interface for better user experience

## Important Disclaimer
⚠️ **MEDICAL DISCLAIMER**

This program is for **educational and demonstration purposes only**. It should NOT be used for:
- Making actual medical diagnoses
- Making treatment decisions
- Replacing professional medical advice
- Self-diagnosis of medical conditions

**Always consult a qualified healthcare professional** for:
- Accurate medical diagnosis
- Treatment recommendations
- Medical emergencies

If you are experiencing health concerns, please contact:
- Your primary care physician
- A local hospital or urgent care facility
- Emergency services (911 in USA, 112 in EU, etc.)

## Author Information
This symptom checker project was created for educational purposes to demonstrate Python programming concepts including:
- Function definitions
- Conditional logic
- List comprehensions
- User input handling
- String manipulation

## License
This project is provided as-is for educational use.

## Contact & Support
For questions or suggestions about the code, refer to Python documentation at https://docs.python.org/


def identify_disease(symptoms):

    symptoms = [s.strip().lower() for s in symptoms]


    rules = {
        "Influenza (Flu)": ["fever", "cough", "fatigue"],
        "Dengue": ["fever", "rash", "joint pain"],
        "Heart Disease": ["chest pain", "shortness of breath"],
        "Migraine": ["headache", "nausea", "sensitivity to light"],
        "Diabetes": ["thirst", "frequent urination", "weight loss"]
    }


    for disease, required_symptoms in rules.items():
        if all(symptom in symptoms for symptom in required_symptoms):
            return f"Possible Disease: {disease}"

    return "Disease not identified. Please consult a doctor."

def main():
    print("=== Symptom Checker ===")
    user_input = input("Enter symptoms separated by commas: ")
    symptoms = user_input.split(",")
    result = identify_disease(symptoms)
    print(result)

if __name__ == "__main__":
    main()




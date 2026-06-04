---
# File: docs/standards/coding.md
title: "Coding Standards"
nav_order: 45
---

# Coding Standards

This document defines the coding standards for all Redbird Robotics projects.  
Following these guidelines ensures our code is **consistent, readable, and maintainable** across teams.

---

## 1. General Guidelines

- Always write **clear, modular, and well-documented code**.  
- Use **English** for variable names, comments, and documentation.  
- Keep files and folders **lowercase-with-dashes** (e.g., `motor-driver/`, `sensor-utils/`).  
- Every project must include a `README.md` explaining:  
  - Purpose of the code  
  - How to build/run it  
  - Dependencies (libraries, hardware, etc.)

---

## 2. Languages & File Types

We primarily use:

- **C/C++** → Embedded firmware, Arduino  
- **Python** (rare)→ Tools, scripts, automation  
- **MATLAB** (rare) → Data analysis or simulations  
- **Other languages** only if documented and approved by the team lead

Each file type should follow the style rules below.

---

## 3. C / C++ Standards
 
- **Braces**: Opening brace on the same line
  ```c
  if (condition) {
      doSomething();
  } else {
      doOtherThing();
  }
  ```
- **Variable names**: lowerCamelCase for local variables, UpperCamelCase for classes/structs.
- **Constants & macros**: ALL_CAPS_WITH_UNDERSCORES
- **Functions**: lowerCamelCase(), keep under ~40 lines.
- **Comments**: Use // for single-line, /** ... */ for function documentation.
- Example:
```c
// Calculates motor speed based on encoder feedback
int calculateMotorSpeed(int encoderTicks, float dt) {
    return (int)(encoderTicks / dt);
}
```

---

## 4. Documentation & Comments
- Every function should have a short docstring or comment explaining what it does.
- Use inline comments only when the logic isn’t obvious.
- At the top of each file, include:
```c
/*
 * File: motor_driver.c
 * Author: Alice Smith
 * Description: Controls DC motors using PWM and encoder feedback.
 */
 ```

---

## 5. Git & Repository Practices
- One feature per branch → branch names like feature/motor-driver or bugfix/sensor-timeout.
- Commit messages should be short but descriptive:
    - ✅ Added PID controller for arm joints
    - ❌ fixed stuff
- Never commit large binaries (e.g., CAD exports) in code repos.
- Use .gitignore to exclude build files, logs, and IDE settings.

---

## 6. Testing & Debugging
- Use serial printouts (Serial.println) or logging functions with clear, consistent formatting.
- Remove debug code before merging into main.

---

## 7. Safety & Reliability
- Always check input ranges and add fail-safes in embedded code.
- Handle hardware errors gracefully (timeouts, disconnects, bad sensor data).
- Avoid “magic numbers” — define constants instead.

---

## 8. Minimum Expectations
- Code compiles without errors or warnings.
- Follows formatting and naming rules above.
- Has meaningful commit messages.
- Includes at least basic documentation in the repo.

---

By following these standards, we ensure that every project is approachable for new members and maintainable for future teams.

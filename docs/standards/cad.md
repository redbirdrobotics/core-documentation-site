---
# File: docs/standards/cad.md
title: "CAD Standards"
nav_category: "Standards"
nav_order: 2
---

# CAD Standards

This document defines the CAD standards for all Redbird Robotics projects. Following these guidelines ensures **consistency, maintainability, and smooth collaboration** across all teams.

---

## 1. File Naming Conventions

- **Lowercase with dashes** for all files and folders:  
  - Part files: `claw.sldprt`, `baseplate.sldprt`  
  - Assembly files: `arm.sldasm`, `robot-chassis.sldasm`  
  - Subassemblies: `gripper-subasm.sldasm`  

- **Include version numbers only if necessary**, otherwise rely on Git for versioning:  
  - Example: `claw.sldprt` → Git keeps history; no `claw_v1.sldprt`.

- Avoid spaces, special characters, or non-English letters.

---

## 2. Folder Structure

Recommended project repo structure:
- `parts/` → individual components  
- `subassemblies/` → reusable subassemblies  
- `assemblies/` → top-level assemblies  

> Keeps team members from stepping on each other’s work and simplifies Git merges.

---

## 3. Assembly & Subassembly Workflow

1. **Parts first:** each team member edits **parts individually** or subassemblies.  
2. **Assembly updates:**  
   - Only touch the top-level assembly if necessary.  
   - Pull the latest `main` before editing.  
   - Rebase your branch if others have updated the assembly.  

3. **Subassemblies are encouraged** to reduce merge conflicts:  
   - Each subassembly should represent a logically independent section of the robot (e.g., `gripper-subasm`, `chassis-subasm`).  
   - Subassemblies should be self-contained with clear references to parts.

---

## 4. References & External Files

- All parts should be referenced **externally** (not copied inside assemblies) to avoid duplication.  
- Avoid using broken or absolute paths — use **relative references** inside the repo.  
- Ensure all referenced files are committed in the repo.

---

## 5. Mates & Constraints

- Keep mates **minimal and intuitive**.  
    - If you want to go the extra mile, **name or sort** your mates.
- Avoid complex constraints that make rebuilding or merging assemblies difficult.  
- Only adjust mates in assemblies/subassemblies you “own” in your branch.

---

## 6. Version Control with Git

- **One part or subassembly per branch** is ideal.  
- Commit changes frequently.  
- Avoid committing generated files (STLs, PDFs) unless required for documentation.  
- Use GitHub Desktop for beginners; Git Bash for advanced workflows if needed.  

---

## 7. Documentation & Metadata

- Include a **design notes file** (`design-notes.md`) in the assembly folder if the assembly is complex.  
- Document:  
  - Intended use of parts/subassemblies  
  - Important mates or constraints  
  - Revision notes if applicable  

- Include screenshots if needed for clarity.

---

## 8. Cleanliness & Best Practices

- Remove unused sketches, features, or suppressed parts before committing.   
- Use consistent material/appearance settings to avoid confusion.

---

## 9. Summary Rules

- `lowercase-with-dashes.sldprt` and `.sldasm`  
- One part per branch; pull latest before assembly edits  
- Use subassemblies to minimize conflicts  
- External references only; no local copies  
- Commit often, document as you go  

> Following these standards will make collaboration across multiple students seamless, reduce Git merge headaches, and keep your projects professional and maintainable.

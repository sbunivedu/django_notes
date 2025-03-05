### **Introduction to Semantic Versioning and Dependency Management**

In software development, managing dependencies is crucial to ensure stability and compatibility across projects. **Semantic Versioning (SemVer)** is a standardized way of versioning software to communicate changes clearly.

---

### **Semantic Versioning (SemVer) Basics**
A version number follows the format:
$$\text{MAJOR}.\text{MINOR}.\text{PATCH}$$
For example: `1.4.2`

1. **MAJOR (1)** – Incremented when there are incompatible API changes.
2. **MINOR (4)** – Incremented when new features are added in a backward-compatible way.
3. **PATCH (2)** – Incremented for backward-compatible bug fixes.

**Example:**
- `1.0.0 → 1.1.0` (New feature added, backward-compatible)
- `1.1.0 → 1.1.1` (Bug fix, no breaking changes)
- `1.1.1 → 2.0.0` (Breaking changes introduced)

---

### **Dependency Management with Semantic Versioning**
Dependency management ensures that a project consistently uses compatible versions of libraries or frameworks.

#### **Example in Python (Django Project)**
Consider a Django project with `requirements.txt`:
```txt
Django>=3.2,<4.0
requests~=2.26
```
- `Django>=3.2,<4.0`: Allows any Django version from `3.2.0` up to (but not including) `4.0.0`.
- `requests~=2.26`: Allows updates within the same minor version (e.g., `2.26.1`, `2.27.0` but not `3.0.0`).

This prevents unexpected breaking changes while allowing updates that fix bugs or add features.

#### **Example in JavaScript (package.json)**
```json
"dependencies": {
  "express": "^4.17.1",
  "lodash": "~4.17.20"
}
```
- `"express": "^4.17.1"` → Accepts updates within `4.x.x`, avoiding `5.0.0` which may have breaking changes.
- `"lodash": "~4.17.20"` → Accepts updates within `4.17.x`, avoiding `4.18.0`.

---

### **Why Semantic Versioning Matters?**
- **Prevents breaking updates** (e.g., upgrading Django from `3.2` to `4.0` could break your app).
- **Allows automatic updates for minor improvements and security patches**.
- **Improves collaboration by setting clear expectations for dependencies**.

### **Exercise**
1. **Check the installed dependencies** in a Django project:
   ```sh
   pip freeze
   ```
2. **Manually upgrade a dependency** (e.g., Django) and observe any breaking changes:
   ```sh
   pip install --upgrade django
   ```
3. **Use `pipenv` or `venv`** to manage dependencies and virtual environments effectively.

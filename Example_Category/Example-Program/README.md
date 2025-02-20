# **Example Program (Python Boilerplate)**

## **📌 Overview**
This script serves as a **general-purpose Python boilerplate**, providing a **flexible foundation** for building automation tools, file processors, and system utilities. It is **lightweight**, allows **easy modification**, and includes **optional command-line arguments** to extend functionality.

This template is designed to be **drop-in ready**, allowing you to:
- **Add your own functions** without modifying the core structure.
- **Optionally use argparse** without breaking simple scripts.
- **Track execution time** and provide user feedback.

---

## **⚙️ Features**
✅ **Preconfigured script structure** with modular functions.  
✅ **Command-line support** _(if `argparse` is available)_.  
✅ **Directory scanning** to list files inside a folder.  
✅ **Execution timing** for performance tracking.  
✅ **Easily expandable** with custom functions.  

---

## **🚀 Usage**
### **1️⃣ Running the script normally**
To execute the boilerplate script without arguments:
```bash
python example-program.py
```

### **2️⃣ Running with optional directory scanning**
To scan a folder and list its contents:
```bash
python example-program.py /path/to/directory
```

### **3️⃣ Enabling verbose output**
For additional details during execution:
```bash
python example-program.py --verbose
```

### **4️⃣ Display script version**
To check the version of the script:
```bash
python example-program.py --version
```

---

## **📂 What This Script Does**
### **1️⃣ Example Function (`example_task()`)**
📌 **A placeholder function to demonstrate execution flow.**  
- Prints a basic message.
- Can be replaced with custom functionality.

### **2️⃣ List Directory Contents (`list_directory_contents()`)**
📌 **Scans a folder and displays file names.**  
- Takes an input **directory path** _(defaults to `./` if none is provided)_.  
- Checks if the directory is **valid** before scanning.  
- Lists **all files and folders** in that location.  
- Prints a **confirmation message** when done.

### **3️⃣ Command-Line Arguments (`parse_arguments()`)**
📌 **Optional arguments for enhanced functionality.**  
- `--verbose` → Enables detailed output.  
- `--version` → Displays script version and exits.  
- `<directory>` _(Positional)_ → Scans a specific folder.

### **4️⃣ Execution Timing**
📌 **Measures script runtime from start to finish.**  
- Begins timing before script execution.  
- Ends timing and displays elapsed time.

---

## **🛠 Installation**
This script does not require external dependencies by default. However, if `argparse` is missing and needed, install it using:
```bash
pip install argparse
```

---

## **📜 License**
This project is licensed under the **MIT License**. See [LICENSE](../../LICENSE) for details.

---

## **📌 Why Use This Template?**
🔹 **Easy-to-modify** for custom automation tasks.  
🔹 **Handles command-line input gracefully** _(without breaking simple scripts)_.  
🔹 **Provides a clear structure** for maintainability.  
🔹 **Includes built-in error handling** for common scenarios.  

This boilerplate is ideal for **quick prototyping, automation scripts, and command-line tools**. 🚀
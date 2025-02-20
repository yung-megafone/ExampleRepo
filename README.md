# **Python Boilerplate Repository**

## **📌 Overview**
This repository serves as a **template for structured Python projects**, ensuring maintainability, scalability, and ease of documentation. It follows a **uniform folder structure** with **boilerplate code**, detailed **pseudocode**, and proper documentation for each program.

This structure allows for **consistent development**, making it easier to add new projects while ensuring they follow the same best practices.

---

## **⚡ Features**
✅ **Structured Project Hierarchy** → Every program is neatly categorized.  
✅ **Boilerplate Python Script** → Ready-to-use starter code for Python projects.  
✅ **Standardized Pseudocode Documentation** → High-Level (`T1`) & Structured (`T2`) pseudocode included.  
✅ **Modular & Expandable** → Easily add new projects with predefined templates.  
✅ **Supports Command-Line Arguments (Optional)** → Argparse is used when needed, without breaking simple scripts.  

---

## **📂 Project Structure**
```
📂 ExampleRepo/
├── 📂 Example_Category/
│   ├── 📂 Example-Program/
│   │   ├── 📄 example-program.py     # Boilerplate Python script
│   │   ├── 📄 README.md              # Program documentation
│   │   ├── 📄 T1_HighLevel_PC.md     # High-Level Pseudocode
│   │   └── 📄 T2_Structured_PC.md    # Structured Pseudocode
├── 📄 LICENSE
├── 📄 README.md                      # Boilerplate repository documentation
└── 📄 requirements.txt               # Dependencies
```

Each **program** is placed in a **category** and follows the **same structure**, making it easier to maintain and expand.

---

## **🚀 How to Use**
### **🔹 1. Clone the Repository**
```bash
git clone https://github.com/yung-megafone/python-boilerplate.git
cd python-boilerplate
```

### **🔹 2. Create a New Program**
To add a new program, follow this structure:
```bash
mkdir -p Example_Category/New-Program
cp -r Example_Category/Example-Program Example_Category/New-Program
```
Then, update the `README.md`, pseudocode files, and script to match your new program.

### **🔹 3. Run the Boilerplate Python Script**
```bash
python example-program.py
```
Or run with arguments (if applicable):
```bash
python example-program.py --directory /path/to/folder --verbose
```

### **🔹 4. Check Script Version**
```bash
python example-program.py --version
```

---

## **📜 Pseudocode Documentation**
Each program contains **two levels of pseudocode**:

### **📌 T1: High-Level Pseudocode (`T1_HighLevel_PC.md`)**
A broad **overview** of what the program does, without implementation details.
```
START

1. Get user input (directory path, optional arguments).
2. Process data:
   a. Scan directories & files.
   b. Sort and filter data.
   c. Generate output.
3. Display results or save them.
4. Handle errors and exit.

END
```

### **📌 T2: Structured Pseudocode (`T2_Structured_PC.md`)**
A **detailed, step-by-step breakdown** closely matching the actual implementation.
```
START PROGRAM

IMPORT necessary libraries
CHECK if argparse is available
DEFINE script metadata (Author, Version, License)
DEFINE CONSTANTS (VERSION, DEFAULT_DIRECTORY)

FUNCTION example_task():
    PRINT "Running example task..."
END FUNCTION

FUNCTION list_directory_contents(directory):
    PRINT "Scanning directory:", directory
    IF directory does not exist:
        PRINT "Error: Invalid directory."
        RETURN
    END IF
    FOR each file in directory:
        PRINT file name
    END FOR
    PRINT "Scan complete."
END FUNCTION

FUNCTION parse_arguments():
    IF argparse is available:
        CREATE argument parser
        ADD arguments (directory, verbose, version)
        RETURN parsed arguments
    ELSE:
        RETURN None
    END IF
END FUNCTION

FUNCTION main():
    PARSE arguments (if available)
    IF version flag is used:
        PRINT script version and exit
    START execution timer
    CALL example_task()
    IF directory argument is provided:
        CALL list_directory_contents(directory)
    STOP execution timer and print execution time
END FUNCTION

IF script is executed directly:
    CALL main()

END PROGRAM
```

---

## **📂 Example Boilerplate Code (`example-program.py`)**
The `example-program.py` script provides a **clean, reusable template** for any Python project.

```python
"""
Example Python Boilerplate
--------------------------
Author: yung-megafone
Date: 2025-02-19
License: MIT License

Description:
This script serves as a generic Python program template. It provides
a structured entry point, optional argparse support, and modular functions.
"""

import os
import sys
import time

# Attempt to import argparse, but allow the script to run without it
try:
    import argparse
    ARGPARSE_AVAILABLE = True
except ImportError:
    ARGPARSE_AVAILABLE = False

# Constants
VERSION = "1.0.0"
DEFAULT_DIRECTORY = "./"


def example_task():
    """Placeholder function for actual functionality."""
    print("🚀 Running example task...")


def list_directory_contents(directory):
    """Lists contents of a directory."""
    print(f"🔍 Scanning directory: {directory}")
    if not os.path.isdir(directory):
        print("❌ Error: Invalid directory.")
        return

    for file in os.listdir(directory):
        print(f"📄 {file}")
    print("✅ Directory scan complete.")


def parse_arguments():
    """Parses command-line arguments (if argparse is available)."""
    if not ARGPARSE_AVAILABLE:
        return None

    parser = argparse.ArgumentParser(description="Example Python Boilerplate Script")
    parser.add_argument("directory", nargs="?", default=DEFAULT_DIRECTORY, help="Directory to scan")
    parser.add_argument("--verbose", action="store_true", help="Enable verbose mode")
    parser.add_argument("--version", action="store_true", help="Show script version")

    return parser.parse_args()


def main():
    """Main execution function."""
    args = parse_arguments() if ARGPARSE_AVAILABLE else None

    if args and args.version:
        print(f"📌 Script Version: {VERSION}")
        sys.exit()

    start_time = time.time()
    print("🎯 Running main script...")

    example_task()

    if args and args.directory:
        list_directory_contents(args.directory)

    elapsed_time = time.time() - start_time
    print(f"✅ Script completed in {elapsed_time:.2f} seconds.")


if __name__ == "__main__":
    main()
```

---

## **📜 License**
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## **💡 Future Enhancements**
🔹 Add **logging support** instead of print statements.  
🔹 Allow **config file support** for script settings.  
🔹 Create **a CLI interface** for easier customization.  

---

This **boilerplate repository** ensures that every Python project starts off **clean, modular, and scalable**. 🚀  
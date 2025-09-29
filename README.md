# s2html

s2html is a lightweight C-based tool that converts C source code into HTML documentation. It parses source files, extracts functions, comments, and generates a readable HTML page with syntax highlighting — perfect for creating code docs quickly.

🚀 Features

* Syntax Highlighting: Highlights C keywords, functions, and comments.

* Function Prototypes Extraction: Lists all functions for easy navigation.

* Comment Integration: Includes your inline comments in the HTML output.

* Customizable Templates: Change CSS or HTML template for personal or project styling.

* Lightweight & Fast: Pure C implementation with no heavy dependencies.

## Project Structure
s2html/
├── README.md              # Documentation
├── s2html_main.c          # Program entry point
├── s2html_conv.c          # Core conversion logic
├── s2html_conv.h          # Header file for conversion functions
├── s2html_event.c         # Event handling during parsing
├── s2html_event.h         # Header for event functions
├── test.c                 # Sample source file for testing
├── styles.css             # Styling for generated HTML
├── tags/                  # Templates for HTML output
└── output/                # Directory for generated HTML files

## Compilation & Execution
Compile:
gcc *.c -o s2html

Run:
./s2html test.c


Output: test.c.html will appear in the output/ folder.

## Usage

Prepare your C source file (.c) with functions and comments.

Run s2html with the file name as input.

Open the generated HTML in a browser:

$ ./s2html test.c
HTML file created: output/test.c.html


Browse the HTML — functions are highlighted, comments included, clean and readable.

🔹 Example

Input test.c:

#include <stdio.h>

// Function to add two numbers
int add(int a, int b){
    return a + b;
}

int main(){
    printf("%d\n", add(3, 4));
    return 0;
}


Generated HTML (test.c.html) highlights:

Keywords: int, return, printf

Comments included as notes

Function prototype listed at top

📊 Program Flow
+-----------------+
| Start           |
+-----------------+
        |
        v
+-----------------+
| Read Source File|
+-----------------+
        |
        v
+-----------------+
| Parse Functions |
+-----------------+
        |
        v
+-----------------+
| Parse Comments  |
+-----------------+
        |
        v
+-----------------+
| Generate HTML   |
+-----------------+
        |
        v
+-----------------+
| Save HTML       |
+-----------------+
        |
        v
+-----------------+
| End             |
+-----------------+

🎨 Customization Tips

1. Change Styles: Modify styles.css to adjust colors, fonts, or layout.

2. Template Adjustments: Edit files in tags/ to change HTML structure (header, footer, section templates).

3. Batch Conversion: Extend the main program to parse multiple .c files at once.

4. Advanced Highlighting: Add regex for macros, constants, or special syntax for bigger projects.

📚 Concepts Behind

1. Converts source code → HTML for readability.

2. Supports documentation generation for projects with multiple source files.

3. Inspired by classic code documentation generators but lightweight in pure C.

 
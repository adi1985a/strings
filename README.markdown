# ✍️✂️ StringMaster Pro: Advanced Text Toolkit 🛠️
_A comprehensive C++ console application for a wide array of string manipulation tasks, featuring a colorful UI, file operations, and robust error handling._

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![C++](https://img.shields.io/badge/Language-C%2B%2B-blue.svg)](https://isocpp.org/)
[![Platform: Windows](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)](https://www.microsoft.com/windows)

## 📋 Table of Contents
1.  [Project Description](#-project-description)
2.  [Key Features](#-key-features)
3.  [Screenshots](#-screenshots)
4.  [System Requirements](#-system-requirements)
5.  [Installation and Running](#️-installation-and-running)
6.  [How to Use](#️-how-to-use)
7.  [Technical Details & Program Logic](#-technical-details--program-logic)
8.  [Contributing](#-contributing)
9.  [Author](#️-author)
10. [License](#-license)

## 📝 Project Description

**StringMaster Pro** is a versatile C++ console application designed to be your go-to tool for a multitude of string and text manipulation tasks. It empowers users to perform operations such as finding and replacing text, removing sections, reversing strings, concatenating multiple texts, and converting case. Unique features include a gender guesser based on names and an ASCII value converter. The program supports saving your work to and loading from files, ensuring your manipulated text is preserved. With its colorful, menu-driven interface and built-in error handling, StringMaster Pro offers a robust and user-friendly experience for all your text processing needs.

![Demo GIF](screenshots/1.gif)

## ✨ Key Features

*   ✍️ **Text Editing & Manipulation**:
    *   **Replace Text**: Substitute a specific part of the text with another string.
    *   **Find Text**: Locate occurrences of a specific substring within the main text.
    *   **Remove Text**: Delete a specified portion of the text.
    *   **Reverse Text**: Invert the order of characters in the string.
    *   **Concatenate Texts**: Join two or more strings together.
    *   **Insert Text**: Add a new string at a specified position within the existing text.
    *   **Copy Text**: Extract and copy a portion of the text.
*   🧑‍🔬 **Analysis & Conversion**:
    *   **Guess Gender by Name**: Attempts to infer gender based on common Polish first names (or a predefined list).
    *   **ASCII Converter**: Display the ASCII decimal values for each character in a string.
    *   **Case Conversion**: Convert the entire text to **UPPERCASE** or **lowercase**.
*   💾 **File Operations**:
    *   **Save to File**: Save the currently manipulated text to a user-specified file.
    *   **Load from File**: Load text from an existing file into the application for manipulation.
*   ❓ **Detailed Help**: An in-app help guide explaining the various functionalities.
*   🌈 **Colorful Console Interface**: Enhanced user experience with colored text for menus, prompts, and output (Windows-specific, via `Utils.h`).
*   ✔️ **Robust Error Handling**: Manages invalid inputs and operational errors gracefully.

## 🖼️ Screenshots

_Screenshots showcasing the main menu, various string operation dialogues, file operations, the help screen, and other key interface elements._

<p align="center">
  <img src="screenshots\Image1.jpg" width="300"/>
  <img src="screenshots\Image2.jpg" width="300"/>
  <img src="screenshots\Image3.jpg" width="300"/>
  <img src="screenshots\Image4.jpg" width="300"/>
  <img src="screenshots\Image5.jpg" width="300"/>
  <img src="screenshots\Image6.jpg" width="300"/>
  <img src="screenshots\Image7.jpg" width="300"/>
  <img src="screenshots\Image8.jpg" width="300"/>
  <img src="screenshots\Image9.jpg" width="300"/>
  <img src="screenshots\Image10.jpg" width="300"/>
  <img src="screenshots\Image11.jpg" width="300"/>
  <img src="screenshots\Image12.jpg" width="300"/>
  <img src="screenshots\Image13.jpg" width="300"/>
</p>


## ⚙️ System Requirements

*   **Operating System**: Windows is recommended for full color functionality, as console utilities (likely via `Utils.h`) often use Windows-specific API calls.
*   **C++ Compiler**: Any modern C++ compiler that supports C++11 or newer (e.g., g++, MinGW, Clang, MSVC).
*   📄 **`Nowy.h` and `Utils.h` Header Files (User-Provided)**: This project **critically requires** two header files, `Nowy.h` and `Utils.h`. **These files are not included in the repository and must be created by the user.**
    *   `Nowy.h` is expected to define a custom string class (e.g., `String1`) with methods for string operations.
    *   `Utils.h` should provide general utility functions for console manipulation.
    See the "Installation and Running" section for more details.

## 🛠️ Installation and Running

1.  **Clone the Repository**:
    ```bash
    git clone <repository-url>
    ```
    (Replace `<repository-url>` with the actual URL of your repository)

2.  **Navigate to the Project Directory**:
    ```bash
    cd <repository-directory>
    ```
    (Replace `<repository-directory>` with the name of the cloned folder)

3.  **Create `Nowy.h` and `Utils.h`**:
    Before compiling, you **must** create these two header files in the project's root directory.

4.  **Compile the Program**:
    Open a terminal (like Command Prompt or PowerShell) in the project directory.
    **Example using g++ (MinGW):**
    ```bash
    g++ main.cpp Nowy.cpp Utils.cpp -o string_operations.exe -static-libgcc -static-libstdc++
    ```
    *(This assumes you have `Nowy.cpp` and `Utils.cpp` for implementations. Adjust if your structure differs).*

5.  **Run the Application**:
    After successful compilation, execute the generated program:
    ```bash
    ./string_operations.exe
    ```
    or simply in CMD:
    ```bash
    string_operations.exe
    ```

## ▶️ How to Use

Upon launching **StringMaster Pro**, you will be greeted with a main menu offering a range of operations. Enter the number corresponding to your desired action:

1.  **Replace text**: Find and replace a substring.
2.  **Find text**: Search for a substring.
3.  **Remove text**: Delete a portion of the string.
4.  **Guess gender by name**: Enter a (typically Polish) first name to get a gender guess.
5.  **Reverse text**: Reverse the current string.
6.  **Concatenate texts**: Append another string to the current one.
7.  **Insert text**: Insert a string at a specific position.
8.  **Copy text**: Copy a substring to (presumably) a clipboard or another variable.
9.  **ASCII converter**: Display ASCII values of characters.
10. **To uppercase**: Convert string to uppercase.
11. **To lowercase**: Convert string to lowercase.
12. **Save to file**: Save the current string to a file.
13. **Load from file**: Load a string from a file.
14. **Show help**: Display detailed instructions or information about the commands.
15. **Exit**: Terminate the application.

*The program will guide you through prompts for necessary inputs for each operation.*

## 💡 Technical Details & Program Logic

*   **`String1` Class (in `Nowy.h`)**: This custom class is central to the program, encapsulating a string and providing methods for all the listed operations (e.g., `zastap_fraze()`, `znajdz()`, `odwroc_kolejnosc()`). It likely uses `std::string` internally.
*   **`Utils.h`**: This user-provided header contains general-purpose utility functions like `setColor()` for console text color, `clearScreen()`, `drawLine()` for UI formatting, and `waitForKeyPress()`.
*   **Gender Guessing**: This feature likely relies on a predefined list of common male and female names (possibly Polish names, given the method names) hardcoded or loaded from a file.
*   **ASCII Conversion**: Iterates through the string and converts each character to its integer ASCII value.
*   **File I/O**: Uses C++ file streams (`fstream`) for saving and loading text data.
*   **Error Handling**: Implements checks for invalid user inputs (e.g., out-of-bounds positions for insertion/deletion, file not found) and provides informative error messages.
*   **User Interface**: A menu-driven console interface built using formatted output and console manipulation functions from `Utils.h`.

## 🤝 Contributing

Contributions to **StringMaster Pro** are highly encouraged! If you have ideas for new string operations, more sophisticated text analysis features, UI improvements, or performance optimizations:

1.  Fork the repository.
2.  Create a new branch for your feature: `git checkout -b feature/your-string-tool-idea`
3.  Implement your changes and commit them: `git commit -m "Feature: Add your string tool idea"`
4.  Push your changes to your branch: `git push origin feature/your-string-tool-idea`
5.  Open a Pull Request.

Please ensure your code is well-commented and aligns with the project's existing style.

## ✍️ Author

**Adrian Lesniak**
_C++ Developer & Text Processing Enthusiast_

## 📃 License

This project is licensed under the **MIT License**.
The full text of the license is available at: [https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

---
🧩 _Mastering text, one operation at a time!_

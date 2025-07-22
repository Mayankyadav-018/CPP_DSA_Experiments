Name – Mayank Kumar Yadav
PRN – 24070123060
CLASS – ENTC A '3'

*Experiment No. 1*

Aim: Downloading and Installing VS Code, (Hello World and Calculator program)
Procedure:

a)	Experiments
1.	Installation
Downloading and Installing VS Code
To successfully complete this tutorial, you must do the following steps:
1.	Install Visual Studio Code.
2.	Install the C/C++ extension for VS Code. You can install the C/C++ extension by searching for 'c++' in the Extensions view (Ctrl+Shift+X).
 
3.	Get the latest version of Mingw-w64 via MSYS2, which provides up-to-date native builds of GCC, Mingw-w64, and other helpful C++ tools and libraries. You can download the latest installer from the MSYS2 page or use this link to the installer.
4.	Follow the Installation instructions on the MSYS2 website to install Mingw-w64. Take care to run each required Start menu and pacman command.
5.	Install the Mingw-w64 toolchain (pacman -S --needed base-devel mingw-w64-x86_64-toolchain). Run the pacman command in a MSYS2 terminal. Accept the default to install all the members in the toolchain group.
6.	Add the path to your Mingw-w64 bin folder to the Windows PATH environment variable by using the following steps:
1.	In the Windows search bar, type 'settings' to open your Windows Settings.
2.	Search for Edit environment variables for your account.
3.	Choose the Path variable in your User variables and then select Edit.
4.	Select New and add the Mingw-w64 destination folder path to the system path. The exact path depends on which version of Mingw-w64 you have installed and where you installed it. If you used the settings above to install Mingw-w64, then add this to the path: C:\msys64\mingw64\bin.
5.	Select OK to save the updated PATH. You will need to reopen any console windows for the new PATH location to be available.
Check your MinGW installation
To check that your Mingw-w64 tools are correctly installed and available, open a new Command Prompt and type:
gcc --version
g++ --version
gdb --version
1.	If you don't see the expected output or g++ or gdb is not a recognized command, make sure your PATH entry matches the Mingw-w64 binary location where the compilers are located. If the compilers do not exist at that PATH entry, make sure you followed the instructions on the MSYS2 website to install Mingw-w64.
2.	If gcc has the correct output but not gdb, then you need to install the packages you are missing from the Mingw-w64 toolset.
o	Missing the mingw-w64-gdb package is one cause of the "The value of miDebuggerPath is invalid." message upon attempted compilation if your PATH is correct.
As you go through the tutorial, you will see three files created in a .vscode folder in the workspace:
•	tasks.json (build instructions)
•	launch.json (debugger settings)
•	c_cpp_properties.json (compiler path and IntelliSense settings)
Add a source code file
In the File Explorer title bar, select the New File button and name the file helloworld.cpp.
Now press Ctrl+S to save the file. Notice how the file you just added appears in the File Explorer view (Ctrl+Shift+E) in the side bar of VS Code:
 
You can also enable Auto Save to automatically save your file changes, by checking Auto Save in the main File menu.
The Activity Bar on the far left lets you open different views such as Search, Source Control, and Run. You'll look at the Run view later in this tutorial. You can find out more about the other views in the VS Code User Interface documentation.
Note: When you save or open a C++ file, you may see a notification from the C/C++ extension about the availability of an Insiders version, which lets you test new features and fixes. You can ignore this notification by selecting the X (Clear Notification).
Run helloworld.cpp
Remember, the C++ extension uses the C++ compiler you have installed on your machine to build your program. Make sure you have a C++ compiler installed before attempting to run and debug helloworld.cpp in VS Code.
1.	Open helloworld.cpp so that it is the active file.
2.	Press the play button in the top right corner of the editor.
 
3.	Choose C/C++: g++.exe build and debug active file from the list of detected compilers on your system.
 
You'll only be asked to choose a compiler the first time you run helloworld.cpp. This compiler will be set as the "default" compiler in tasks.json file.
4.	After the build succeeds, your program's output will appear in the integrated Terminal.
 
 
C++ Program Structure
#include<iostream>
usingnamespace std;

// main() is where program execution begins.
intmain(){
   cout <<"Hello World";// prints Hello World
return0;
}

•	The C++ language defines several headers, which contain information that is either necessary or useful to your program. For this program, the header <iostream> is needed.
•	The line using namespace std; tells the compiler to use the std namespace. Namespaces are a relatively recent addition to C++.
•	The next line '// main() is where program execution begins.' is a single-line comment available in C++. Single-line comments begin with // and stop at the end of the line.
•	The line int main() is the main function where program execution begins.
•	The next line cout << "Hello World"; causes the message "Hello World" to be displayed on the screen.
•	The next line return 0; terminates main( )function and causes it to return the value 0 to the calling process.

Algorithm: Basic Arithmetic Operations(Calculator)
1) Start
2) Declare two integer variables: a and b
3) Display "Enter first number:"
4) Read input and store it in a
5) Display "Enter second number:"
6) Read input and store it in b
7) Calculate a + b and display "Addition: " followed by the result
8) Calculate a - b and display "Subtraction: " followed by the result
9) Calculate a * b and display "Multiplication: " followed by the result
10) Calculate a / b and display "Division: " followed by the result (assume b ≠ 0)
11) End



Conclusion:
In this experiment, we successfully installed Visual Studio Code and set up the environment for C++ programming.
We wrote and executed a simple "Hello World" program, which verified that the compiler and editor were configured correctly.
This experiment helped us understand the basic setup process and the structure of a simple C++ program. 
It laid the foundation for writing and executing more complex C++ programs in the future.

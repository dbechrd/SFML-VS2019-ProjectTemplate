This template serves as an example of a good way to configure a VS 2019 project for both x86 and x64 targets.

All of the files in /lib and /include, and all of the .dlls in /bin are the same files distributed with SFML 2.5.1, as retrieved from the following URL on April 10, 2020:
https://www.sfml-dev.org/download/sfml/2.5.1/

The following download links on that page were used to obtain the x86 and x64 files, respectively:

Visual C++ 15 (2017) - 32-bit
https://www.sfml-dev.org/files/SFML-2.5.1-windows-vc15-32-bit.zip

Visual C++ 15 (2017) - 64-bit
https://www.sfml-dev.org/files/SFML-2.5.1-windows-vc15-64-bit.zip

Many project settings were changed from the default VS2019 "Empty Project" template, most of which were simple changes to the directory structure to create something sane and usable for a multi-target project.

For some or all combinations of (x86/Debug, x86/Release, x64/Debug, x64/Release), the following project settings were changed:

General
    Output Directory
    Intermediate Directory
    Target Name
Debugging
    Working Directory
VC++ Directories
    Include Directories
    Library Directories
    Source Directories
Linker
    Input

For further information, please download and open the project file in Visual Studio 2019 and inspect the directory layout and whichever project properties you're interested in.

The example application, Pong.cpp, was taken directly from SFML 2.5.1's examples/pong directory.

Hope this helps those who are confused about how to use SFML in a 64-bit application, or how to sanely configure a multi-target project in VS 2019 in general.

Happy coding!
-Dan
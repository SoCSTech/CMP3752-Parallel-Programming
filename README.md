# OpenCL Installation Guide for CMP3752 Parallel Programming

These instructions were tested on Windows 11 on one of the Lab machines in INB1102, with an Intel CPU and an NVIDIA GPU. These instructions should also work for AMD CPUs or GPUs.

## Setup

### Required Components

* Visual Studio 2022
* Intel OpenCL Software Development Kit (SDK)
* Intel CPU OpenCL Runtime
* GPU OpenCL Runtime

### Explaination

The Intel OpenCL SDK is what allows your computer to develop and compile OpenCL code.

The Intel CPU OpenCL Runtime is what allows OpenCL code to communicate with Intel CPUs. It should also work for AMD CPUs as they use the same architecture.

The GPU OpenCL Runtime is what allows OpenCL code to communicate with GPUs. This runtime is normally installed automatically with your GPU drivers.

### Installation Process

This installation process is assuming you are using Windows 11 with an Intel or AMD CPU, and a discrete NVIDIA or AMD GPU.

We understand that not everybody will have access to a Windows machine with a discrete NVIDIA or AMD GPU at home. As we are only able to test on the lab machines, we are unable to provide detailed instructions for alternative hardware.

Please try the following instructions, but if you are unable to set up OpenCL on your personal machine, use the lab PCs either in person or on Splashtop.

1. Make sure Visual Studio 2022 is installed on your machine.
2. Install the Intel OpenCL SDK from here.
3. Install the Intel CPU OpenCL Runtime from here. The Intel runtime should also work for AMD CPUs.
4. The GPU OpenCL runtime should be automatically installed with your GPU drivers if you have an NVIDIA or AMD GPU.

Once this nis done, you should be ready to test the environment.

## Testing

1. Head to the module GitHub repo here, and download (or clone) the contents to your machine. The module files take the form of a Visual Studio solution (OpenCL Tutorials.sln) containing 3 projects (Tutorial 1, Tutorial 2, Tutorial 3).
2. Open the solution, and then build Tutorial 1 by right clicking on the tutorial on the right and selecting 'Build'.
3. If the project does not successfully build, then your OpenCL SDK is not installed properly. In this case, review the installation process above.
4. If the project does successfully build, then navigate to Tutorial 1\x64\Debug. You should see 'Tutorial 1.exe'
5. Launch a Command Prompt (Powershell will not work), and navigate to this folder. Type "Tutorial 1.exe" (including the quotation marks), and press enter.
6. If your code does not successfully run, then it is likely your CPU/GPU runtimes are not installed.
7. If the code does run, run it again but type '"Tutorial 1.exe" -l' (including only double quotation marks). This should display a list of the available platforms and devices.
8. If you see one CPU platform and one GPU platform then your environment is properly set up!
9. You can also use the argument -p and -d to choose what platform and device the code should run on. For example '"Tutorial 1.exe" -p 0', will run on platform 0.
10. If you have successfully followed the above instructions, you can now proceed with the tutorials.

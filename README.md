<p align="left">
<a href="https://github.com/Zeathary/cell-analyzer">
    <img src="https://readme-typing-svg.demolab.com/?font=Georgia&size=24&duration=500&pause=50&multiline=true&repeat=false&width=650&height=250&lines=[ML+Cell+Analyzer];Zachary+Heath;Marvin+Hozi;Lilly+McAfee;Young+Bok+(Abraham)+Kang+PhD;George+Fox+University+Engineering;Software+to+record+and+predict+cell+motion+responding;to+biological+and+mechanical+stimulation." alt="Typing SVG" />
</a>
</p>

# Summary
<p align="left" style="font-family: Georgia; font-size: small; color: #1e81b0">
A program to record and predict cell motion responding to biological and mechanical stimulation. Utilizing the libraries of pysimplegui, opencv and scikit-learn, this program features a graphical user-interface which allows the user to track the number, size, and location of cells within any given image or video taken of cells with a microscope. Can be used to track and visualize useful statistics about the cell cultures in response to biological and mechanical stimulation.
<br>
<br>
Entry Point: prototype/cell-analyzer.py
</p>

# Instructions for Use:
## Conda

[Conda](https://docs.conda.io) is an open-source package management system and environment management system.
We will use Conda to help us create and manage a Python environment with the specific packages needed for this project.

## Installation

We will use a minimal installer for Conda called [Miniconda](https://docs.conda.io/en/latest/miniconda.html).
Follow the instructions below for your operating system.
Note that in all cases, we will be using Python 3.x, _not_ Python 2.7, so make sure you are downloading and installing the correct version of Conda/Miniconda.

### Windows

This section assumes you are installing Conda using a Windows installer for use with the traditional Windows command prompt.
If you are using the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl) (WSL), use the Linux instructions instead.

1.  Download the [latest version](https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe) of Miniconda from the [Windows installer section](https://docs.conda.io/en/latest/miniconda.html#windows-installers) of the Miniconda website

2.  [Install Miniconda](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html), and configure it with the following options if prompted:

    - Yes, add to path

    - No, do not make the system's default Python

    - Yes, create Start menu entries

3.  Verify that your install works as expected using the testing steps described in the [Miniconda installation instructions](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html)

## Environment Setup

Once you have Conda installed, you will need to set up a Conda environment that contains Python itself and all of the supporting packages we'll be using in the project.
Once the environment is created, you will simply activate it and set it as the default interpreter.
To create your Conda environment, complete the following steps:

1. Open a new command-line shell

    - On Windows: run the "Anaconda Prompt" application from the Start menu

2. In your shell, change directory to the location where you are storing this project
   ```cd C:\your\path\```

3. Clone this repository to your local machine:

    ```git clone https://github.com/Zeathary/cell-analyzer.git```

4. Change directory to the newly-cloned `cell-analyzer` directory

5. Create the `cell_analyzer_env` Conda environment:

    ```conda env create -f env_setup.yml```

6. Once the environment is created, activate it:

    ```conda activate cell_analyzer_env```

7. Change your Interpreter in Pycharm (Optional):
   - File > Settings > Project:cell-analyzer > Python Interpreter > Add > Conda Environment > Existing Environment > 
   - ```Interpreter: C:\Users\yourname\miniconda3\envs\cell_analyzer_env\python.exe```
8. Run cell-analyzer.py

If all works as expected, the script will run correctly. If any of the packages report an error, verify that you have first activated the correct Conda environment.

### Building an Executable

In order to make this step very easy, a script has been made to execute commands on your behalf that will initiate the build process with PyInstaller. 
Here are the steps to take if you want to build the project into an executable. You need to have all the modules imported and working for this to go without
any trouble! YOu have been warned!

1. Make sure you are in the same directory as the script. Use the ```cd ./prototype/``` command to get into the 
   prototype folder, assuming you are one level above. If you are not, get to the prototype folder using the ```cd``` command.
2. Ensure that you use your IDE terminal (Must be Powershell on Windows) to run the following command: ```powershell -executionpolicy unrestricted .\build-exec.ps1```.
   You will get a security warning asking you to type the letter R if you want to run the script. Do it. It's safe...

This will execute the script with administrator privileges so it can complete successfully. 

3. Give the script some time to run. It will take time and that is proportional to how fast your computer is. Be patient.
4. After the script is done running, it will generate a directory called "dist" and it will bein the "prototype" folder. Go into
   "dist" and you will find the "cell-analyzer" directory where the executable is: "cell-analyzer.exe". 
5. Congrats, you may now copy/move the "cell-analyzer" folder anywhere you want. It will run on any x64-86 Windows computer!

OPTIONAL: You may delete the folder named "build" it's completely useless and was used build the executable. It's useless now.
You may also delete any file with the suffix ".spec" since those files are also useless now.

Contact mhozi18@our fox email, I will be happy to help you with the build section of this project if you need it!

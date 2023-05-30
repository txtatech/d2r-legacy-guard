# Legacy Guard for Diablo II: Resurrected is a GPU Monitoring and Key Press Script that monitors the GPU usage of the D2R.exe process and sends a simulated key press event when the GPU usage exceeds a threshold.

It is designed to work on Windows systems with Nvidia GPUs and requires the following dependencies to be installed:

- `pynvml`: Python wrapper for NVIDIA Management Library (NVML).
- `pynput`: Library for monitoring and controlling input devices.
- `psutil`: Cross-platform library for retrieving system information.

## Dependency Installation (Via the Release download)

Run the included 'install_deps_only.bat' file to install dependencies used by the script.

(OR)

Run the included 'install_deps_plus_python.bat' if your system needs Python installed. Note: This will install both Python and the script's dependencies.

## Manual Dependency Installation Method:

1. Install the required dependencies by running the following commands:

   pip install pynvml
   pip install pynput
   pip install psutil

## Usage:

Open the script in a Python environment or run it using the command: python start_legacyguard.py

The script will continuously monitor the GPU usage of all processes named "D2R.exe".

If the GPU usage exceeds the specified threshold (40% by default), a simulated key press event for the 'G' key will be sent to the topmost game window.

The GPU monitoring is on a 6 second delay (by default) and to limit polling it is reccommended not to go below 2.5 seconds if the default is manually adjusted.
 
Press the spacebar to pause or resume monitoring.

Please note that this script is specifically designed for Windows systems with Nvidia GPUs.

## Troubleshooting:

If you encounter any issues or errors while running the script, make sure you have the required dependencies installed correctly. 

Additionally, ensure that the "D2R.exe" process is running and accessible by the script. 

Both the start and stop scripts should be located in the same folder as D2R.exe if being launched from inside a mod. 

If not launching the scripts via a mod they can be placed anywhere.

## Notes:

The script is set to a 40% GPU usage threshold by default. (This can be manually adjusted as needed per your requirements)

The script is set to a 6 second polling delay by default. (This can be manually adjusted as needed per your requirements)
It is not reccomended to set the polling delay below 2.5 seconds.

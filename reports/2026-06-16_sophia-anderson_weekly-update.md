Weekly Project Update - GitHub Repository Development

Author: Sophia Anderson

Date: June 16, 2026


Overview

This report provides a weekly update on current progress and ongoing work related to transferring project code, documentation, and supporting materials to GitHub for long-term accessibility and maintainability.


Completed Work

Qwiic BME280 Library Repository

A repository for the Qwiic BME280 library has been completed. This library was converted from CircuitPython to MicroPython.

ADXL375 Accelerometer Library Repository (In Progress)

A repository for the ADXL375 accelerometer library is currently being finalized. This library was developed specifically for MicroPython, using the Adafruit CircuitPython ADXL34x/ADXL37x libraries as references, along with extensive review of the ADXL375 datasheet to verify functionality and accuracy.

The repository includes an original calibration utility, adxl375_calibration.py, developed for the Bumble Bee Transport Project. This utility provides:


Baseline offset correction
Dual-stage low-pass filtering
Simple motion detection capabilities


The implementation is designed to run efficiently on resource-constrained embedded platforms such as the Raspberry Pi Pico W.


Vibration Testing Results (USDA Facilities, July 2025)

Vibration testing was conducted at the USDA facilities using the vibration shaker table located in the shipping containers. Brady Lindsey (USDA) assisted with generating FFT (Fast Fourier Transform) plots.

Summary of Results


The vibration shaker was operated at 25 Hz.
FFT analysis showed a dominant peak at 25 Hz across all three measurement systems (Laser, Tri-Axis, and ADXL375), demonstrating excellent agreement between sensors.
Time-domain analysis showed close alignment between the ADXL375 and the reference sensors during 25 Hz, 3 g excitation testing.
The ADXL375 accurately identified the applied vibration frequency and produced measurements closely matching the reference instrumentation.
The sensor was configured to sample at 100 Hz, satisfying the Nyquist-Shannon sampling criterion with four samples per vibration cycle.


Cost vs. Performance

At approximately $24.95 USD, the ADXL375 performed comparably to significantly more expensive laboratory-grade equipment. Results presented were based on raw, unfiltered measurements. Optional filtering functionality is available within the calibration library but was intentionally not applied during testing.

Conclusion: The ADXL375 is a suitable sensor for transportation and shipment monitoring applications, including beehive transport studies.


Next Steps
BLE Repository (Raspberry Pi Pico W)

Documentation is currently being created for the Bluetooth Low Energy (BLE) system implemented on the Raspberry Pi Pico W. A Standard Operating Procedure (SOP) will be included within the repository.

The BLE implementation focuses on receiving sensor data from the Pico W and downloading that data through a mobile application — a workflow with relatively little existing documentation, requiring significant experimentation and adaptation.

Primary Bumble Bee Transport Project Repository

Once the above repositories are complete, work will begin on the primary Bumble Bee Transport Project repository. Due to the nature of the project and associated USDA work, this repository will likely remain private and accessible only to members of the USDA Sensor Group.

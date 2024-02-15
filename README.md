# Microcontroller Provisioning using BLE

| Supported Targets | ESP32 | ESP32-C2 | ESP32-C3 | ESP32-S2 | ESP32-S3 |
| ----------------- | ----- | -------- | -------- | -------- | -------- |


## Introduction
This code provides a template for provisioning a microcontroller, such as ESP32, using Bluetooth Low Energy (BLE) technology. By following these instructions, you can configure your microcontroller with Wi-Fi credentials using a BLE provisioning application.

### Requirements

* Microcontroller (e.g., ESP32)
* BLE provisioning application (available on app stores)
## Instructions
Microcontroller Configuration:

Ensure that you have the appropriate microcontroller platform (e.g., ESP32) and development environment set up.
Modify the code as needed to fit your specific microcontroller platform.
BLE Provisioning Application:

Download a BLE provisioning application from your device's app store (e.g., Google Play Store, Apple App Store).


### Building the Application 

#### Using Command Line

1. Navigate to the root directory of your ESP-IDF project.

2. Run the build command to compile the application:
    ```
    idf.py build
    ```

##### Flashing the Application

1. Connect your ESP32 device to your computer via USB.

2. Run the flash command to upload the compiled firmware to the ESP32:
    ```
    idf.py -p PORT flash
    ```
    Replace `PORT` with the port name of your ESP32 device (e.g., `/dev/ttyUSB0` on Linux, `COM3` on Windows).

#### Using Visual Studio Code

1. Install the idf extention in vscode.
2. Open the folder containing the project and use the extention to `Build`, `Falsh` and `Monitor`.

## Provisioning Process:

Compile and upload the provided code to your microcontroller.
Upon starting the microcontroller, if it is not yet provisioned, it will enter provisioning mode.
Use the BLE provisioning application to scan for nearby devices.
Connect to the microcontroller from the provisioning application.
Follow the prompts in the provisioning application to enter Wi-Fi credentials.
Once provisioning is successful, the microcontroller will store the credentials and connect to the specified Wi-Fi network.
## Running the Application:

After successful provisioning, the microcontroller will automatically connect to the configured Wi-Fi network.
You can now use the microcontroller for your desired application.

## Implement Your Application Logic:
 - After provisioning, the ESP32 will run the application logic inside the main while loop.
 - Add your application logic within the `while (1)` loop in the `app_main()` function.
 - This is where you can define the behavior of your ESP32 device, such as reading sensors, controlling actuators, or communicating with other devices.

### Additional Notes

- Ensure that you have the necessary permissions and drivers installed to access the serial port of your ESP32 device.
- Refer to the ESP-IDF documentation for troubleshooting and further customization.
- For production deployments, consider implementing security measures such as unique salts and verifiers as mentioned in the code.
- Always test the application thoroughly before deploying it in a production environment.
<p align="center">
  <img src="./img.png" alt="Project Banner" width="100%">
</p>

# SECUREHER 🎯

## Basic Details

### Team Name: HerTz

### Team Members
- Member 1: Iza K Jamaludheen - SCMS School of Engineering & Technology
- Member 2: Ameena Jennath KS - SCMS School of Engineering & Technology

### Project Description
The project aims to design and develop a smart women safety wearable device that provides immediate assistance during emergency situations. The system is designed to be compact, portable, and easy to use, ensuring quick activation even under stress.
The device is built using an ESP32 microcontroller, an ADXL335 accelerometer, a GPS module, and a push button. The accelerometer continuously monitors the user’s motion, while the push button acts as an arming mechanism to prevent false triggers. When the user presses the button, the system enables motion detection for a predefined time window. If abnormal or panic motion is detected within this interval, the system identifies it as an emergency.

### The Problem statement
Ensuring the safety of women in public and isolated environments remains a critical social challenge. In emergency situations, victims may not be able to access their mobile phones to make calls or send messages due to panic, physical restraint, or time constraints.
Therefore, there is a need for a compact, wearable, and easy-to-activate safety device that can automatically detect distress situations and send emergency alerts with location information. The system should minimize false triggering, operate in real time, and provide reliable communication to emergency contacts

### The Solution
The problem of delayed or inaccessible emergency communication is solved by designing a gesture-based, IoT-enabled women safety device that operates independently of mobile phone interaction during critical situations.
The solution uses an ESP32 microcontroller as the central processing unit. A push button is used to intentionally arm the system, which prevents accidental activation. Once armed, an ADXL335 accelerometer continuously monitors the user’s motion to detect abnormal or panic movements.
When the detected acceleration exceeds a predefined threshold within a specific time window, the system identifies the situation as an emergency. The ESP32 then retrieves the user’s real-time location using a GPS module. This information, along with an emergency alert message, is transmitted through a Telegram bot using Wi-Fi connectivity.
---

## Technical Details

### Technologies/Components Used

**For Hardware:**

- Main components:
  ESP32 Development Board – Main microcontroller
  ADXL335 Accelerometer – Motion / panic gesture detection
  GPS Module (NEO-6M) – Real-time location tracking
  Push Button – User confirmation to avoid false triggering
  
- Tools required:
  Arduino IDE
  
---

## Features

List the key features of your project:
- Feature 1: Gesture based emergency detection: detects a panic motion using a 3-axis accelerometer
- Feature 2: Instant Alert via telegram: Sends emergency notifications with location details to predefined contacts through a Telegram bot using Wi-Fi connectivity.
- Feature 3: Real-Time Location Tracking: Fetches live geographical coordinates using a GPS module and shares the user’s location during emergencies
- Feature 4: False Trigger Prevention: Uses a push-button arming mechanism and a predefined time window to ensure alerts are triggered only with user intent.

---

## Implementation]

### For Hardware:

#### Components Required
Microcontroller: ESP32 Development Board [ESP32devkit] with wifi module
Accelerometer: ADXL335 - 3 axus accelerometer with analog output
GPS Module: NEO-6M to provide real time latitude and longitude.
Push button: Momentary push button to prevent false triggers.

#### Circuit Setup
The circuit is constructed by interfacing all input and output components with the ESP32 microcontroller, which acts as the central control unit.
The ADXL335 accelerometer is powered using the 3.3 V supply from the ESP32, and its X, Y, and Z axis output pins are connected to the ESP32’s pins to continuously monitor motion. A push button is connected to a digital pin configured with an internal pull-up resistor, allowing the user to arm the system intentionally.
The GPS module is powered using the 5 V supply and communicates with the ESP32 through UART serial communication, where the GPS transmit pin is connected to the ESP32 receive pin and vice versa. This enables continuous reception of location data.
The ESP32 is powered via USB or battery, and once the connections are established, the circuit is ready for programming and testing.
---

## Project Documentation

### For Hardware:

#### Schematic & Circuit

![Circuit](Add your circuit diagram here)
*Add caption explaining connections*

![Schematic](Add your schematic diagram here)
*Add caption explaining the schematic*

#### Build Photos

![Team](Add photo of your team here)

![Components](Add photo of your components here)
*List out all components shown*

![Build](Add photos of build process here)
*Explain the build steps*

![Final](Add photo of final product here)
*Explain the final build*

---

## Additional Documentation

### For Web Projects with Backend:

#### API Documentation

**Base URL:** `https://api.yourproject.com`

##### Endpoints

**GET /api/endpoint**
- **Description:** [What it does]
- **Parameters:**
  - `param1` (string): [Description]
  - `param2` (integer): [Description]
- **Response:**
```json
{
  "status": "success",
  "data": {}
}
```

**POST /api/endpoint**
- **Description:** [What it does]
- **Request Body:**
```json
{
  "field1": "value1",
  "field2": "value2"
}
```
- **Response:**
```json
{
  "status": "success",
  "message": "Operation completed"
}
```

[Add more endpoints as needed...]

---

### For Mobile Apps:

#### App Flow Diagram

![App Flow](docs/app-flow.png)
*Explain the user flow through your application*

#### Installation Guide

**For Android (APK):**
1. Download the APK from [Release Link]
2. Enable "Install from Unknown Sources" in your device settings:
   - Go to Settings > Security
   - Enable "Unknown Sources"
3. Open the downloaded APK file
4. Follow the installation prompts
5. Open the app and enjoy!

**For iOS (IPA) - TestFlight:**
1. Download TestFlight from the App Store
2. Open this TestFlight link: [Your TestFlight Link]
3. Click "Install" or "Accept"
4. Wait for the app to install
5. Open the app from your home screen

**Building from Source:**
```bash
# For Android
flutter build apk
# or
./gradlew assembleDebug

# For iOS
flutter build ios
# or
xcodebuild -workspace App.xcworkspace -scheme App -configuration Debug
```

---

### For Hardware Projects:

#### Bill of Materials (BOM)

| Component | Quantity | Specifications | Price | Link/Source |
|-----------|----------|----------------|-------|-------------|
| Arduino Uno | 1 | ATmega328P, 16MHz | ₹450 | [Link] |
| LED | 5 | Red, 5mm, 20mA | ₹5 each | [Link] |
| Resistor | 5 | 220Ω, 1/4W | ₹1 each | [Link] |
| Breadboard | 1 | 830 points | ₹100 | [Link] |
| Jumper Wires | 20 | Male-to-Male | ₹50 | [Link] |
| [Add more...] | | | | |

**Total Estimated Cost:** ₹[Amount]

#### Assembly Instructions

**Step 1: Prepare Components**
1. Gather all components listed in the BOM
2. Check component specifications
3. Prepare your workspace
![Step 1](images/assembly-step1.jpg)
*Caption: All components laid out*

**Step 2: Build the Power Supply**
1. Connect the power rails on the breadboard
2. Connect Arduino 5V to breadboard positive rail
3. Connect Arduino GND to breadboard negative rail
![Step 2](images/assembly-step2.jpg)
*Caption: Power connections completed*

**Step 3: Add Components**
1. Place LEDs on breadboard
2. Connect resistors in series with LEDs
3. Connect LED cathodes to GND
4. Connect LED anodes to Arduino digital pins (2-6)
![Step 3](images/assembly-step3.jpg)
*Caption: LED circuit assembled*

**Step 4: [Continue for all steps...]**

**Final Assembly:**
![Final Build](images/final-build.jpg)
*Caption: Completed project ready for testing*

---

### For Scripts/CLI Tools:

#### Command Reference

**Basic Usage:**
```bash
python script.py [options] [arguments]
```

**Available Commands:**
- `command1 [args]` - Description of what command1 does
- `command2 [args]` - Description of what command2 does
- `command3 [args]` - Description of what command3 does

**Options:**
- `-h, --help` - Show help message and exit
- `-v, --verbose` - Enable verbose output
- `-o, --output FILE` - Specify output file path
- `-c, --config FILE` - Specify configuration file
- `--version` - Show version information

**Examples:**

```bash
# Example 1: Basic usage
python script.py input.txt

# Example 2: With verbose output
python script.py -v input.txt

# Example 3: Specify output file
python script.py -o output.txt input.txt

# Example 4: Using configuration
python script.py -c config.json --verbose input.txt
```

#### Demo Output

**Example 1: Basic Processing**

**Input:**
```
This is a sample input file
with multiple lines of text
for demonstration purposes
```

**Command:**
```bash
python script.py sample.txt
```

**Output:**
```
Processing: sample.txt
Lines processed: 3
Characters counted: 86
Status: Success
Output saved to: output.txt
```

**Example 2: Advanced Usage**

**Input:**
```json
{
  "name": "test",
  "value": 123
}
```

**Command:**
```bash
python script.py -v --format json data.json
```

**Output:**
```
[VERBOSE] Loading configuration...
[VERBOSE] Parsing JSON input...
[VERBOSE] Processing data...
{
  "status": "success",
  "processed": true,
  "result": {
    "name": "test",
    "value": 123,
    "timestamp": "2024-02-07T10:30:00"
  }
}
[VERBOSE] Operation completed in 0.23s
```

---

## Project Demo

### Video
[Add your demo video link here - YouTube, Google Drive, etc.]

*Explain what the video demonstrates - key features, user flow, technical highlights*

### Additional Demos
[Add any extra demo materials/links - Live site, APK download, online demo, etc.]

---

## AI Tools Used (Optional - For Transparency Bonus)

If you used AI tools during development, document them here for transparency:

**Tool Used:** [e.g., GitHub Copilot, v0.dev, Cursor, ChatGPT, Claude]

**Purpose:** [What you used it for]
- Example: "Generated boilerplate React components"
- Example: "Debugging assistance for async functions"
- Example: "Code review and optimization suggestions"

**Key Prompts Used:**
- "Create a REST API endpoint for user authentication"
- "Debug this async function that's causing race conditions"
- "Optimize this database query for better performance"

**Percentage of AI-generated code:** [Approximately X%]

**Human Contributions:**
- Architecture design and planning
- Custom business logic implementation
- Integration and testing
- UI/UX design decisions

*Note: Proper documentation of AI usage demonstrates transparency and earns bonus points in evaluation!*

---

## Team Contributions

- [Name 1]: [Specific contributions - e.g., Frontend development, API integration, etc.]
- [Name 2]: [Specific contributions - e.g., Backend development, Database design, etc.]
- [Name 3]: [Specific contributions - e.g., UI/UX design, Testing, Documentation, etc.]

---

## License

This project is licensed under the [LICENSE_NAME] License - see the [LICENSE](LICENSE) file for details.

**Common License Options:**
- MIT License (Permissive, widely used)
- Apache 2.0 (Permissive with patent grant)
- GPL v3 (Copyleft, requires derivative works to be open source)

---

Made with ❤️ at TinkerHub

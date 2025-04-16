# Yaskawa LabVIEW Library

<p align="center">
    <img width="100%" alt="Yaskawa LabVIEW Library" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/banner.png" >
</p>


[![LABView 2010](https://img.shields.io/badge/LABView-2010-yellow?logo=LabVIEW)](#)
[![LABView 2011](https://img.shields.io/badge/LABView-2011-yellow?logo=LabVIEW)](#)
[![LABView 2012](https://img.shields.io/badge/LABView-2012-yellow?logo=LabVIEW)](#)
[![LABView 2013](https://img.shields.io/badge/LABView-2013-yellow?logo=LabVIEW)](#)
[![LABView 2014](https://img.shields.io/badge/LABView-2014-yellow?logo=LabVIEW)](#)
[![LABView 2015](https://img.shields.io/badge/LABView-2015-yellow?logo=LabVIEW)](#)
[![LABView 2016](https://img.shields.io/badge/LABView-2016-yellow?logo=LabVIEW)](#)
[![LABView 2017](https://img.shields.io/badge/LABView-2017-yellow?logo=LabVIEW)](#)
[![LABView 2018](https://img.shields.io/badge/LABView-2018-yellow?logo=LabVIEW)](#)
[![LABView 2019](https://img.shields.io/badge/LABView-2019-yellow?logo=LabVIEW)](#)
[![LABView 2020](https://img.shields.io/badge/LABView-2020-yellow?logo=LabVIEW)](#)
[![LABView 2021](https://img.shields.io/badge/LABView-2021-yellow?logo=LabVIEW)](#)
[![LABView 2022](https://img.shields.io/badge/LABView-2022-yellow?logo=LabVIEW)](#)
[![LABView 2023](https://img.shields.io/badge/LABView-2023-yellow?logo=LabVIEW)](#)
[![LABView 2024](https://img.shields.io/badge/LABView-2024-yellow?logo=LabVIEW)](#)

### 🤖 Effortlessly Communicate with Yaskawa robots

The **Yaskawa SDK** enables seamless integration with Yaskawa robots for automation, data exchange, and remote control. Ideal for industrial automation, research, and advanced robotics applications.

It allows you to connect to a **real robot**.

🔗 **More Information:** [https://underautomation.com/yaskawa](https://underautomation.com/yaskawa)  
🔗 Also available for **[💻 .NET](https://github.com/underautomation/Yaskawa.NET)** & **[🐍 Python](https://github.com/underautomation/yaskawa.py)**

---

**⭐ Star if you like it !**

**👁️ Watch to be notified of latest updates !**

---

## 🚀 TL;DR (Too Long; Didn’t Read)

A powerful and efficient LabVIEW library for communicating with Yaskawa Motoman industrial robots using the High-Speed Ethernet Server (HSES) protocol. Enables seamless connectivity, motion control, and data acquisition.

✅ No additional installations or Yaskawa options are required to use this SDK.

**Key Benefits:**

- 📡 **Fast & Reliable**: Leverage high-speed UDP communication for real-time control.
- 🛠️ **Easy Integration**: Works with .NET projects, compatible with VB.NET and C#.
- 🤖 **Advanced Features**: Supports status monitoring, alarm handling, job selection, and more.
- 🌎 **Cross-Platform**: Works with Windows/Linux using .NET Core.

---





## 📥 Download Example Applications

Explore the **Yaskawa SDK** with fully functional example applications for your LabVIEW version.

📌 **Download:** [📥 UnderAutomation.Yaskawa.lvproj](https://github.com/underautomation/Yaskawa.vi/releases)


<p align="center">
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-connect-to-robot.png" >
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-alarms-and-status.png" >
</p>
<p align="center">
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-servo-job.png" >
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-file-handling.png" >
</p>
<p align="center">
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-positon-move.png" >
    <img height="250" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/main-demo-read-write-registers.png" >
</p>

---
## 📌 Features
The library is a set of .vi files grouped under a library ```UnderAutomation.Yaskawa.lvlib```.

📌 **Download:** [📥 UnderAutomation.Yaskawa.lvlib](https://github.com/underautomation/Yaskawa.vi/releases)

<p align="center">
    <img src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/project.png" >
</p>

### 🖧 **Connect to the robot**
```ConnectToRobot.vi``` allows you to connect to the robot using its IP address.

This VI returns an instance of the robot the High-Speed Ethernet Server protocol. These returned values are to be used as input to the VIs described below.

![Connect to robot](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/connect-to-robot.png)

---

### Alarm

#### Alarm Reset
![alarm-reset](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/alarm-reset.png)

#### Get Alarm
![get-alarm](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-alarm.png)

---

### File

#### Delete File
![delete-file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/delete-file.png)

#### Get File
![get-file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-file.png)

#### Get File List
![get-file-list](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-file-list.png)

#### Load File
![load-file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/load-file.png)

---

### Job

#### Get Executing Job Information
![get-executing-job-information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-executing-job-information.png)

#### Select Job
![select-job](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/select-job.png)

#### Start Job
![start-job](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/start-job.png)

---

### Position

#### Get Cartesian Position
![get-cartesian-position](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-cartesian-position.png)

#### Get Joint Position
![get-joint-position](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-joint-position.png)

#### Move Cartesian
![move-cartesian](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/move-cartesian.png)

#### Move Joints
![move-joints](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/move-joints.png)


---

### Status

#### Get Status Information
![get-status-information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-status-information.png)

#### Get System Information
![get-system-information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-system-information.png)

#### Get Torque
![get-torque](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-torque.png)

---

### Display

#### Display
![display](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/display.png)

---

### Read/Write

#### Read IO

![read-io](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-io.png)

#### Read Registers
- 16 Bytes Char
- 32 Bytes Char
- Byte
- Double
- Integer
- Register
- Single

![read-io](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-registers.png)


#### Read position
- Base Position
- External Position
- Position Variable

![read-io](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-position-variables.png)


---

### Commands

#### Servo Command
![servo-command](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/servo-command.png)

#### Switching Command
![switching-command](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/switching-command.png)


---

## 🔍 Compatibility

✅ **Supported Robots:** DX200, YRC1000, YRC1000 Micro
✅ **Operating Systems:** Windows  
✅ **LabVIEW Versions:** LV2010 and newer  

---

## 📢 Contributing

We welcome contributions! Feel free to:

- Report issues via [GitHub Issues](https://github.com/underautomation/Yaskawa.vi/issues)
- Submit pull requests with improvements
- Share feedback & feature requests

---

## 📜 License

**⚠️ This SDK requires a commercial license.**  
🔗 Learn more: [UnderAutomation Licensing](https://underautomation.com/yaskawa/eula)

---

## 📬 Need Help?

If you have any questions or need support:

- 📖 **Check the Docs**: [Documentation](https://underautomation.com/yaskawa/documentation)
- 📩 **Contact Us**: [Support](https://underautomation.com/contact)

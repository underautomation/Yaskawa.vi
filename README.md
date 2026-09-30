# Yaskawa Robot Communication SDK for LabVIEW

<p align="center">
    <img width="100%" alt="Yaskawa LabVIEW Library" src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/banner.png" >
</p>

[![LabVIEW](https://img.shields.io/badge/LabVIEW-2010_to_2024-yellow)](#compatibility)
[![License](https://img.shields.io/badge/license-commercial-blue)](https://underautomation.com/yaskawa/eula)

**UnderAutomation.Yaskawa for LabVIEW** is a library of VIs that communicates with Yaskawa Motoman robot
controllers (**YRC1000 (micro)**, **MOTOMAN NEXT**, **DX100 / DX200**, **FS100**, **ERC / XRC / MRC**) through the **High Speed Ethernet Server** (HSES) of
the controller, over UDP. Nothing is installed on the controller, no Yaskawa option is needed.

The VIs call the .NET library `UnderAutomation.Yaskawa.dll`, which is included in the package. Use them
to read the status, the alarms and the positions, move the robot, select and start jobs, read variables
and I/O, and transfer files.

- Product page: [underautomation.com/yaskawa](https://underautomation.com/yaskawa)
- Documentation: [underautomation.com/yaskawa/documentation/get-started-labview](https://underautomation.com/yaskawa/documentation/get-started-labview)
- Also available for .NET: [Yaskawa.NET](https://github.com/underautomation/Yaskawa.NET), and Python: [Yaskawa.py](https://github.com/underautomation/Yaskawa.py).

## Installation

Download the zip of your LabVIEW version, `UnderAutomation.Yaskawa_LabVIEW_<year>.zip`, from the
[releases page](https://github.com/underautomation/Yaskawa.vi/releases), or clone this repository. Each
`LabVIEW_<year>` folder contains:

- `UnderAutomation.Yaskawa.lvproj`: the project, with the example `Examples/1. Main demo.vi`;
- `UnderAutomation.Yaskawa/UnderAutomation.Yaskawa.lvlib`: the library of VIs;
- `UnderAutomation.Yaskawa/lib/UnderAutomation.Yaskawa.dll`: the .NET library called by the VIs.

On Windows, unblock the zip file before you extract it (right-click, "Properties", "Unblock").

## Example application

`Examples/1. Main demo.vi` connects to the robot and shows the main features: status and alarms, servo and
jobs, files, positions and motion, registers.

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

## Features

The VIs are grouped in the library `UnderAutomation.Yaskawa.lvlib`.

<p align="center">
    <img src="https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/project.png" >
</p>

### Connection and license

`ConnectToRobot.vi` connects to the robot with its IP address. It returns the robot reference used as
input by the other VIs. `RegisterLicense.vi` registers your license key.

![Connect to robot](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/connect-to-robot.png)

### Alarms

`AlarmReset.vi` resets the alarms. `GetAlarm.vi` reads one of the last alarms.

![Alarm reset](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/alarm-reset.png)
![Get alarm](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-alarm.png)

### Files

`GetFileList.vi`, `GetFile.vi`, `LoadFile.vi` and `DeleteFile.vi` list, download, upload and delete the
files of the controller.

![Get file list](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-file-list.png)
![Get file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-file.png)
![Load file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/load-file.png)
![Delete file](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/delete-file.png)

### Jobs

`SelectJob.vi` and `StartJob.vi` select and start a job. `GetExecutingJobInformation.vi` reads the name,
the line and the step of the executing job.

![Select job](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/select-job.png)
![Start job](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/start-job.png)
![Get executing job information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-executing-job-information.png)

### Positions and motion

`GetCartesianPosition.vi` and `GetJointPosition.vi` read the position of the robot. `MoveCartesian.vi` and
`MoveJoints.vi` move it.

![Get Cartesian position](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-cartesian-position.png)
![Get joint position](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-joint-position.png)
![Move Cartesian](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/move-cartesian.png)
![Move joints](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/move-joints.png)

### Status and system

`GetStatusInformation.vi`, `GetSystemInformation.vi` and `GetTorque.vi` read the status of the controller,
its software version and the torque of each axis. `Display.vi` shows a message on the pendant.

![Get status information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-status-information.png)
![Get system information](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-system-information.png)
![Get torque](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/get-torque.png)
![Display](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/display.png)

### Variables and I/O

`ReadIO.vi` reads the I/O signals. Other VIs read the variables: registers, byte, integer, double
integer, real (`ReadSingle.vi`) and string variables (16 and 32 bytes), position variables, base and
external axis positions.

![Read IO](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-io.png)
![Read registers](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-registers.png)
![Read position variables](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/read-position-variables.png)

### Commands

`ServoCommand.vi` switches the servo on and off. `SwitchingCommand.vi` selects the cycle mode (cycle,
step, continuous).

![Servo command](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/servo-command.png)
![Switching command](https://raw.githubusercontent.com/underautomation/Yaskawa.vi/refs/heads/main/.github/assets/switching-command.png)

The commands (servo, motion, job start, file write) need the remote mode on the controller. The settings
are described in the [Yaskawa.NET README](https://github.com/underautomation/Yaskawa.NET#configure-the-robot).

## Compatibility

- **LabVIEW:** 2010 to 2024, one folder per version.
- **Operating system:** Windows.
- **Controllers:** Yaskawa YRC1000 (micro), MOTOMAN NEXT, DX100 / DX200, FS100, ERC / XRC / MRC, with the High Speed Ethernet Server.

## License

This SDK needs a commercial license. A 30-day trial starts at the first use, no key needed.

- License agreement: [underautomation.com/yaskawa/eula](https://underautomation.com/yaskawa/eula) and [License.md](License.md)
- Trial key: [underautomation.com/license](https://underautomation.com/license?sdk=yaskawa)
- Prices and quote: [underautomation.com/yaskawa](https://underautomation.com/yaskawa)

## Support

- Documentation: [underautomation.com/yaskawa/documentation](https://underautomation.com/yaskawa/documentation)
- Issues: [GitHub Issues](https://github.com/underautomation/Yaskawa.vi/issues)
- Contact: [underautomation.com/contact](https://underautomation.com/contact)

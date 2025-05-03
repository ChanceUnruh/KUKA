# KUKA KRL BAS Commands Explanation

In KUKA Robot Language (KRL), **`BAS`** stands for **Basic Settings**. It is a set of pre-defined system functions used to configure various parameters for the robot’s operation. The **`BAS`** function is used to set the robot’s default behavior and ensure it operates according to the desired settings, such as velocity, acceleration, tool configurations, and coordinate systems.

---

### 1. **BAS (#INIMOV, 0)**
The `BAS (#INIMOV, 0)` command initializes the robot's settings to their default values:
- **`#INIMOV`** refers to the initial movement, essentially resetting the robot to a neutral state upon startup.
- The argument `0` resets both the **`BASE`** and **`TOOL`** coordinates to their default (zeroed) values. This is useful for ensuring that the robot starts from a known position, with all coordinate systems and tool settings cleared.
```krl
BAS (#INIMOV, 0) ;SETS THE BASE AND TOOL TO DEFAULT VALUES
```
---

### 2. **BAS (#VEL_PTP, 100)**
The `BAS (#VEL_PTP, 100)` command sets the robot's velocity for **Point-to-Point (PTP)** movements:
- **`#VEL_PTP`** specifies the velocity for PTP motions.
- The value `100` sets the velocity to a default value (in percent), indicating that the robot should move at full speed during PTP movements.
```krl
BAS (#VEL_PTP, 20) ;SETS THE PTP VELOCITY TO 20% OF THE MAX SPEED
```
---

### 3. **BAS (#ACC_PTP, 20)**
The `BAS (#ACC_PTP, 20)` command sets the robot's acceleration for **Point-to-Point (PTP)** movements:
- **`#ACC_PTP`** specifies the acceleration for PTP motions.
- The value `20` defines the acceleration, with a higher value indicating quicker acceleration. This value is in percent, with 100 representing the maximum possible acceleration.
```krl
BAS (#ACC_PTP, 20) ;SETS THE VALUE FOR PTP ACCELERATION TO 20% OF THE MAX SPEED
```
---

### 4. **$VEL.CP = 0.2**
This command sets the robot's velocity for **Continuous Path (CP)** movements:
- **`$VEL.CP`** controls the speed of the robot when performing CP movements (i.e., when moving along a continuous path like a linear or circular motion).
- The value `0.2` sets the velocity to 0.2 m/s, meaning the robot will move at 20% of its maximum speed during CP operations.
```krl
$VEL.CP = 0.2 ;SETS LIN AND CIRC MOVEMENT TYPES SPEED IN M/S
```
---

### 5. **BAS (#TOOL, 0)**
The `BAS (#TOOL, 0)` command resets the robot's tool settings:
- **`#TOOL`** refers to the robot's tool coordinate system, which defines how the robot interacts with its tool.
- The argument `0` sets the **tool** to its default configuration (i.e., no tool or a zeroed tool frame).
```krl
BAS (#TOOL, 5) ;SETS THE ACTIVE TOOL TO TOOL 5
```
---

### 6. **BAS (#BASE, 0)**
The `BAS (#BASE, 0)` command resets the robot's base settings:
- **`#BASE`** refers to the robot's base coordinate system, which determines the reference frame for the robot's movements.
- The argument `0` sets the **base** to its default configuration (i.e., no offset or transformation applied).
```krl
BAS (#BASE, 2) ;SETS THE ACTIVE BASE TO BASE 2
```
---

These commands are often used at the beginning of a program to ensure that the robot starts with a consistent and known configuration, which helps in avoiding unexpected behavior.

# KUKA KRL Variables
#### Disclaimer:
#### This reference covers the most commonly used variable types in KUKA KRL for basic programming tasks. There are additional variable types and advanced features in KUKA KRL that are not covered here. For a complete reference, consult the official KUKA documentation or the KUKA Robotics System Manual.
---
## BASIC TYPES

```krl
;DECLARATION
DECL INT my_int ;INTEGER (WHOLE NUMBER)
DECL REAL my_real ;REAL (DECIMAL NUMBER)
DECL BOOL my_bool ;BOOLEAN (TRUE OR FALSE)
DECL CHAR my_char ;SINGLE CHARACTER
DECL STRING[20] my_string ;STRING WITH MAX LENGTH 20

;INITIALIZATION
my_int = 5
my_real = 3.14
my_bool = TRUE
my_char = 'A'
my_string = "Hello World"
```

## POSITION AND MOVEMENT TYPES
```krl
;DECLARATION
DECL POS robot_pos ;CARTESIAN POSITION (X,Y,Z,A,B,C)
DECL FRAME base_frame ;TOOL OR BASE FRAME (SIMILAR TO POS)
DECL AXIS joint_axes ;JOINT POSITION (A1 TO A6, E1 TO E6)
DECL E6POS ext_pos ;POSITION INCLUDING EXTERNAL AXES
DECL E6AXIS ext_axes ;AXIS INCLUDING EXTERNAL AXES

;INITIALIZATION
robot_pos = {X 500.0, Y 0.0, Z 600.0, A 0.0, B 90.0, C 180.0}
base_frame = {X 0.0, Y 0.0, Z 0.0, A 0.0, B 0.0, C 0.0}
joint_axes = {A1 0.0, A2 0.0, A3 0.0, A4 0.0, A5 0.0, A6 0.0}
ext_pos = {X 500.0, Y 0.0, Z 600.0, A 0.0, B 90.0, C 180.0, E1 0.0, E2 0.0, E3 0.0, E4 0.0, E5 0.0, E6 0.0}
ext_axes = {A1 0.0, A2 0.0, A3 0.0, A4 0.0, A5 0.0, A6 0.0, E1 0.0, E2 0.0, E3 0.0, E4 0.0, E5 0.0, E6 0.0}

```

## ARRAYS
```krl
;DECLARATION
DECL FRAME my_frame_array[3] ;ARRAY OF POSITIONS (3 ELEMENTS)

;INITIALIZATION
my_frame_array[1] = {X 100.0, Y 0.0, Z 500.0, A 0.0, B 0.0, C 0.0}
my_frame_array[2] = {X 200.0, Y 100.0, Z 500.0, A 0.0, B 0.0, C 0.0}
my_frame_array[3] = {X 300.0, Y 200.0, Z 500.0, A 0.0, B 0.0, C 0.0}
```

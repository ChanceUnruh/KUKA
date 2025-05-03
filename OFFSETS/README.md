# KUKA KRL Offsets
This folder explains how to use offsets in KUKA Robot Language (KRL).

In KRL, the position shift depends on where the colon is placed:

- If the colon is **after** the position (P1 : {}), the shift is relative to the **$TOOL**.
- If the colon is **before** the position ({ } : P1), the shift is relative to the **$BASE**.

### Example – Tool Offset:
```krl
PTP P1 : {X 0, Y 0, Z 100, A 0, B 0, C 0}
```
This moves the robot 100mm in the **Z+ direction** from P1, using the **$TOOL** frame.
***
### Example – Base Offset:
```krl
PTP {X 0, Y 0, Z 100, A 0, B 0, C 0} : P1
```
This moves the robot 100mm in the **Z+ direction** from P1, using the **$BASE** frame.

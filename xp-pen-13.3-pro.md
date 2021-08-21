# Device details
- VendorID: `0x28bd`
- Device ID: `0x092b`
- Product page: https://www.xp-pen.com/product/464.html

# Frame / Express keys (and dial)
## Report Descriptor - Interface 0
```
0x05, 0x01,         /*  Usage Page (Desktop),                   */
0x09, 0x06,         /*  Usage (Keyboard),                       */
0xA1, 0x01,         /*  Collection (Application),               */
0x85, 0x06,         /*      Report ID (6),                      */
0x05, 0x07,         /*      Usage Page (Keyboard),              */
0x19, 0xE0,         /*      Usage Minimum (KB Leftcontrol),     */
0x29, 0xE7,         /*      Usage Maximum (KB Right GUI),       */
0x15, 0x00,         /*      Logical Minimum (0),                */
0x25, 0x01,         /*      Logical Maximum (1),                */
0x75, 0x01,         /*      Report Size (1),                    */
0x95, 0x08,         /*      Report Count (8),                   */
0x81, 0x02,         /*      Input (Variable),                   */
0x05, 0x07,         /*      Usage Page (Keyboard),              */
0x19, 0x00,         /*      Usage Minimum (None),               */
0x29, 0xFF,         /*      Usage Maximum (FFh),                */
0x26, 0xFF, 0x00,   /*      Logical Maximum (255),              */
0x75, 0x08,         /*      Report Size (8),                    */
0x95, 0x06,         /*      Report Count (6),                   */
0x81, 0x00,         /*      Input,                              */
0xC0                /*  End Collection                          */
```

## USB Packets - Interface ?
Regular buttons (From the top, skipping dial)
- 1
  - `06:00:05:00:00:00:00:00`
- 2
  - `06:00:08:00:00:00:00:00`
- 3
  - `06:04:00:00:00:00:00:00`
- 4
  - `06:00:2C:00:00:00:00:00`
- 5
  - `06:00:19:00:00:00:00:00`
- 6
  - `06:01:16:00:00:00:00:00`
- 7
  - `06:01:1D:00:00:00:00:00`
- 8
  - `06:05:11:00:00:00:00:00`

Dial (Only 1 dial)
- Left rotate
  - `06:01:56:00:00:00:00:00`
- Right rotate
  - `06:01:57:00:00:00:00:00`

## Report Descriptor - Interface 2 with "Key"
```

```

## USB Packets - Interface 2 with "Key"
Regular buttons (From the top, skipping dial)
- 1
  - `02:f0:01:00:00:00:00:00:00:00:00:00`
- 2
  - `02:f0:02:00:00:00:00:00:00:00:00:00`
- 3
  - `02:f0:04:00:00:00:00:00:00:00:00:00`
- 4
  - `02:f0:08:00:00:00:00:00:00:00:00:00`
- 5
  - `02:f0:10:00:00:00:00:00:00:00:00:00`
- 6
  - `02:f0:20:00:00:00:00:00:00:00:00:00`
- 7
  - `02:f0:40:00:00:00:00:00:00:00:00:00`
- 8
  - `02:f0:80:00:00:00:00:00:00:00:00:00`
- On Unpress/Key Up
  - `02:f0:00:00:00:00:00:00:00:00:00:00`

Dial (Only 1 dial)
- Left Rotate
  - `02:f0:00:00:00:00:00:02:00:00:00:00`
- Right Rotate
  - `02:f0:00:00:00:00:00:01:00:00:00:00`
- Stop Rotate
  - `02:f0:00:00:00:00:00:00:00:00:00:00`

## Byte Descriptions
- Total bytes: 12
- Total bits: 96
- Total bytes with interface removed: 11
- Total bits with interface removed: 88

# Pen/Digitizer
## Report Descriptor - Interface 1
```
0x05, 0x0D,         /*  Usage Page (Digitizer),                 */
0x09, 0x02,         /*  Usage (Pen),                            */
0xA1, 0x01,         /*  Collection (Application),               */
0x85, 0x07,         /*      Report ID (7),                      */
0x09, 0x20,         /*      Usage (Stylus),                     */
0xA1, 0x00,         /*      Collection (Physical),              */
0x09, 0x42,         /*          Usage (Tip Switch),             */
0x09, 0x44,         /*          Usage (Barrel Switch),          */
0x09, 0x45,         /*          Usage (Eraser),                 */
0x15, 0x00,         /*          Logical Minimum (0),            */
0x25, 0x01,         /*          Logical Maximum (1),            */
0x75, 0x01,         /*          Report Size (1),                */
0x95, 0x03,         /*          Report Count (3),               */
0x81, 0x02,         /*          Input (Variable),               */
0x95, 0x02,         /*          Report Count (2),               */
0x81, 0x03,         /*          Input (Constant, Variable),     */
0x09, 0x32,         /*          Usage (In Range),               */
0x95, 0x01,         /*          Report Count (1),               */
0x81, 0x02,         /*          Input (Variable),               */
0x95, 0x02,         /*          Report Count (2),               */
0x81, 0x03,         /*          Input (Constant, Variable),     */
0x75, 0x10,         /*          Report Size (16),               */
0x95, 0x01,         /*          Report Count (1),               */
0x35, 0x00,         /*          Physical Minimum (0),           */
0xA4,               /*          Push,                           */
0x05, 0x01,         /*          Usage Page (Desktop),           */
0x09, 0x30,         /*          Usage (X),                      */
0x65, 0x13,         /*          Unit (Inch),                    */
0x55, 0x0D,         /*          Unit Exponent (13),             */
0x46, 0x28, 0x2D,   /*          Physical Maximum (11560),       */
0x26, 0xFF, 0x7F,   /*          Logical Maximum (32767),        */
0x81, 0x02,         /*          Input (Variable),               */
0x09, 0x31,         /*          Usage (Y),                      */
0x46, 0x64, 0x19,   /*          Physical Maximum (6500),        */
0x26, 0xFF, 0x7F,   /*          Logical Maximum (32767),        */
0x81, 0x02,         /*          Input (Variable),               */
0xB4,               /*          Pop,                            */
0x09, 0x30,         /*          Usage (Tip Pressure),           */
0x45, 0x00,         /*          Physical Maximum (0),           */
0x26, 0xFF, 0x1F,   /*          Logical Maximum (8191),         */
0x81, 0x42,         /*          Input (Variable, Null State),   */
0x09, 0x3D,         /*          Usage (X Tilt),                 */
0x15, 0x81,         /*          Logical Minimum (-127),         */
0x25, 0x7F,         /*          Logical Maximum (127),          */
0x75, 0x08,         /*          Report Size (8),                */
0x95, 0x01,         /*          Report Count (1),               */
0x81, 0x02,         /*          Input (Variable),               */
0x09, 0x3E,         /*          Usage (Y Tilt),                 */
0x15, 0x81,         /*          Logical Minimum (-127),         */
0x25, 0x7F,         /*          Logical Maximum (127),          */
0x81, 0x02,         /*          Input (Variable),               */
0xC0,               /*      End Collection,                     */
0xC0,               /*  End Collection,                         */
```

## USB Packets - Interface 1
- Hover - Top Left Corner
  - `07:A0:00:00:00:00:00:00:00:00` 
- Hover - Bottom Right Corner
  - `07:A0:FF:7F:FF:7F:00:00:00:00`
- Hover Center - Button Closest to tip
  - `07:A2:B3:38:B6:44:00:00:00:04`
- Hover Center - Button Furthest from tip
  - `07:A4:04:3D:92:40:00:00:00:02`
- Tap - Top Left Corner
  - `07:A1:00:00:00:00:FF:06:00:00`
- Tap - Bottom Right Corner
  - `07:A1:FF:7F:FF:7F:46:0B:00:00`
- Tap Center - Tilt Up
  - `07:A1:56:3E:21:45:C4:0A:10:D3`
- Tap Center - Tilt Down
  - `07:A1:7E:3D:9E:44:45:09:0E:36`
- Tap Center - Tilt Left
  - `07:A1:3A:3E:88:44:7F:0B:D0:11`
- Tap Center - Tilt Right
  - `07:A1:B4:3E:78:41:4F:0F:37:10`
- Tap Center - Button Closest to tip
  - `07:A3:7C:37:62:46:A1:04:0B:0C` 
- Tap Center - Button Furthest from tip
  - `07:A5:6B:3B:C4:47:71:00:FA:F5`

## Report Descriptor - Interface 2 with "Key"
```

```

## USB Packets - Interface 2 with "Key"
- Hover - Top Left Corner
  - `02:a0:93:00:00:00:00:00:00:00:00:00`
- Hover - Bottom Right Corner
  - `02:a0:14:72:80:f3:00:00:00:00:00:00`
- Hover Center - Button Closest to tip
  - `02:A2:EA:33:06:1D:00:00:00:0E:00:00`
- Hover Center - Button Furthest from tip
  - `02:A4:B2:32:37:1F:00:00:08:0B:00:00`
- Tap - Top Left Corner
  - `02:a1:c9:00:a1:00:3d:1b:00:00:00:00`
- Tap - Bottom Right Corner
  - `02:a1:ab:71:be:3f:f7:1d:00:00:00:00`
- Tap Center - Tilt Up
  - `02:a1:d2:35:10:1e:cb:0b:f5:ca:00:00`
- Tap Center - Tilt Down
  - `02:a1:d1:36:88:21:59:17:10:32:00:00`
- Tap Center - Tilt Left
  - `02:a1:cd:34:93:1e:7e:19:d6:f1:00:00`
- Tap Center - Tilt Right
  - `02:a1:d2:37:5b:1f:3e:1b:23:0e:00:00`
- Tap Center - Button Closest to tip
  - `02:a3:d2:35:10:1e:cb:0b:f5:ca:00:00`
- Tap Center - Button Furthest from tip
  - `02:a4:d2:35:10:1e:cb:0b:f5:ca:00:00`

Most likely structure:
- 1 byte: 02 -> Interface 2
- 1 byte: a0/a1/a3/a4 -> Hover / Tap / Button closest to tip / Button furthest from tip
- 2 bytes: X coordinate
- 2 bytes: Y coordinate
- 2 bytes: Pressure Level
- 1 byte: Vertical tilt (Positive is Up)
- 1 byte: Horizontal tilt (Positive is Left)
- 2 bytes: Unused

## Byte Descriptions
- Total bytes: 12
- Total bits: 96
- Total bytes with interface removed: 11
- Total bits with interface removed: 88

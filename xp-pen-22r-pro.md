## Device details
- VendorID: 0x28bd
- Device ID: 0x091b
- Product page: https://www.xp-pen.com/product/541.html

# Frame / Express keys (and dials)
## Report Descriptor - Interface 0
```
const __u8 uclogic_rdesc_xppen_artist_22r_pro_frame_arr[] = {
    0x05, 0x01,         /*  Usage Page (Desktop),                       */
    0x09, 0x06,         /*  Usage (Keyboard),                           */
    0xA1, 0x01,         /*  Collection (Application),                   */
    0x85, 0x06,         /*      Report ID (6),                          */
    0x05, 0x0D,         /*      Usage Page (Digitizer),                 */
    0x09, 0x39,         /*        Usage (Tablet Function Keys)          */
    0xA1, 0x00,         /*        Collection (Physical)                 */
    0x15, 0x00,         /*          Logical Minimum (0),                */
    0x25, 0x01,         /*          Logical Maximum (1),                */
    0x75, 0x01,         /*          Report Size (1),                    */
    0x95, 0x08,         /*          Report Count (8),                   */
    0x81, 0x02,         /*          Input (Variable),                   */
    0x05, 0x07,         /*          Usage Page (Keyboard),              */
    0x19, 0x00,         /*          Usage Minimum (None),               */
    0x29, 0xFF,         /*          Usage Maximum (FFh),                */
    0x26, 0xFF, 0x00,   /*          Logical Maximum (255),              */
    0x75, 0x08,         /*          Report Size (8),                    */
    0x95, 0x06,         /*          Report Count (6),                   */
    0x81, 0x00,         /*          Input,                              */
    0xC0,               /*      End Collection                          */
    0xC0,               /*  End Collection                              */
};
```

## USB Packets - Interface 0
Buttons are from top down, starting left side then right side.
### Left
- 1
  - 06:00:05:00:00:00:00:00
- 2
  - 06:00:08:00:00:00:00:00
- 3
  - 06:04:00:00:00:00:00:00
- 4
  - 06:00:2c:00:00:00:00:00
- 5
  - 06:01:16:00:00:00:00:00
- 6
  - 06:01:16:00:00:00:00:00
- 7
  - 06:05:1d:00:00:00:00:00
- 8
  - 06:03:1d:00:00:00:00:00
- 9
  - 06:00:19:00:00:00:00:00
- 10
  - 06:00:0f:00:00:00:00:00
### Right
- 1
  - 06:01:12:00:00:00:00:00
- 2
  - 06:01:11:00:00:00:00:00
- 3
  - 06:03:11:00:00:00:00:00
- 4
  - 06:01:08:00:00:00:00:00
- 5
  - 06:00:09:00:00:00:00:00
- 6
  - 06:00:07:00:00:00:00:00
- 7
  - 06:00:1b:00:00:00:00:00
- 8
  - 06:01:4c:00:00:00:00:00
- 9
  - 06:01:06:00:00:00:00:00
- 10
  - 06:01:19:00:00:00:00:00
### Left Dial
- L
  - 06:01:56:00:00:00:00:00
- R
  - 06:01:57:00:00:00:00:00
### Right Dial
- L
  - 06:00:2f:00:00:00:00:00
- R
  - 06:00:30:00:00:00:00:00

## Byte Descriptions
- Total bytes: 8
- Total bits: 64
- Total bytes with interface removed: 7
- Total bits with interface removed: 56

## Report Descriptor - Interface 2 with "Key"
```

```

## USB Packets - Interface 2 with "Key"
### Left
- 1
  - 02:f0:01:00:00:00:00:00:00:01
- 2
  - 02:f0:02:00:00:00:00:00:00:02
- 3
  - 02:f0:04:00:00:00:00:00:00:03
- 4
  - 02:f0:08:00:00:00:00:00:00:04
- 5
  - 02:f0:10:00:00:00:00:00:00:05
- 6
  - 02:f0:20:00:00:00:00:00:00:06
- 7
  - 02:f0:40:00:00:00:00:00:00:07
- 8
  - 02:f0:80:00:00:00:00:00:00:08
- 9
  - 02:f0:00:01:00:00:00:00:00:09
- 10
  - 02:f0:00:02:00:00:00:00:00:0a
### Right
- 1
  - 02:f0:00:04:00:00:00:00:00:0b
- 2
  - 02:f0:00:08:00:00:00:00:00:0c
- 3
  - 02:f0:00:10:00:00:00:00:00:0d
- 4
  - 02:f0:00:20:00:00:00:00:00:0e
- 5
  - 02:f0:00:40:00:00:00:00:00:0f
- 6
  - 02:f0:00:80:00:00:00:00:00:10
- 7
  - 02:f0:00:00:01:00:00:00:00:11
- 8
  - 02:f0:00:00:02:00:00:00:00:12
- 9
  - 02:f0:00:00:04:00:00:00:00:13
- 10
  - 02:f0:00:00:08:00:00:00:00:14
### Left Dial
- L
  - 02:f0:00:00:00:00:00:02:00:14
- R
  - 02:f0:00:00:00:00:00:01:00:14
### Right Dial
- L
  - 02:f0:00:00:00:00:00:20:00:14
- R
  - 02:f0:00:00:00:00:00:10:00:14

## Byte Descriptions
- Total bytes: 10
- Total bits: 80
- Total bytes with interface removed: 9
- Total bits with interface removed: 72

# Pen/Digitizer
## Report Descriptor - Interface 1
```
const __u8 uclogic_rdesc_xppen_artist_22r_pro_tablet_arr[] = {
	0x05, 0x0D,         /*  Usage Page (Digitizer),             */
	0x09, 0x02,         /*  Usage (Pen),                        */
	0xA1, 0x01,         /*  Collection (Application),           */
	0x85, 0x07,         /*      Report ID (7),                  */
	0x09, 0x20,         /*      Usage (Stylus),                 */
	0xA1, 0x00,         /*      Collection (Physical),          */
	0x09, 0x42,         /*          Usage (Tip Switch),         */
	0x09, 0x44,         /*          Usage (Barrel Switch),      */
	0x09, 0x46,         /*          Usage (Eraser),             */
	0x15, 0x00,         /*          Logical Minimum (0),        */
	0x95, 0x03,         /*          Report Count (3),           */
	0x81, 0x02,         /*          Input (Variable),           */
	0x95, 0x02,         /*          Report Count (2),           */
	0x81, 0x03,         /*          Input (Constant, Variable), */
	0x09, 0x32,         /*          Usage (In Range),           */
	0x95, 0x01,         /*          Report Count (1),           */
	0x81, 0x02,         /*          Input (Variable),           */
	0x95, 0x02,         /*          Report Count (2),           */
	0x81, 0x03,         /*          Input (Constant, Variable), */
	0x75, 0x10,         /*          Report Size (16),           */
	0x95, 0x01,         /*          Report Count (1),           */
	0x35, 0x00,         /*          Physical Minimum (0),       */
	0x05, 0x01,         /*          Usage Page (Desktop),       */
	0x09, 0x30,         /*          Usage (X),                  */
	0x26, 0x30, 0xBA,   /*          Logical Maximum (47664),    */
	0x09, 0x31,         /*          Usage (Y),                  */
	0x26, 0x9A, 0x68,   /*          Logical Maximum (26778),    */
	0x09, 0x30,         /*          Usage (Tip Pressure),       */
	0x45, 0x00,         /*          Physical Maximum (0),       */
	0x26, 0xFF, 0x1F,   /*          Logical Maximum (8191),     */
	0x81, 0x02,         /*          Input (Variable),           */
	0x09, 0x3D,         /*          Usage (X Tilt),             */
	0x15, 0x81,         /*          Logical Minimum (-127),     */
	0x25, 0x7F,         /*          Logical Maximum (127),      */
	0x75, 0x08,         /*          Report Size (8),            */
	0x95, 0x01,         /*          Report Count (1),           */
	0x81, 0x02,         /*          Input (Variable),           */
	0x09, 0x3E,         /*          Usage (Y Tilt),             */
	0x15, 0x81,         /*          Logical Minimum (-127),     */
	0x25, 0x7F,         /*          Logical Maximum (127),      */
	0x81, 0x02,         /*          Input (Variable),           */
	0xC0,               /*      End Collection,                 */
	0xC0,               /*  End Collection,                     */
};
```

## USB Packets - Interface 1
- Hover - Top Left Corner
  - 07:a0:74:00:00:00:00:00:00:00
- Hover - Bottom Right Corner
  - 07:a0:55:b9:48:68:00:00:00:00
- Tap - Top Left Corner
  - 07:a1:c1:00:a4:00:91:16:00:00
- Tap - Bottom Right Corner
  - 07:a1:d9:b9:4d:68:51:1c:00:00
- Tap Center - Tilt Up
  - 07:a1:f3:5b:e3:31:29:17:0b:d6
- Tap Center - Tilt Down
  - 07:a1:2b:59:bc:35:bd:16:0e:2a
- Tap Center - Tilt Left
  - 07:a1:77:58:59:33:61:18:e9:0e
- Tap Center - Tilt Right
  - 07:a1:41:5c:e8:36:85:18:2a:10
- Tap Center - Button Closest to tip
  - 07:a3:35:56:15:33:4d:0c:0e:f9
- Tap Center - Button Furthest from tip
  - 07:a4:0d:5b:f5:34:00:00:02:fa

## Byte Descriptions
- Total bytes: 10
- Total bits: 80
- Total bytes with interface removed: 9
- Total bits with interface removed: 72

## Report Descriptor - Interface 2 with "Key"
From https://github.com/DIGImend/digimend-kernel-drivers/pull/291/commits/7df6ea248d39e068e04b3dbbc5d1e91a389f9f8e
```
const __u8 uclogic_rdesc_xppen_artist_22r_pro_special_tablet_arr[] = {
    0x05, 0x0D,         /*  Usage Page (Digitizer),                 */
    0x09, 0x02,         /*  Usage (Pen),                            */
    0xA1, 0x01,         /*  Collection (Application),               */
    0x85, 0x02,         /*      Report ID (2),                      */
    0x09, 0x20,         /*      Usage (Stylus),                     */
    0xA0,               /*      Collection (Physical),              */
    0x14,               /*          Logical Minimum (0),            */
    0x25, 0x01,         /*          Logical Maximum (1),            */
    0x09, 0x42,         /*          Usage (Tip Switch),             */
    0x09, 0x44,         /*          Usage (Barrel Switch),          */
    0x09, 0x46,         /*          Usage (Tablet Pick),            */
    0x75, 0x01,         /*          Report Size (1),                */
    0x95, 0x03,         /*          Report Count (3),               */
    0x81, 0x02,         /*          Input (Variable),               */
    0x95, 0x02,         /*          Report Count (2),               */
    0x81, 0x01,         /*          Input (Constant),               */
    0x09, 0x32,         /*          Usage (In Range),               */
    0x95, 0x01,         /*          Report Count (1),               */
    0x81, 0x02,         /*          Input (Variable),               */
    0x95, 0x02,         /*          Report Count (2),               */
    0x81, 0x01,         /*          Input (Constant),               */
    0x75, 0x10,         /*          Report Size (16),               */
    0x95, 0x01,         /*          Report Count (1),               */
    0xA4,               /*          Push,                           */
    0x05, 0x01,         /*          Usage Page (Desktop),           */
    0x55, 0xFD,         /*          Unit Exponent (-3),             */
    0x65, 0x13,         /*          Unit (Inch),                    */
    0x34,               /*          Physical Minimum (0),           */
    0x09, 0x30,         /*          Usage (X),                      */
    0x27, UCLOGIC_RDESC_PEN_PH(X_LM),
                        /*          Logical Maximum (PLACEHOLDER),  */
    0x47, UCLOGIC_RDESC_PEN_PH(X_PM),
                        /*          Physical Maximum (PLACEHOLDER), */
    0x81, 0x02,         /*          Input (Variable),               */
    0x09, 0x31,         /*          Usage (Y),                      */
    0x27, UCLOGIC_RDESC_PEN_PH(Y_LM),
                        /*          Logical Maximum (PLACEHOLDER),  */
    0x47, UCLOGIC_RDESC_PEN_PH(Y_PM),
                        /*          Physical Maximum (PLACEHOLDER), */
    0x81, 0x02,         /*          Input (Variable),               */
    0xB4,               /*          Pop,                            */
    0x09, 0x30,         /*          Usage (Tip Pressure),           */
    0x27, UCLOGIC_RDESC_PEN_PH(PRESSURE_LM),
                        /*          Logical Maximum (PLACEHOLDER),  */
    0x81, 0x02,         /*          Input (Variable),               */
    0xA4,               /*          Push,                           */
    0x54,               /*          Unit Exponent (0),              */
    0x65, 0x14,         /*          Unit (Degrees),                 */
    0x35, 0xC3,         /*          Physical Minimum (-61),         */
    0x45, 0x3C,         /*          Physical Maximum (60),          */
    0x15, 0xC3,         /*          Logical Minimum (-61),          */
    0x25, 0x3C,         /*          Logical Maximum (60),           */
    0x75, 0x08,         /*          Report Size (8),                */
    0x95, 0x02,         /*          Report Count (2),               */
    0x09, 0x3D,         /*          Usage (X Tilt),                 */
    0x09, 0x3E,         /*          Usage (Y Tilt),                 */
    0x81, 0x02,         /*          Input (Variable),               */
    0xB4,               /*          Pop,                            */
    0xC0,               /*      End Collection,                     */
    0xC0                /*  End Collection                          */
};
```

## USB Packets - Interface 2 with "Key"
- Hover - Top Left Corner
- Hover - Bottom Right Corner
- Tap - Top Left Corner
- Tap - Bottom Right Corner
- Tap Center - Tilt Up
- Tap Center - Tilt Down
- Tap Center - Tilt Left
- Tap Center - Tilt Right
- Tap Center - Button Closest to tip
- Tap Center - Button Furthest from tip

## Byte Descriptions
- Total bytes: 
- Total bits: 
- Total bytes with interface removed:
- Total bits with interface removed:

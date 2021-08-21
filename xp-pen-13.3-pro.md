# Device details
- VendorID: 0x28bd
- Device ID: 0x092b
- Product page: https://www.xp-pen.com/product/464.html

# Pen/Digitizer
## Report Descriptor - Interface 1
```

```

## USB Packets - Interface 1
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

## Report Descriptor - Interface 2 with "Key"
```

```

## USB Packets - Interface 2 with "Key"
- Hover - Top Left Corner
  - 02:a0:93:00:00:00:00:00:00:00:00:00
- Hover - Bottom Right Corner
  - 02:a0:14:72:80:f3:00:00:00:00:00:00
- Tap - Top Left Corner
  - 02:a1:c9:00:a1:00:3d:1b:00:00:00:00
- Tap - Bottom Right Corner
  - 02:a1:ab:71:be:3f:f7:1d:00:00:00:00
- Tap Center - Tilt Up
  - 02:a1:d2:35:10:1e:cb:0b:f5:ca:00:00
- Tap Center - Tilt Down
  - 02:a1:d1:36:88:21:59:17:10:32:00:00
- Tap Center - Tilt Left
  - 02:a1:cd:34:93:1e:7e:19:d6:f1:00:00
- Tap Center - Tilt Right
  - 02:a1:d2:37:5b:1f:3e:1b:23:0e:00:00
- Tap Center - Button Closest to tip
  - 02:a3:d2:35:10:1e:cb:0b:f5:ca:00:00
- Tap Center - Button Furthest from tip
  - 02:a4:d2:35:10:1e:cb:0b:f5:ca:00:00

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

### Frame Button Packets
Regular buttons (From the top, skipping dial)
- 1
  - 02:f0:01:00:00:00:00:00:00:00:00:00
- 2
  - 02:f0:02:00:00:00:00:00:00:00:00:00
- 3
  - 02:f0:04:00:00:00:00:00:00:00:00:00
- 4
  - 02:f0:08:00:00:00:00:00:00:00:00:00
- 5
  - 02:f0:10:00:00:00:00:00:00:00:00:00
- 6
  - 02:f0:20:00:00:00:00:00:00:00:00:00
- 7
  - 02:f0:40:00:00:00:00:00:00:00:00:00
- 8
  - 02:f0:80:00:00:00:00:00:00:00:00:00
- On Unpress/Key Up
  - 02:f0:00:00:00:00:00:00:00:00:00:00

Dial (Only 1 dial)
- Left Rotate
  - 02:f0:00:00:00:00:00:02:00:00:00:00
- Right Rotate
  - 02:f0:00:00:00:00:00:01:00:00:00:00
- Stop Rotate
  - 02:f0:00:00:00:00:00:00:00:00:00:00

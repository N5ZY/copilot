# N1MM+ RoverQTH Integration

## Overview

The Co-Pilot automatically updates N1MM+'s RoverQTH field via UDP when you cross grid boundaries. No manual entry required!

## How It Works

1. GPS detects grid boundary crossing
2. Co-Pilot sends UDP command to N1MM+ with new grid
3. N1MM+ updates RoverQTH field automatically
4. All subsequent QSOs logged with correct grid

**Fully automatic** - just drive and operate!

## N1MM+ Requirements

**Minimum Version: 1.0.11082.0 (January 20, 2026)**

This version added UDP support for RoverQTH updates. Earlier versions won't work.

To check your version:
1. Open N1MM+
2. Help → About N1MM Logger+
3. Look for version number

Download latest: [n1mmplus.hamdocs.com](https://n1mmplus.hamdocs.com/)

## N1MM+ Configuration

### 1. Enable UDP Broadcast

1. Open N1MM+
2. Go to **Config → Configure Ports, Mode Control, Winkey, etc...**
3. Click the **Broadcast Data** tab
4. Check **"WSJT/JTDX"** (enables the UDP listener)
5. Note the port number (default: 2333)
6. Click **OK**

### 2. Co-Pilot Settings

1. Go to **Settings** tab in Co-Pilot
2. Under **Contest Logger**, select **N1MM+**
3. Set **N1MM+ TCP Port** to match N1MM+ (default: 2333)
4. Click **Save Settings**

## Testing

### Test Mode Tab

1. Go to **Test Mode** tab
2. Enter a test grid (e.g., `EM01`)
3. Click **"Send to WSJT-X + N1MM+"**
4. Check N1MM+ - RoverQTH should update

### Verify in N1MM+

After sending a test grid:
1. In N1MM+, go to **Config → Change Your Station Data**
2. Look at **Rover QTH** field
3. Should show your test grid

## Troubleshooting

### "RoverQTH not updating"

1. **Check N1MM+ version** - Must be 1.0.11082.0 or newer
2. **Check UDP is enabled** - Broadcast Data → WSJT/JTDX checked
3. **Check port numbers match** - Co-Pilot settings must match N1MM+
4. **Check N1MM+ is running** - Must be open before sending updates

### "Updates work in test but not during contest"

- Make sure N1MM+ is started before the contest begins
- Co-Pilot sends updates on every grid change automatically

### "Wrong grid in log"

- Verify GPS has lock (check status bar)
- RoverQTH updates are sent before each QSO is logged
- Check Alerts tab for "GRID CHANGE" messages

## How QSO Logging Works

When a QSO is logged (from WSJT-X or Manual Entry):

1. Co-Pilot updates RoverQTH to current GPS grid
2. Co-Pilot sends QSO data to N1MM+
3. N1MM+ logs QSO with correct RoverQTH

This ensures every QSO has the right grid, even if you crossed a boundary mid-QSO.

## Manual Override

The button at the bottom of the main window shows:
```
[Send to N1MM+: EM16]
```

Click it to manually send the current grid to N1MM+ if needed.

---

73 de N5ZY

# N5ZY VHF Contest Co-Pilot

VHF/UHF contest automation for amateur radio rovers. Handles the tedious stuff so you can focus on making contacts.

**Version 1.8.31** | February 2026

## Features

### Core Automation
- **Automatic Grid Updates** - GPS tracks your position and updates WSJT-X + N1MM+/N3FJP when you cross grid boundaries
- **Reliable QSO Relay** - Queues QSOs from up to 4 WSJT-X instances to your contest logger with retry logic
- **Battery Monitoring** - Victron SmartShunt integration showing voltage, current, and state of charge
- **Voice Announcements** - Hands-free alerts for grid changes, QSOs logged, GPS lock status

### Situational Awareness
- **PSK Reporter Monitor** - Detects Sporadic-E, multi-hop E, and tropo openings in your area
- **QSY Advisor** - Database of 788 stations showing what bands they operate (built from ARRL public logs)
- **APRS-IS Integration** - Beacon your position and get alerts when other mobiles are nearby

### Specialized Tools
- **Manual Entry** - Log phone/CW contacts with grid or county exchange
- **Grid Corner Tracker** - Track QSOs with other rovers at grid corners (the "grid dance")
- **Slack Notifications** - Auto-post grid activations to Slack channels

## Quick Start

### 1. Install Python 3.10+
Download from [python.org](https://www.python.org/downloads/). During install, check **"Add Python to PATH"**.

### 2. Install Dependencies
In Windows, create a new folder such as c:\n5zy-copilot and download all these file to that folder.
Double-click **`install_dependencies.bat`**

### 3. Run the App
Double-click **`run.bat`**
(make a folder on your desktop and create a shortcut to this file in that folder, along with a shortcut to your N1MM and GPS Clock app and shortcuts to your verious WSJT profiles)

### 4. Configure Settings
1. Go to the **Settings** tab
2. Enter your **callsign**
3. Set your **GPS COM port** (e.g., COM3)
4. Configure **WSJT-X instances** (name, log path, UDP port)
5. Select your **bands** under "My Bands"
6. Click **Save Settings**

## Hardware

| Item | Purpose | Notes |
|------|---------|-------|
| USB GPS Dongle | Grid tracking | Any NMEA-compatible (e.g., VK-172, ~$12) |
| Victron SmartShunt | Battery monitoring | Optional but recommended |

## Documentation

- [Battery Setup Guide](BATTERY_SETUP_GUIDE.md)
- [N1MM+ RoverQTH Guide](N1MM_ROVERQTH_GUIDE.md)
- [QSO Logging Relay](QSO_LOGGING_RELAY.md)
- [QSY Advisor Guide](QSY_ADVISOR_GUIDE.md)

## Support

- **Documentation & Blog**: [n5zy.org/copilot](https://n5zy.org/copilot)
- **Community Forum**: [groups.io/g/n5zy-copilot](https://groups.io/g/n5zy-copilot)
- **Issues**: Use GitHub Issues

## Contributing

Pull requests welcome! This project was developed with assistance from Claude (Anthropic).

## License

MIT License - See [LICENSE](LICENSE)

## Donate

If this tool helps your rover operation, consider supporting development:

[PayPal.me/n5zy](https://paypal.me/n5zy)

---

73 de N5ZY 📻

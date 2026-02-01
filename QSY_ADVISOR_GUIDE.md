# QSY Advisor - Multi-Band Station Database

The QSY Advisor is a searchable database of VHF/UHF stations showing which bands they operate. Use it to identify QSY opportunities and plan contest strategy.

## Features

- **788 stations** pre-loaded from ARRL public logs
- **Searchable** by callsign, grid, or minimum band count
- **Click to lookup** on QRZ.com
- **Distance and bearing** from your current position
- **Fetch updates** from ARRL when new contest results are published

## Using the QSY Advisor Tab

### Search & Filter

- **Callsign**: Search for specific stations (e.g., "K5" finds all K5 calls)
- **Grid**: Filter by grid square (e.g., "EM" shows all EM grids)
- **Min Bands**: Show only stations with 2+, 3+, etc. bands

### Station List

| Column | Description |
|--------|-------------|
| Callsign | Click to open QRZ.com lookup |
| Bands | List of bands operated (6m, 2m, 70cm, etc.) |
| Grids | Grid squares they've operated from |
| # Bands | Total band count |
| Dist (mi) | Distance from your current GPS position |
| Dir | Compass direction to the station |
| Last Seen | Most recent contest appearance |

### Pre-Contest Planning

1. Filter by grids you'll be activating
2. Sort by band count to find multi-band stations
3. Click callsigns to look up on QRZ
4. Reach out via email to coordinate schedules
5. Focus on high-band operators (23cm, 10GHz) for maximum points

### During Contest

When you work a station, check the QSY Advisor to see if they have other bands. Ask them to QSY!

## Updating the Database

### Fetch ARRL Logs

Click **"Fetch ARRL Logs"** to download public logs from:
- January VHF Contest
- June VHF Contest  
- September VHF Contest
- 222 MHz and Up Distance Contest

**Note:** Only refresh when ARRL publishes new contest results, typically a few weeks before the next contest.

The database date is shown below the search bar.

### Add Stations Manually

Click **"Add Station"** to add a station you know about:
- Enter callsign
- Select bands they operate
- Enter their grid square

### Import Cabrillo Logs

Use the command-line tool to import your own contest logs:

```bash
cd tools
python import_cabrillo.py "path/to/your_contest.log"
```

## Band Codes

| Code | Band |
|------|------|
| 50 | 6m |
| 144 | 2m |
| 222 | 1.25m |
| 432 | 70cm |
| 902 | 33cm |
| 1296 | 23cm |
| 2304 | 13cm |
| 3456 | 9cm |
| 5760 | 5cm |
| 10368 | 3cm |

## Database File

Station data is stored in:
```
data/station_bands.json
```

This file is included with the distribution and can be updated via the Fetch ARRL Logs feature.

## Tips

1. **Sort by # Bands** to find the most capable stations
2. **Filter by nearby grids** to find stations in your target area
3. **High-band stations** (23cm+) are rare and valuable - prioritize them
4. **Rovers** often have many bands - look for "/R" calls
5. **Pre-contest outreach** via QRZ email can set up valuable schedules

---

73 de N5ZY

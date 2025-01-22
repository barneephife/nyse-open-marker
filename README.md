# NYSE Market Time Indicators for TradingView

A Pine Script indicator that displays NYSE market open and close times on TradingView charts, automatically adjusting to your local timezone.

## Screenshots

### Weekly Timeframe View
![Weekly Timeframe Example](images/1w01.jpg)
*Market open/close lines shown on weekly chart*

### Daily Timeframe View
![Daily Timeframe Example](images/1d01.jpg)
*Market open/close lines with next event indicator on daily chart*

### 4-Hour Timeframe View
![4-Hour Timeframe Example](images/4hr01.jpg)
*Detailed view of market events on 4-hour chart*

### 1-Hour Timeframe View
![1-Hour Timeframe Example](images/1hr01.jpg)
*Precise market timing on 1-hour chart*

### 15-Minute Timeframe View
![15-Minute Timeframe Example](images/15m01.jpg)
*High precision view of market events on 15-minute chart*

## Features

- Displays vertical lines at NYSE market open (15:30 CET/CEST) and close (22:00 CET/CEST)
- Shows both historical market events and the next upcoming market open/close
- Next market events are shown with semi-transparent lines and "Next" labels
- Automatically skips weekends when calculating next market events
- Works across all timeframes (1m to Monthly)
- Customizable appearance for both open and close indicators
- Debug information showing time ranges and market status
- Visual confirmation dots at the top of the chart
- Only shows indicators on weekdays (Monday-Friday)
- Automatically handles timezone differences and DST changes

## Installation

1. Open TradingView chart
2. Click "Pine Editor" (Alt+P)
3. Copy and paste the script content
4. Click "Save" and then "Add to Chart"

## Settings

### Open Line Settings
- Line Color: Color of the market open line (default: blue)
- Width: Line thickness (1-4 pixels)
- Style: Line style (solid, dashed, or dotted)

### Close Line Settings
- Line Color: Color of the market close line (default: red)
- Width: Line thickness (1-4 pixels)
- Style: Line style (solid, dashed, or dotted)

### Label Settings
- Show Labels: Toggle visibility of "Market Open" and "Market Close" labels
- Size: Label text size (small, normal, or large)

## Debug Information

The indicator includes a debug panel showing:
- Current bar's time range
- Whether it's a weekday
- Market time check status

## Versions

Two versions are available:
1. `NYSE_Market_Open_Lines.pine`: Basic version with only market open indicators
2. `NYSE_Market_Open_Lines_with_Labels.pine`: Full version with both open and close indicators, plus labels

## Usage Tips

- Use smaller timeframes (15m or less) for precise timing
- The indicator works on any timeframe by detecting if the market time falls within the bar's range
- Blue dots indicate market open times, red dots indicate market close times
- Lines extend beyond the chart for better visibility
- Semi-transparent lines indicate upcoming market events
- "Next Market Open/Close" labels help distinguish future events from historical ones

## Notes

- Times are displayed in your local timezone
- The indicator automatically adjusts for:
  - Standard Time vs Daylight Saving Time
  - Different DST transition dates between US and Europe
  - Your local timezone settings
- Historical data will show all previous market open/close lines
- Next market events automatically adjust for weekends
- Semi-transparent lines indicate upcoming market events
- "Next Market Open/Close" labels help distinguish future events from historical ones

## Market Hours Information

The New York Stock Exchange (NYSE) regular trading hours in different timezones:

Eastern Time (ET):
- Open: 9:30 AM ET
- Close: 4:00 PM ET

Central European Time (CET/CEST):
- Standard Time (October-March):
  - Open: 15:30 CET
  - Close: 22:00 CET
- Daylight Saving Time (March-October):
  - Open: 15:30 CEST
  - Close: 22:00 CEST

---

Zurich is typically in the Central European Time (CET) zone, which is 6 hours ahead of Eastern Time (ET) during standard time and 5 hours ahead during daylight saving time.

NYSE Hours in Zurich Time:
	1.	Standard Time (late fall to early spring):
	•	NYSE opens at 3:30 PM Zurich time. (15:30	)
	•	NYSE closes at 10:00 PM Zurich time. (22:00)
	2.	Daylight Saving Time (spring to late fall):
	•	NYSE opens at 2:30 PM Zurich time. (14:30)
	•	NYSE closes at 9:00 PM Zurich time. (21:00)

Notes:
	•	The U.S. and Europe don't switch between standard and daylight saving time on the same dates, so there are a few weeks of overlap where the difference might temporarily shift.
	•	If you're working with TradingView, it will automatically adjust the displayed hours according to your local time settings.
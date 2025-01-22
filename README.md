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

- Displays vertical lines at NYSE market open and close times in your local timezone
- Shows both historical market events and the next upcoming market open/close
- Next market events are shown with semi-transparent lines and "Next" labels
- Automatically skips weekends when calculating next market events
- Works across all timeframes (1m to Monthly)
- Customizable appearance for both open and close indicators
- Debug information showing time ranges and market status
- Visual confirmation dots at the top of the chart
- Only shows indicators on weekdays (Monday-Friday)
- Automatically handles timezone differences and DST changes worldwide

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

## Market Hours Information

The New York Stock Exchange (NYSE) regular trading hours:

Eastern Time (ET) - Base Market Hours:
- Open: 9:30 AM ET
- Close: 4:00 PM ET

Your Local Time:
The indicator automatically converts NYSE market hours to your local timezone. For example:
- Central European Time: 15:30-22:00 CET/CEST
- Japan Standard Time: 23:30-06:00 JST
- Australian Eastern Time: 00:30-07:00 AEST

## Notes

- Times are automatically converted to your local timezone
- The indicator handles:
  - Any timezone worldwide
  - Standard Time vs Daylight Saving Time
  - Different DST transition dates between regions
  - Your local timezone settings in TradingView
- Historical data will show all previous market open/close lines
- Next market events automatically adjust for weekends
- Semi-transparent lines indicate upcoming market events
- "Next Market Open/Close" labels help distinguish future events from historical ones

---
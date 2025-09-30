# Candle Timer Indicator for MetaTrader 5

A professional and customizable candle timer indicator that displays remaining time until the current candle closes, along with broker server time.

## Features

### Timer Display
- **Real-time countdown** showing minutes and seconds until candle close
- **Percentage completion** option to see how much of the candle has formed
- **Color-coded warnings** based on remaining time:
  - 🟢 Green (Normal): More than 30 seconds remaining
  - 🟠 Orange (Warning): 10-30 seconds remaining
  - 🔴 Red (Critical): Less than 10 seconds remaining

### Server Time Display
- Shows broker server time in HH:MM:SS format
- Positioned below the timer with adjustable spacing
- Smaller font size for better visual hierarchy
- Can be toggled on/off independently

### Customization Options
- **Display Options**:
  - Toggle time display on/off
  - Toggle percentage display on/off
  - Toggle server time display on/off
  - Combine time and percentage in one display

- **Colors**:
  - Customize normal state color (default: Lime Green)
  - Customize warning state color (default: Orange)
  - Customize critical state color (default: Red)
  - Customize server time color (default: Gray)

- **Fonts & Spacing**:
  - Adjustable font size for timer (default: 12)
  - Adjustable font size for server time (default: 9)
  - Choose font family (default: Courier New)
  - Adjust horizontal distance from candle (default: 70 pixels)
  - Adjust vertical distance above candle (default: 0 pixels)
  - Adjust spacing between timer and server time (default: 5 pixels)

## Installation

1. Download `CandleTimer.mq5`
2. Copy the file to your MetaTrader 5 data folder:
   - Open MT5
   - Click `File` → `Open Data Folder`
   - Navigate to `MQL5/Indicators/`
   - Paste the file here
3. Restart MetaTrader 5 or refresh indicators in Navigator
4. Find "CandleTimer" in the Navigator panel under Indicators
5. Drag and drop onto any chart

## Usage

### Basic Setup
1. Attach the indicator to any chart and timeframe
2. The timer will automatically appear above the current candle
3. Adjust settings in the indicator properties as needed

### Input Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| NormalColor | color | Lime Green | Color when time remaining > 30s |
| WarningColor | color | Orange | Color when time remaining 10-30s |
| CriticalColor | color | Red | Color when time remaining < 10s |
| ServerTimeColor | color | Gray | Color for server time display |
| ShowTime | bool | true | Display countdown timer |
| ShowPercent | bool | false | Display completion percentage |
| ShowServerTime | bool | true | Display broker server time |
| FontSize | int | 12 | Font size for timer |
| ServerTimeFontSize | int | 9 | Font size for server time |
| FontName | string | Courier New | Font family |
| PixelDistanceY | int | 0 | Vertical distance above candle |
| PixelDistanceX | int | 70 | Horizontal distance from candle |
| SpacingBetweenLabels | int | 5 | Space between timer and server time |

### Display Modes

**Time Only**
```
<=04:35
12:45:30
```

**Time + Percentage**
```
<=04:35 (85%)
12:45:30
```

**Percentage Only**
```
(85%)
12:45:30
```

## Technical Details

- **Platform**: MetaTrader 5
- **Type**: Chart Indicator
- **Timer Update**: Every second
- **Position**: Dynamically follows the current candle
- **Compatibility**: All timeframes and instruments

## Features in Detail

### Smart Positioning
The indicator intelligently positions itself relative to the current candle's high point, automatically adjusting as you zoom or scroll the chart.

### Auto-Update
Updates every second to provide accurate countdown information without requiring manual refresh.

### Multi-Timeframe Support
Works seamlessly on all timeframes from M1 to MN1.

### Non-Intrusive Design
The indicator is set to be non-selectable and hidden from object lists to prevent accidental modification while trading.

## Tips

- Use smaller `PixelDistanceX` values to position closer to candle
- Increase `SpacingBetweenLabels` if text overlaps
- Disable `ShowPercent` for cleaner display on smaller timeframes
- Match `ServerTimeColor` to your chart theme for better aesthetics
- For dark themes, use bright colors (White, Cyan, Yellow)
- For light themes, use darker colors (Black, Dark Blue, Dark Red)

## Troubleshooting

**Timer not showing?**
- Check if indicator is loaded in Indicator List (Ctrl+I)
- Verify chart has enough space above current candle
- Try adjusting PixelDistanceY

**Position looks wrong after zooming?**
- The indicator auto-adjusts on chart events
- If stuck, remove and re-add the indicator

**Server time seems incorrect?**
- This displays your broker's server time, not local time
- Verify with your broker's timezone settings

## Features

- Added broker server time display
- Added customizable spacing between elements
- Added server time color customization
- Improved positioning system
- Initial release
- Basic timer functionality
- Color-coded warnings
- Customizable display options

## Download

[Thirtynader-Candle Timer](https://github.com/Thirtynader/Candle-Timer/releases)

## Preview

![Thirtynader-Candle Timer preview](https://github.com/Thirtynader/Candle-Timer/blob/main/TCT1.png)
![Thirtynader-Candle Timer](https://github.com/Thirtynader/Candle-Timer/blob/main/TCT1.png)

## Credits

**Developer**: Thirtynader 

## License

This indicator is provided as-is for personal and commercial use.

## Support

Email: Thirtynader[@]gmail.com
---

**Happy Trading! 📈**

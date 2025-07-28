# 📊 Custom Chart Component for PowerApps (Canvas)

This repository contains a **custom PowerApps Canvas Component** built using **Chart.js** that supports all default chart types. It enables flexible, responsive chart visualizations directly inside your PowerApps Canvas app with minimal configuration.

---

## 🔧 Features

- ✅ Supports all Chart.js chart types: `bar`, `line`, `pie`, `doughnut`, `polarArea`, `radar`, `bubble`, `scatter`
- ✅ Fully configurable via component properties
- ✅ Optimized for Canvas Apps
- ✅ Lightweight and embeddable
- ✅ Built using PowerApps Component Framework (PCF)

---

## 🧩 Component Properties

| Property       | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `chartType`    | Chart type to display (`bar`, `line`, `pie`, etc.)                          |
| `chartData`    | JSON-formatted string for rendering the chart                               |
| `isHorizontal` | (Only for `bar` and `line`) If true, rotates the chart horizontally         |
| `showLegend`   | Boolean to control visibility of the chart legend                           |

---

## 📦 Installation

1. **Enable PCF Components** in Canvas Apps:
   - Go to Power Platform Admin Center
   - Navigate to **Environments → Settings → Features**
   - Turn ON **“Power Apps component framework for canvas apps”**

2. **Import the Solution**:
   - Open **Power Apps → Solutions**
   - Click **Import**, and select `CustomChart.zip`

3. **Use in Canvas App**:
   - Open a Canvas App
   - Insert `ChartComponent` from **Custom Components**
   - Configure its properties via formula bar or property pane

---

## 📘 Sample `chartData` Inputs (PowerApps Formula Format)

> ⚠️ PowerApps requires JSON strings to be wrapped in **double quotes**, and all internal quotes must be doubled (`""`).  
>  
> Use the samples below directly inside the `chartData` formula property:

---

### 📊 Bar
"{
  ""labels"": [""Q1"", ""Q2"", ""Q3"", ""Q4""],
  ""datasets"": [
    {
      ""label"": ""Sales"",
      ""data"": [15000, 20000, 18000, 22000],
      ""backgroundColor"": [""#4dc9f6"", ""#f67019"", ""#f53794"", ""#537bc4""]
    }
  ]
}"

### 📊 Line
"{
  ""labels"": [""Jan"", ""Feb"", ""Mar"", ""Apr""],
  ""datasets"": [
    {
      ""label"": ""Visitors"",
      ""data"": [500, 700, 800, 650],
      ""fill"": false,
      ""borderColor"": ""#4bc0c0"",
      ""tension"": 0.3
    }
  ]
}"

### 📊 Pie
"{
  ""labels"": [""Chrome"", ""Firefox"", ""Safari"", ""Edge""],
  ""datasets"": [
    {
      ""label"": ""Browser Share"",
      ""data"": [60, 20, 10, 10],
      ""backgroundColor"": [""#ff6384"", ""#36a2eb"", ""#cc65fe"", ""#ffce56""]
    }
  ]
}"

### 📊 Doughnut
"{
  ""labels"": [""Online"", ""In-Store"", ""Partner""],
  ""datasets"": [
    {
      ""label"": ""Sales Channels"",
      ""data"": [55, 30, 15],
      ""backgroundColor"": [""#36a2eb"", ""#ffcd56"", ""#4bc0c0""]
    }
  ]
}"

### 📊 PolarArea
"{
  ""labels"": [""North"", ""South"", ""East"", ""West""],
  ""datasets"": [
    {
      ""label"": ""Demand"",
      ""data"": [11, 16, 7, 14],
      ""backgroundColor"": [""#ff6384"", ""#36a2eb"", ""#cc65fe"", ""#ffce56""]
    }
  ]
}"

### 📊 Radar
"{
  ""labels"": [""Speed"", ""Strength"", ""Endurance"", ""Agility"", ""Flexibility""],
  ""datasets"": [
    {
      ""label"": ""Athlete A"",
      ""data"": [65, 59, 90, 81, 56],
      ""borderColor"": ""#4dc9f6"",
      ""backgroundColor"": ""rgba(77, 201, 246, 0.2)""
    }
  ]
}"

### 📊 Bubble
"{
  ""datasets"": [
    {
      ""label"": ""Bubbles"",
      ""data"": [
        { ""x"": 10, ""y"": 20, ""r"": 5 },
        { ""x"": 15, ""y"": 10, ""r"": 10 },
        { ""x"": 20, ""y"": 30, ""r"": 7 }
      ],
      ""backgroundColor"": ""#36a2eb""
    }
  ]
}"

### 📊 Scatter
"{
  ""datasets"": [
    {
      ""label"": ""Scatter Data"",
      ""data"": [
        { ""x"": -10, ""y"": 0 },
        { ""x"": 0, ""y"": 10 },
        { ""x"": 10, ""y"": 5 }
      ],
      ""borderColor"": ""#f67019"",
      ""backgroundColor"": ""#f67019""
    }
  ]
}"





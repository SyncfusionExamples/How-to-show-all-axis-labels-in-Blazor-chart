# How to Show All Axis Labels in a Syncfusion Blazor Chart

## Overview

This sample demonstrates how to display all category axis labels in a Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) component when labels would normally overlap due to limited axis space.

The application renders a column chart using category-based data and configures the primary X-axis with the `LabelIntersectAction` property. Instead of trimming or hiding labels, the sample rotates intersecting labels by 45 degrees so that each category remains visible and readable. This technique is useful when visualizing datasets that contain long text labels or a large number of categories.

## Key Features

- Uses the `SfChart` component to render a chart visualization.
- Configures `ChartPrimaryXAxis` with:
  - `ValueType="ValueType.Category"` for category-based axis labels.
  - `LabelIntersectAction="LabelIntersectAction.Rotate45"` to display all labels without trimming.
- Uses the `ChartSeriesCollection` component to host chart series.
- Uses a `ChartSeries` configured with:
  - `Type="ChartSeriesType.Column"` for column chart rendering.
  - `DataSource="@MedalDetails"` for data binding.
  - `XName="X"` to map category values.
  - `YName="Y"` to map numeric values.
- Demonstrates handling of long category names such as country names without losing label visibility.
- Uses a strongly typed `ChartData` model for chart binding.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the project file:

   `AxisLabel/AxisLabel.csproj`

3. Restore the NuGet packages.
4. Build the project.
5. Run the application using **Ctrl+F5**.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open the integrated terminal.
3. Navigate to the project folder:

```bash
cd AxisLabel
```

4. Restore NuGet packages:

```bash
dotnet restore
```

5. Run the application:

```bash
dotnet run
```

6. Open the local application URL displayed in the terminal after the application starts.

## Project Structure

- `AxisLabel/Pages/Index.razor` - Implements the Syncfusion Blazor Chart sample and demonstrates axis label collision handling using `LabelIntersectAction.Rotate45`.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Refer to the official documentation for axis label customization and label intersection handling: https://help.syncfusion.com/chart-sdk/blazor/charts/axis-customization

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.
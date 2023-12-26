# How-to-show-all-axis-labels-in-Blazor-chart

This article explains how to show all axis label in Blazor Chart Component

**Showing all axis labels in Blazor chart**

By default, intersecting axis labels are hidden in the [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts). You are provided with options to display all the labels and position them intelligently when they collide by using [LabelIntersectAction](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartCommonAxis.html#Syncfusion_Blazor_Charts_ChartCommonAxis_LabelIntersectAction) property. You can choose to hide the intersecting labels or rotate all the labels to arrange in a smart manner within available space. 

The following code snippet demonstrates how to rotate axis labels when they intersect.

**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart Title="Olympic Medals" Width="1000">
	<ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category" LabelIntersectAction="LabelIntersectAction.Rotate45" />
	<ChartSeriesCollection>
		<ChartSeries DataSource="@MedalDetails" XName="X" YName="Y" Type="ChartSeriesType.Column" />
	</ChartSeriesCollection>
</SfChart>

@code {

	public class ChartData
	{
		public string X { get; set; }
		public double Y { get; set; }
	}

	public List<ChartData> MedalDetails = new List<ChartData>
	{
		new ChartData { X= "South Korea", Y= 39 },
		new ChartData { X= "India", Y= 61 },
		new ChartData { X= "Pakistan", Y= 20 },
		new ChartData { X= "Germany", Y= 65 },
		new ChartData { X= "Australia", Y= 15 },
		new ChartData { X= "Italy", Y= 29 },
		new ChartData { X= "United Kingdom", Y= 44 },
		new ChartData { X= "Saudi Arabia", Y= 9 },
		new ChartData { X= "Russia", Y= 40 },
		new ChartData { X= "Mexico", Y= 31 },
		new ChartData { X= "Brazil", Y= 75 },
		new ChartData { X= "China", Y= 51 }
	};

}

```

The following code snippet illustrates the output of the above code snippet.

**Output:**

![](/all-axis-labels.png)

**Conclusion**

I hope you enjoyed learning how to show all axis labels in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!
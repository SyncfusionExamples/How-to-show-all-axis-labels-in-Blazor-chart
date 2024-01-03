# How-to-show-all-axis-labels-in-Blazor-chart

This article explains how to display axis labels without intersecting in the Blazor Chart Component.

**Showing all axis labels in Blazor chart**

By default, the axis labels that intersect with each other will be trimmed. [Blazor Chart](https://www.syncfusion.com/blazor-components/blazor-charts) has options to make all the labels visible and position the collided labels smartly by using [LabelIntersectAction](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html) property.

The [LabelIntersectAction](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html) property includes the following customization actions:

- [None](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_None)- Show all labels, regardless of intersections.
- [Hide](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_Hide)- Hide labels that intersect with each other.
- [Trim](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_Trim)- Trim labels to fit within the available space when they intersect.
- [Wrap](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_Wrap)- Wrap labels to multiple lines when they intersect.
- [MultipleRows](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_MultipleRows)- Display labels in multiple rows when they intersect.
- [Rotate45](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_Rotate45)- Rotate labels by 45 degrees when they intersect.
- [Rotate90](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.LabelIntersectAction.html#Syncfusion_Blazor_Charts_LabelIntersectAction_Rotate90)- Rotate labels by 90 degrees when they intersect. 

In the following code example, the intersect labels are rotated to 45 degrees.
 
**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart Title="Olympic Medals" Width="1000">

	<ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category" LabelIntersectAction="LabelIntersectAction.Rotate45"/>

	<ChartSeriesCollection>
		<ChartSeries DataSource="@MedalDetails" XName="X" YName="Y" Type="ChartSeriesType.Column"/>
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

I hope you enjoyed learning how to display axis labels smartly without intersecting in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!
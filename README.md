# HoI4-SGUI-Basic-Pie-Chart-100
A basic and modern implementation of a pie chart using shaders, array logic, and scripted effects for ease of use.

![Showcase Image](https://media.discordapp.net/attachments/795283607987159073/1453255773554475219/image.png?ex=694cc968&is=694b77e8&hm=0e9166fc35f61b503974295d122b6f57abca4b1aaba49241312a69728b36e497&=&format=webp&quality=lossless)

Comes with a **scripted GUI** of a pie chart as well as **scripted effects** containing code that maintains multiple variables contained in an array to sum up to 100 for something such as an influence power struggle.

The implementation uses stacked radial progressbars utilizing the `radial_progress.shader` shader, to create the pie chart. In this example, the array containing the influence variables are `pie_influence`, with its elements being `pie_influence^0`, `pie_influence^1`, `pie_influence^2`, `pie_influence^3`. For more information, visit [The HOI4 Modding Wiki's Data Structures page.](https://hoi4.paradoxwikis.com/Data_structures#Arrays)

The logic is as such:
The top most radial progress bar has frames of `pie_influence^0`.  
The second layer has frames of `pie_influence^0` + `pie_influence^1` to offset for the top layer's frames.  
The third layer has frames of `pie_influence^0` + `pie_influence^1` + `pie_influence^2` to offset the two above layers.  
The lowest layer's frames aren't set as it is a static image that fills the rest of the pie chart.

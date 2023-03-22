---
icon: material/speedometer
---

For users who would like to test their buck regulators, this page demonstrates a simple load test on the [5V buck regulator board](https://www.sparkfun.com/products/21255).

!!! note
	Users who wish to test the maximum parameters of their board will need to consider the thermal and current limitations of the hardware. At minimum:
	
	* A professional/benchtop DC electric load tester should be used instead of the [variable load kit](https://www.sparkfun.com/products/14449).
	* Active cooling should be provided to the buck regulator. 

## Required Hardware
To test the buck regulator boards, users will need the following hardware:

* DC Electric Load Tester
	* We are using the [SparkFun Variable Load Kit](https://www.sparkfun.com/products/14449)
* Power Supply
	* Use a benchtop-style power supply where you can configure the output voltage and see the current draw when loaded.
	* We are using the [80W DC Power Supply](https://www.sparkfun.com/products/retired/9291) *(retired product)*	


<table class="pdf">
	<tr>
		<td>
			<a href="https://www.sparkfun.com/products/retired/9291">
				<center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/2/8/1/6/09291-1.jpg">
				</center>
				<h3 class="title">Power Supply - 80W DC Switching Mode</h3>
			</a>
			TOL-09291
		</td>
		<td>
			<a href="https://www.sparkfun.com/products/14449">
				<center><img src="https://cdn.sparkfun.com/r/140-140/assets/parts/1/2/4/7/9/14449-SparkFun_Variable_Load_Kit-05.jpg">
				</center>
				<h3 class="title">SparkFun Variable Load Kit</h3>
			</a>
			KIT-14449
		</td>
    </tr>
</table>


<div class="grid cards hide" markdown>

-   <a href="https://www.sparkfun.com/products/retired/9291">**Power Supply - 80W DC Switching Mode**<br>
	TOL-09291

	---

	<figure markdown>
	![](https://cdn.sparkfun.com/assets/parts/2/8/1/6/09291-1.jpg)
	</figure></a>

-   <a href="https://www.sparkfun.com/products/14449">**SparkFun Variable Load Kit**<br>
	KIT-14449

	---

	<figure markdown>
	![](https://cdn.sparkfun.com/assets/parts/1/2/4/7/9/14449-SparkFun_Variable_Load_Kit-05.jpg)
	</figure>
	</a>

</div>

## Hardware Setup
For this test, the hardware was setup up as follows:

* Power was supplied to the buck regulator through the soldered barrel jack.
* The output power from the buck regulator was connected to the variable load kit, through the screw terminal.
* Power was enabled using a jumper on the headers, soldered to the `VIN` and `EN` PTH pins.
* No heat sink was attached to the buck regulator.

## Test
To perform the test, the power supply was set to provide 6.08V at up to 4A. Meanwhile, the SparkFun variable load kit was configured to draw 1A(1).
{ .annotate }

1. For current draws over 1.5A, users should include a heat sink; and active cooling for loads over 2.5A.

<figure markdown>
[![](../img/hookup_guide/test_setup.jpg){ width="400" }](../img/hookup_guide/test_setup.jpg "Click to enlarge")<br>
<figcaption markdown>Setup for a basic load test on the 5V Buck Regulator (AP63357DV).</figcaption>
</figure>

Although it is a little hard to see in the picture, the power supply is providing 6.08V with a 928mA current draw to the buck regulator. The variable load kit is drawing 1A with the 5.11V output voltage from the buck regulator.
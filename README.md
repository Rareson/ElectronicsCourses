ElectronicsCourses
==================

Programms for my electronics courses.

This is for proofread of my homework. They are built with Simulink， which belongs to Mathworks.

[![image]](http://www.mathworks.com/index.html?s_tid=gn_logo)
[image]: http://www.mathworks.com/includes_content/nextgen/images/bg_header_mwlogo_notag.jpg "github"

The names of these slx files should explain which problems they are related to.

The scope near the shematic shows the result. I offer a snapshot for every model so you can preview the result.

Some further explanations are provided by Max on [his blog](http://romax.me/). 

You can always have the newest version of this repository by visiting https://github.com/Rareson/ElectronicsCourses

Preview
-------------------
![github](https://github.com/Rareson/ElectronicsCourses/blob/master/Electronics_II_ch1_1_10_b.png "github")

![github](https://github.com/Rareson/ElectronicsCourses/blob/master/Electronics_II_ch1_1_11_d.png "github")



Notes
-----------------

> Electronics_II_ch1_1_9_a, Electronics_II_ch1_1_9_b, Electronics_II_ch1_1_10_b, Electronics_II_ch1_1_10_c use SimPowerSystem. 
> And I made ideal switch enabled.

>> And the following models use Simscape elements.

>> However, with Simscape I found nothing like ideal elements. And I need to use Diode so I set the forward voltage to 0.01V.
>> The result is quite satisfactory.

### Electronics_II_ch1_1_11_c
	The current is quite small for Diode2 but it is through.
	
### Electronics_II_ch1_1_12
	I encountered a major problem here. Transistor (maybe) has no direct mapping in Simulink library, although there is although
	there is a Three-Level Bridge there. I'll try Proteus from here.
	
### Electronics_II_ch1_1_11_d
	Because ch1_1_12 switch to Proteus, I use ch1_1_11_d to test. As noticed, the generic Diode should represents the 
	Silicon diode, which consumes about 0.7V. Considering this, the simulation is successful.
	
### Electronics_II_ch1_1_12_2
	This is a test for the current. When I set it to 1A, the voltage meter shows 15V. But I don't
	know the reason behind it.

### Electronics_II_ch1_1_15_a
	Notice that the potential is realized by DC from generator mode. Actually the result should be determined by the output
	graph of the transistor. For this transistor is stopped, the Ib should be 0 while here Ib~10^(-7), which is close
	to zero. Maybe this works. Wait.... should we use voltage to determine the result? well, this is another way.
	
	Solution: The above result is due to the mode in Proteus, which only allows two extreme conditions.
	
### Electronics_II_ch1_1_15_c
	From the current value of Ib, Ic, we see the transistor is working. But the voltage meter shows 0V, which should
	be 3V. Need to be investigated further.(see the Solution of Electronics_II_ch1_1_15_a.)
	But successfully worked with Multisim. The voltage is 3V.

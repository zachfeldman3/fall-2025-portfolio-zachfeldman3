---
layout: default
title: "Chassis Structural Analysis"
description: ACP
category: featured
image: /assets/images/acpdeformation2.png
---
The goal of this project is to determine that the chasiss of the car is strong enough to sustain the loading on the car. We use a tool in ansys called acp (ansys composites prespost) which allows us to model our sandwhich structure with our given composites orientation. the most important part is the baseplate which undergoes the most loading and supports teh entire weight of the car (220kg). 

#Pretensioning Bolts 

One project used with acp is to see if we can pretension bolts on teh wehel whell. First I did hand calcs using... (chat gpt ill send u the hand calcs describe them  and ill attach the images below on the portfolio). The handcalcs determiend that the core would 100% crush though and that it would not be a good idea to clamp the basepalte in this way.

To validate the hand calcs we modeled it in acp, however we did it assuming a washer of a smaller diamteer (.75in). we determiend our force to be 1000n as arbitrary force value and would multipy that by the safety factor to see what the max force allowed is and see if that was still far below the required force to pretesnion the bolt well. Our max force was a little over 2000N stil lwell below the required necessary to pretension.

---
title       : A Simple Shiny Application
subtitle    : Calculation of Body Mass Index (BMI) Value
author      : 
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax, quiz, bootstrap]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Numerical Input: Weight and Height

Weight (in Kg, default = 60) is a numerical input with minimum and maximum value of 0 and 150. Height (in cm, default = 175) is also a numerical input. The min and max value for height is 0 and 250.


```r
wt = 60
ht = 175

wt
```

```
## [1] 60
```

```r
ht
```

```
## [1] 175
```

---
## Choice Input: Gender

Gender is a choice input in this app and the users can choose either "Male" or "Female". The default value is "Male"


```r
gd = 'Male'

gd
```

```
## [1] "Male"
```

---
## Output: Calculated BMI Value

The BMI value is calculated as $BMI = weight/height^2$, where weight is in Kg and height is in meter.


```r
BMI = wt/(ht/100)^2

BMI
```

```
## [1] 19.59
```

---
## Output: Classify Result To Obese Status

The obese status was determined based on the criteria given in the following link:

http://halls.md/body-mass-index/bmirefs.htm

The result is performed in shiny apps using if-else statement based on different genders and the output is provided to the user.

For the default values (weight = 60 Kg, height = 175 cm, gender = "Male"), the output will be "Underweight".


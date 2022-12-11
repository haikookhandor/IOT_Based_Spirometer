# IOT_Based_Spirometer

1.  In this code we shall first take the input from the sensor when the sensor detects light it
means that the hole passed through it
2.  To get the output in rps we shall calculate number of holes passing through the sensor in
1000 milisecond and then divide the output by number of hole on the slotted disc.
3.  To count number of holes passing through the sensor, we shall take a variable named
counter and add 1 to counter every time the sensor detects the light. 

4.  When the sensor
detects the light it does that for some epsilon time. And so we need to add
while(digitalRead(sensor)); inside the if condition to pause the output for that brief time

That is in technical terms:

```if(digitalRead(sensor))
{
counter = counter +1;
while(digitalRead(sensor));
}
```
5.  The counter variable hold the value of number of holes that passed through the sensor in last
1 second
6.  So counter/number_of_holes = rps
And 1rpm = 60*rps

# Model

As part of this project, our goal is to develop a functional prototype of a low-cost spirometer that can be used for regular home respiratory health checkups. The model determines the impeller rpm-based rate of air expulsion, which can be used to determine lung capacity. This method can be modified to assess lung capacity directly.

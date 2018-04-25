# Butterworth_filter_coefficients-MATLAB-in-C
## Motivation 
In order to obtain the same results as the function 'butter' in MATLAB, uses 'high' and filter order 4 for example
```MATLAB
[BB, AA] = butter(4,freq,'high')
```
## How to use
Just include the header file and write your own codes based on the example programs.
> bwlp.c-lowpass filter coefficient calculator<br />
> bwhp.c-highpass ilter coefficient calculator<br />
> bwbp.c-bandpass filter coefficient calculator<br />
> bwbs.c-bandstop filter coefficient calculator

These are the official guides but i recommend you to check out my example code `butter.cpp`!
## Useful tip
Actually if you have finished the program you might find the result different from that in MATLAB.
<br />
Just as the question in [STACKOVERFLOW](https://stackoverflow.com/questions/10373184/bandpass-butterworth-filter-implementation-in-c).
<br />
This bro indeed has brilliant ability to solve this problem, but i strongly recommend you an easier way.
<br />  
The problem is that the result you got from the code hasn't been normalized, and notice that a variable `sff` either in my example code or in bwhp.c.
<br />
If you set that to 1, the problem will be solved.
```c++
int sff;  //scale flag: 1 to scale, 0 to scale ccof
```
btw. Would someone please help me answer the question on stackoverflow?I don't have any reputation lol.

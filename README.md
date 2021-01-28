# Python-StopWatch


How To Create A Stopwatch In Python
 By Svarnim Agarwal

In this tutorial, we will be going through a fun program to create a stopwatch in python. For this, we will be using time.time() function from the time module.
A stopwatch essentially tells the time elapsed from start to stop.

time.time() in Python
We will be using time.time() function from the time module. Documentation is here.
time.time() function keeps the track of the number of seconds passed from the time the day began i.e. the epoch 00:00.
To use this function we will first import the time module into our code.

import time
Time to create a stopwatch using Python
We will import time module.
The user will press Enter to start the stopwatch. At this point start_time is set using time.time(). So, at this point, start_time has the number of seconds passed since epoch when the clock is started.
Now, the clock will run in the background.
Now the user will press Enter again for stopping the stopwatch. At this point end_time is set using time.time(). So, at this point, end_time has the number of seconds passed since epoch when the clock is stopped.
So, the time lapse can be calculated using the difference between end_time and start_time.
time_lapsed has the value in seconds. We want the output in hours, minutes and seconds. To do this we will use the user-defined function time_convert().
time_convert() will convert seconds into minutes by dividing the number of seconds by 60 and then the number of minutes divided by 60 is the number of hours.
We are printing the Lapsed time also from inside time_convert().
import time
def time_convert(sec):
  mins = sec // 60
  sec = sec % 60
  hours = mins // 60
  mins = mins % 60
  print("Time Lapsed = {0}:{1}:{2}".format(int(hours),int(mins),sec))
input("Press Enter to start")
start_time = time.time()
input("Press Enter to stop")
end_time = time.time()
time_lapsed = end_time - start_time
time_convert(time_lapsed)
Output
If 140 seconds have passed then the output will look like:

Time Lapsed = 0:2:20
So, here it is.  A very simple program to create a Stopwatch in Python.

# SimpleTimer
Simple C++ header only timer wrapper for chrono.

# Timer and Stopwatch
The stopwatch class handles the time keeping, the timer class is a wrapper around the stopwatch class, and automatically starts the stopwatch upon creation so as to write fewer lines of code.

In simple terms, stopwatch allows for you to create the stopwatch variable and start the stopwatch whenever you like. Timer will start the stopwatch as soon as it's created.

# Usage
Download the file and place where your header files reside.

For stopwatch
```c++
#include <SimpleTimer>

int main()
{
    SimpleTimer::Stopwatch stopwatch; //Initalise variable
    stopwatch.Start(); //Start the clock
    //Do work
    stopwatch.Stop();
}
```

For timer
```c++
#include <SimpleTimer>

int main()
{
    SimpleTimer::Timer timer; //Initialise variable. Timer starts ticking on creation.
    //Do work
    timer.Stop();
    std::cout << "Seconds: " << timer.GetTimerSeconds() << "\tMicroseconds: " << timer.GetTimerMicroseconds() << "\tMilliseconds: " << timer.GetTimerMilliseconds() << "\tNanoseconds: " << timer.GetTimerNanoseconds() << "\n";
}
```

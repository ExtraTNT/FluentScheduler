<p align="center">
    <a href="#fluentscheduler">
        <img alt="logo" src="https://raw.githubusercontent.com/fluentscheduler/FluentScheduler/version-6/Logo/logo-200x200.png">
    </a>
</p>

<p align="center">
    <a href="https://ci.appveyor.com/project/TallesL/fluentscheduler">
        <img alt="logo" src="https://ci.appveyor.com/api/projects/status/github/fluentscheduler/fluentscheduler?svg=true">
    </a>
    <a href="https://www.nuget.org/packages/FluentScheduler">
        <img alt="logo" src="https://badge.fury.io/nu/fluentscheduler.svg">
    </a>
</p>

# FluentScheduler

This is a fork from the currently not really maintained FluentScheduler

Automated job scheduler with fluent interface for the .NET platform.

```cs
var schedule = new Schedule(
    () => Console.WriteLine("5 minutes just passed."),
    run => run.Every(5).Minutes()
);

schedule.Start();
```
## Changes to the original one:
 - Fix doubble execution
 - Implement ms timing (only useful around 50ms, below that it can sometimes bug around and should not be used for tasks, where the time must be accurate)


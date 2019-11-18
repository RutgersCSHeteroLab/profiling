


Record and Report hardware counters that reports application, kernel, and library stats.
----------------------------------------------------------------------------------------

Note: the vmlinux given an example of choosing your Linux kernel for profiling both application and the OS

Enable kernel profiling in sysctl conf. Requires sudo permission

```
kernel.perf_event_paranoid = -1
```

Enable kernel profiling for perf.
```
sudo su
echo 0 > /proc/sys/kernel/perf_even_paranoid
```

Record and Report
````
perf record -e cpu-cycles,instructions --vmlinux=/lib/modules/4.17.0/build/vmlinux $APP
perf report
```

Sort and summarize the report
```
perf report --sort=dso
```




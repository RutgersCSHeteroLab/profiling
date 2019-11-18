


Record and hardware counters
-------------------------
```
perf record -e cpu-cycles,instructions --vmlinux=/lib/modules/4.17.0/build/vmlinux appbench/apps/filebench/run.sh
perf report
```

Sort and summarize the report
```
perf report --sort=dso
```




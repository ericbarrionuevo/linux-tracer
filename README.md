# linux-tracer
Linux CPU tracer for MDATP processes

## Context:
This tool is intended for Linux performance data collection, CPU and memory load investigation and analysis or when high CPU or memory load is reported. 
It aims to quickly being able to determine a device’s CPU and memory load and ellaborate on mitigation, as well as propose fixes.
## What it does:
The script linux_cpu_tracer.sh, captures CPU and memory data for a period of time and is at the moment, independent of “Client Analyzer” for Linux. 
It’s a command-line tool, shellscript, that receives an interval of time, in seconds, as its only parameter, and captures CPU and memory activity for that specified period every second. The processes being monitored are wdavdaemon and MDATP auditd plugin. Can also be used in a long run mode in the background, to spot memory leaks.
The script gathers data, by looping through the top command periodically, and filtering out relevant data regarding MDATP processes. Gathered data is then processed and organized so as to present human-readable log files. 

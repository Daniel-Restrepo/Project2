# CS 3502 Project 2 - CPU Scheduling Simulator

## Overview
This project is a CPU Scheduling Simulator for CS 3502: Operating Systems at Kennesaw State University.

I used the provided Windows Forms starter project and extended it for Project 2 by adding:

- Shortest Remaining Time First (SRTF)
- Multi-Level Feedback Queue (MLFQ)
- required performance metrics for comparison:
  - Average Waiting Time
  - Average Turnaround Time
  - CPU Utilization
  - Throughput
  - Average Response Time

The simulator allows the user to enter or load process data, run multiple scheduling algorithms on the same workload, and compare the results through the results screen. The project report and screenshots show the algorithms in action, and the demo video explains the implementation and comparison results. :contentReference[oaicite:0]{index=0} :contentReference[oaicite:1]{index=1}

---

## Algorithms Included

### Original starter algorithms
- FCFS
- SJF
- Priority Scheduling
- Round Robin

### New algorithms added for Project 2
- SRTF
- MLFQ

---

## MLFQ Settings Used
My MLFQ implementation uses:

- 3 queues
- time quanta of 2, 4, and 8
- priority boost interval of 20 time units

These settings were chosen to keep the implementation simple while still demonstrating the core MLFQ behavior.

---

## Performance Metrics
The simulator now displays the following metrics for algorithm runs:

- Average Waiting Time
- Average Turnaround Time
- CPU Utilization
- Throughput
- Average Response Time

### Formulas used
- Waiting Time = Turnaround Time - Burst Time
- Turnaround Time = Finish Time - Arrival Time
- Response Time = Start Time - Arrival Time
- CPU Utilization = (Total Burst Time / Total Elapsed Time) × 100
- Throughput = Number of Processes / Total Elapsed Time

Elapsed time is measured from the earliest process arrival to the latest process finish.

---

## Files Changed
Only one main source file was modified for this project:

- `CpuSchedulerForm.cs`

The following files were intentionally left unchanged:
- `CpuSchedulerForm.Designer.cs`
- `Program.cs`
- `Algorithms.cs`

---

## Platform / Environment
This project uses the Windows Forms starter project, so it is intended to run on **Windows** with **.NET / Visual Studio** support for WinForms. The assignment handout identifies the starter code as Windows-specific. :contentReference[oaicite:2]{index=2}

---

## How to Run

### Option 1: Visual Studio
1. Open the solution/project in Visual Studio.
2. Build the project.
3. Run the application.
4. Use the Scheduler page to enter or load process data.
5. Click one of the algorithm buttons to run the simulation.
6. View the results in the Results page.

### Option 2: Command Line
If your environment supports building the project from the command line:

1. Open a terminal in the project directory.
2. Build the project.
3. Run the generated application.

Example build command:
```bash
dotnet build

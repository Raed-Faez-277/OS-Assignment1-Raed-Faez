# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

A process is peogram in execution that has peogram code, current activity, and allocated resources.


A thread is light weight process that has a thread ID, program counter, and register set.

Thread simply is a small process that comes from a process. A process can have multiple threads.

The difference in terms of memory is that process has it's own memory and contains some keys such as : text section, stack (holds temporary data), and data section. Process provide isolation and protection 

Threads share the same memory within a process. Thread shares resource data.

We used thread because it's lightweight data and shares the same memory and it makes the connection between them easier and faster. Threads have lower creation and context switch times.


## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**
When a process doesn't finish within the time quantum it will go back again to ready queue by FIFO concept.


Example from my output:
```
? P3 executing quantum [3000ms] 
  ? Quantum progress: [███████████████] 100%
  ? P3 completed quantum 3000ms │ Overall progress: [████████████░░░░░░░░] 63%
     Remaining time: 1735ms
  ? P3 yields CPU for context switch

  ? P3 (Priority: 3) enters the ready queue │ Burst time: 4735ms
┌─ Ready Queue ─────────────────────────────────────────────────────────────────
│ [P5 ? P6 ? P7 ? P8 ? P9 ? P10 ? P11 ? P12 ? P13 ? P14 ? P15 ? P2 ? P3]
└───────────────────────────────────────────────────────────────────────────────
```

**Explanation of example:**
In the example above we see that P3 didn't finish his whole burst time, because the quantum time is 3000ms and P3 burst time is 4735ms. It only stays for 3000ms then it should leave and go back to the ready queue. It will going to come back after other processes in line finish.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: P1 is in the new state when it is first created but has not added to the ready queue.

2. **Runnable**: P1 becomes runnable when it is added to the ready queue and ready to be executed by a thread.

3. **Running**: P1 is Running when its thread starts and it is executing for its time quantum on the CPU.

4. **Waiting**: P1 enters the waiting state after its time quantum finishes and it still has remaining burst time, so its going back ro ready queue and waits for its next turn

5. **Terminated**:P1 will be terminated after it finishes his burst time completely

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Server

**Description**: 
The web server can handles multiple clients requests.
Every request is a thread and every thread will take a specific time in the CPU

**Why Round-Robin works well here**: 
The round robin will work here because every thread will share CPU time fairly. 
Also, It will decrease collisions between different pages.

### Example 2: Online Games

**Description**: 
In online games multiple players can join in the same game.
where everything the players do will be treated as threat such as : main menu, buttons, and closing the game.

**Why Round-Robin works well here**:

In this case every threat will be treated equally in the CPU time. 
So it will increase the responsiveness, and players can play the game smoothly.

---

## Summary

**Key concepts I understood through these questions:**
1. How threads work concurrently and share CPU time equally.
2. How round-robin works
3. how to track waiting rime and context switch.

**Concepts I need to study more:**
1. More practice in coding and learn more advanced thread methods.
2.  How to calculate waiting time for each process accurately.

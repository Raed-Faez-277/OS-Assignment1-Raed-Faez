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

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 

# Explain very thorough what a process is and what a process do in a operatingsystem?

## Introduction
According to Andrew Tanenbaum [Ch. 2.1]{tanenbaum_modern_2015}, all runnable software on the computer is organized into sequential processes. One such process is simply an instance of an executing or running program, which also includes the current values of the program counter, registers and variables. In principle, a single CPU can only run one process at a time. While one CPU can rapidly switch between processes, thereby creating an illusion of parallelism, true parallelism requires multiprocessor systems. In order for the operating system to keep track of its running processes, it maintains what is called a process control block (also known as a process table) for each separate process. The process control block is a data structure, similar to a data table, that keeps track of information related to each process.

% Her må det stå noe om PCB, Stack, Data, Text, Adresseområde, Registre, Prosess bytte. 

% Bør forklare prinsippet om eksekvering av prosesser

% Bør forklare prinsippet om ressursgruppering for prosesser

\subsection{Process creation}
With the exception of very simple systems, most operative systems need a way to create processes during operation. According to Tanenbaum \parencite[Ch. 2.1.2]{tanenbaum_modern_2015}, there are four ways of doing this:
\begin{enumerate}
    \item System initialization.
    \item Execution of a process-creation system call by a running process.
    \item A user request to create a new process.
    \item Initiation of a batch job.
\end{enumerate}


\subsection{Process termination}
All good things must come to an end, even processes. This is called termination and is according to Tanenbaum \parencite[Ch. 2.1.3]{tanenbaum_modern_2015} done due to one of the following conditions:

\begin{enumerate}
    \item Normal exit (voluntary).
    \item Error exit (voluntary).
    \item Fatal error (involuntary).
    \item Killed by another process (involuntary).
\end{enumerate}


\begin{comment}
\subsection{Process hierarchies}
When a process is created by another process, they are called a parent and child. In some systems this can be of importance. Just like humans, a child can also reproduce and form further descendants. Processes however have only one parent. 

In UNIX this is important due to the fact that a process, together with all its children and descendants, form a process group. In Windows however, none of this matters. Here all processes are created equal. Some are however more equal than others. A parent is given a “handle”, a special token that lets them control their children. This token can however be passed on to other processes. 
\end{comment}


\subsection{Process states}

There are, in essence, 3 different states that a process can be in. Tanenbaum \parencite[Ch. 2.1.5]{tanenbaum_modern_2015} presents them as follows:

- Running (actually using the CPU at that instant).
- Ready (runnable; temporarily stopped to let another process run).
- Blocked (unable to run until some external event happens).


\begin{comment}
Even given the above mentioned list, a process still has to be created by having an existing process perform a process creation system call. In UNIX “fork” is the system call that creates a new process. This clones the creating process. The child process then uses system calls to change its memory and run a new program. In Windows, however, the Win32 function “CreateProcess” single-handedly handles both creating the new process and loading the correct program into it. This system call alone has 10 parameters which says something of its complexity. In both Windows and UNIX, the parent and child processes have their own distinct address space after the creation process is finished.

\subsection{Process hierarchies}
When a process is created by another process, they are called a parent and child. In some systems this can be of importance. Just like humans, a child can also reproduce and form further descendants. Processes however have only one parent. 

In UNIX this is important due to the fact that a process, together with all its children and descendants, form a process group. In Windows however, none of this matters. Here all processes are created equal. Some are however more equal than others. A parent is given a “handle”, a special token that lets them control their children. This token can however be passed on to other processes. 
\end{comment}


5 * x * y^(2/3)
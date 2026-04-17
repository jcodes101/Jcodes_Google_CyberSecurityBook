# Linux architecture — components and flow

Understanding **Linux architecture** helps security analysts see how a system is organized and how it functions. A request to complete a task starts with the **user** and flows through **applications**, the **shell**, the **Filesystem Hierarchy Standard (FHS)**, the **kernel**, and **hardware**.

---

## User

The **user** is the person interacting with a computer. They initiate and manage computer tasks.

**Linux** is a **multi-user** system: multiple users can use the same resources at the same time.

---

## Applications

An **application** is a program that performs a specific task. Many applications exist on a computer—some are often **pre-installed** (e.g., calculators, calendars); others are **installed later** (e.g., some web browsers or email clients).

On **Linux**, you often use a **package manager** to install applications. A package manager helps users **install**, **manage**, and **remove** packages or applications. A **package** is a piece of software that can be combined with other packages to form an application.

---

## Shell

The **shell** is the **command-line interpreter**. Everything entered into the shell is **text-based**. The shell lets users give commands to the **kernel** and receive responses.

You can think of the shell as a **translator** between you and your computer: it translates the commands you enter so the computer can perform the tasks you want.

---

## Filesystem Hierarchy Standard (FHS)

The **Filesystem Hierarchy Standard (FHS)** is the part of the Linux OS that **organizes data**. It specifies **where** data is stored in the operating system.

A **directory** is a file that organizes where other files are stored. Directories are sometimes called **folders**; they can contain files or other directories. The FHS defines how directories, directory contents, and other storage are organized so the OS knows where to find specific data.

---

## Kernel

The **kernel** is the part of the Linux OS that **manages processes and memory**. It communicates with applications to **route commands**. The **Linux kernel** is unique to the Linux OS and is critical for **allocating resources** in the system. The kernel controls all major functions of the **hardware**, which helps get tasks done more efficiently.

---

## Hardware

**Hardware** is the physical components of a computer (e.g., hard drives, CPUs). Hardware is categorized as **peripheral** or **internal**.

### Peripheral devices

**Peripheral devices** are hardware attached to and controlled by the computer. They are **not** core components required to run the system and can be added or removed freely.

**Examples:** monitors, printers, keyboard, mouse.

### Internal hardware

**Internal hardware** consists of the components **required** to run the computer: a main circuit board (**motherboard**) and everything attached to it.

**Central Processing Unit (CPU)** — The computer’s main **processor** for general computing tasks. The CPU **executes instructions** from programs so those programs can run.

**Random Access Memory (RAM)** — Hardware used for **short-term memory**. Data is stored **temporarily** while you work (e.g., data for an open report). When you close the program, that data is cleared from RAM. Data in RAM **cannot** be accessed after the computer is turned off. The CPU takes data from RAM to run programs.

**Hard drive** — Hardware used for **long-term memory**. Programs and files are stored here for later access. Data on the hard drive **persists** after power off. A computer can have **multiple** hard drives.

---

## Key takeaways

Security analysts benefit from understanding **Linux architecture** and how these pieces fit together. The main components are the **user**, **applications**, **shell**, **Filesystem Hierarchy Standard**, **kernel**, and **hardware**. Each plays a role in how Linux functions.

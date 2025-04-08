Some modifications made!
# PP1

## Goal
All PPn practical exercises share a common purpose: to help you demonstrate—step by step—that you followed and understood the content presented in the weekly lectures. This ongoing feedback loop allows me, as your lecturer, to monitor your personal progress.

In this first exercise, your goal is to demonstrate an understanding of digital computation: specifically, how to map elements of an input set to an output set. We'll begin with simple mappings and gradually increase the difficulty.

**Important:** Start a stopwatch when you begin and work uninterruptedly for 90 minutes. Once time is up, stop immediately and document the point where you had to pause.

---

## Workflow
Each exercise will follow the same basic workflow:

1. **Fork** the repository
2. **Modify and Commit** your solution
3. **Submit your link for Review**

### Step 1: Fork the Repository
A fork is a personal copy of this repository under your own GitHub account. You can edit and manage it freely. Even if you make mistakes, you can always restart or revisit your progress.

To fork this repository:

1. Create a GitHub account (you may use your university email).
2. Open this project in your browser.
3. Click the `Fork` button in the top-right corner:

   ![Fork-Button](./assets/fork.png)

---

4. Scroll down in the dialog and click `Create fork`:

   ![Create fork-Button](./assets/create_fork.png)

---

### Step 2: Modify and Commit
A **commit** is a saved snapshot of your work.

1. Navigate to the `README.md` file.
2. Click the pencil icon to edit the file:

   ![Pencil-Button](./assets/pencil.png)

---

3. Use the built-in editor to make changes.
4. Click `Commit changes` when done:

   ![Commit-Button](./assets/commit_button.png)

---

Add a meaningful comment about what you did and how long it took.

### Step 3: Submit for Review
If you get stuck, visit the discussions forum:
[https://github.com/MaxClerkwell/PP1/discussions](https://github.com/MaxClerkwell/PP1/discussions)

When you have finished working, in Moodle, click "Add solution" and submit the link to your repository.

---

## Tasks

### Task 1: Mapping Symbols to Binary
Fill out the following table, mapping decimal numbers `0` through `15` to their binary representations:

| Decimal | Binary Representation |
|---------|------------------------|
| 0       | 0000                   |
| 1       | 0001                   |
| 2       | 0010                   |
| 3       | 0011                   |
| 4       | 0100                   |
| 5       | 0101                   |
| 6       | 0110                   |
| 7       | 0111                   |
| 8       | 1000                   |
| 9       | 1001                   |
| 10      | 1010                   |
| 11      | 1011                   |
| 12      | 1100                   |
| 13      | 1101                   |
| 14      | 1110                   |
| 15      | 1111                   |

**How many binary digits (bits) are needed?**

Explain how to calculate the number of bits required:
<details>
<summary>Your Answer</summary>
You have 4 digits. The first number is the right digit. It starts with 2^0 (1) then comes 2^1 (2) after that the next number is 2^2 (4) and the last number is 2^3 (8). I took the number an divided it by 2. if the rest is zero then the bit is 0 if the rest is one then the bit is 1. for example: 16/2= 8 R 0 , 
                                                                           8/2=4 R0 , 
                                                                           4/2=2 R0, 
                                                                           2/2=1 R0, 
                                                                           1/2= 0 R1. 
                                                                                                                                                                                                        |2^0 (1)|   
The result of the first Division is the least significant bit so it is 2^0. The last result of the divsion ist the most significant Bit. It is on the last bit. So in my example the order is: 16 = 1000 |  0.   |
      |2^4 (16) |2^3 (8)|2^2 (4)| 2^1 (2) |2^0 (1)
16 =  | 1       | 0     | 0     | 0       | 0
   for the number 16 you need 5 Bits (10000).
</details>

---

### Task 2: Mapping Binary to Binary
Digital processors implement **logical functions** using **logic gates** like NAND, AND, OR, etc.
These functions map binary input sets (voltages) to binary outputs.

Refer to the truth table of a 1-bit full adder:

| C<sub>in</sub> | B | A | Sum (S) | C<sub>out</sub> |
|--------------|---|---|---------|-----------------|
| 0            | 0 | 0 | 0       | 0               |
| 0            | 0 | 1 | 1       | 0               |
| 0            | 1 | 0 | 1       | 0               |
| 0            | 1 | 1 | 0       | 1               |
| 1            | 0 | 0 | 1       | 0               |
| 1            | 0 | 1 | 0       | 1               |
| 1            | 1 | 0 | 0       | 1               |
| 1            | 1 | 1 | 1       | 1               |

> Simulate this adder using NAND gates:
[Full Adder NAND CircuitVerse Project](https://circuitverse.org/users/305021/projects/full-adder-nand-990621f6-993b-4676-a1b5-2a31aae451ce)

#### Your Task
Create a truth table for a **2-bit adder** without carry-in. What are the possible inputs and outputs?

| A<sub>1</sub> | B<sub>1</sub> | A<sub>0</sub> |B<sub>0</sub> | S<sub>1</sub> |S<sub>0</sub> |
|---------------|---------------|---------------|-------------|---------------|--------------|
| 0             | 0             | 0             | 0           | 0             | 0            |
| 0             | 0             | 0             | 1           | 0             | 1            |
| 0             | 0             | 1             | 0           | 0             | 1            |
| 0             | 0             | 1             | 1           | 0             | 0            |
| 0             | 1             | 0             | 0           | 1             | 0            |
| 0             | 1             | 0             | 1           | 1             | 1            |
| 0             | 1             | 1             | 0           | 1             | 1            |
| 0             | 1             | 1             | 1           | 1             | 0            |
| 1             | 0             | 0             | 0           | 1             | 0            |
| 1             | 0             | 0             | 1           | 1             | 1            |
| 1             | 0             | 1             | 0           | 1             | 1            |
| 1             | 0             | 1             | 1           | 1             | 0            |
| 1             | 1             | 0             | 0           | 0             | 0            |
| 1             | 1             | 0             | 1           | 0             | 1            |
| 1             | 1             | 1             | 0           | 0             | 1            |
| 1             | 1             | 1             | 1           | 0             | 0            |

---

### Task 3: Boolean Equations via Karnaugh Maps
Use the [K-Map method](https://github.com/STEMgraph/4b957490-badf-4264-b9f2-1b5aa370f36e) to derive Boolean equations for each output bit in your 2-bit adder.

1. Fill out Karnaugh Maps
2. Write down an equation for each cell marked `1`
3. Combine them using OR gates
4. Minimize the equations

<details>
<summary>The final functions</summary>

Q<sub>0</sub> = .......

Q<sub>1</sub> = .......

C<sub>out</sub> = .......

</details>

---

### Task 4: Circuit Implementation
Using your Boolean equations, build a logic network in [CircuitVerse](https://circuitverse.org) that implements at least one bit of the adder.

<details>
<summary>Your solution</summary>
A share link to your solution goes here: <a href=".................">Link!</a>
</details>

---

**Remember:** Stop working after 90 minutes and record where you stopped!


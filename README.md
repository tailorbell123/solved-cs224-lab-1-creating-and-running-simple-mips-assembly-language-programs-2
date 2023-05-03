Download Link: https://assignmentchef.com/product/solved-cs224-lab-1-creating-and-running-simple-mips-assembly-language-programs-2
<br>



<strong>Purpose</strong>: <strong>1</strong>. Introduction to MIPS assembly language programming and MARS environment. <strong>2</strong>. Learning CS224 lab rules and procedures.

You are obliged to read this document word by word and are responsible for the mistakes you make by not following the rules. Your programs should be reasonably documented and must have a neat syntax in terms of variable names and spacing. In all labs if it is not specified assume that inputs are always correct.

<strong>Part 1</strong> : array, palindrome, division without division instruction, code generation and defining some terms. (Due date of this part is the same for all groups).

<strong>Lab: (Study lab part at home and try to finish it before coming to the lab. Make sure that you show the lab work to your TA before uploading in the lab.)</strong>

<strong>Part 2</strong> : Using MARS with “hello world”.

<strong>Part 3</strong> : Using breakpoints, fixing errors in a Fibonacci programusing jal (jump and link) and jr (jump register) instructions.

<strong>Part 4</strong> : Implementing an arithmetic expression given in lab.

<strong>Part 5</strong>  Implementing a simple menu with loops.

<ol>

 <li>Please bring and drop your hardcopy (printed copy) of the preliminary work into the box(es) provided in the lab by 10:40 on Wednesday.</li>

</ol>

Please <strong>upload your programs of Part 1 (PRELIMINARY WORK)</strong> to the Unilica by 10:40 on Wednesday Use filename <strong>StudentID_FirstName_LastName_SecNo_PRELIM_LabNo.txt</strong> <u>Upload only the programs. Only a NOTEPAD FILE (txt file) is accepted. </u>Your paper submission for preliminary work must match MOSS submission. <u>Any format other than txt gets 0 points.</u>

<ol>

 <li>To get credit for preliminary work you have to submit its hard copy and upload its txt version to unilica.</li>

</ol>

You have to demonstrate your lab work to the TA for grade by <strong>12:15</strong> in the morning lab and by <strong>17:15</strong> in the afternoon lab. Your TAs may give further instructions on this. If you wait idly and show your work last minute, 20 points may be taken off from your grade.

At the conclusion of the demo for getting your grade, you will <strong>upload your entire program work</strong> to the Unilica Assignment, for similarity testing by MOSS. See Part 6 below for details.

<strong>Part 1. Preliminary Work / Preliminary Design Report</strong>

You have to provide a neat presentation prepared by <u>Word or a word processor with similar output quality such as latex</u>. At the top of the paper on left provide the following information and staple all papers. In this part provide the program listings with proper identification (please make sure that this info is there for proper grading of your work, otherwise some points will be taken off).

CS224

Section No.: Enter your section no. here

Lab No. 1

Your Full Name/Bilkent ID




<ol>

 <li><strong> Input an Array: </strong>Write a MIPS program that</li>

</ol>

Creates an array of maximum size of 20 elements that asks the user first the number of elements and then enters the elements one by one.

Displays array contents

Reverses the array contents and display the array (for example 1, 2, 3 becomes 3, 2, 1).




<ol start="2">

 <li><strong> Palindrome: </strong>Write a MIPS program that</li>

</ol>

Read an integer array as defined above and check if it is a palindrome. (For example, an array with four elements like 1, 4, 4, 1 is a palindrome: the order of the elements from the beginning to the end and from the end to the beginning are the same.




<ol start="3">

 <li><strong> Perform Division Without Division Instruction: </strong>Write a MIPS program that</li>

</ol>

Inputs two integer numbers n1 and n2 and performs integer division n1/n2 without using division instruction and display both the division and the remainder of the division.




<ol start="4">

 <li><strong> Object Code Generation: </strong>Generate the object code for the following instructions first in binary then give it in hex.</li>

</ol>

add        $t0, $t1, $t2

addi       $s0, $s3, 15

mult       $a0, $a1

sw          $t1, 8($t2)

lw           $t2, 8($t1)




<ol start="5">

 <li><strong> Define Terms: </strong>Define the following terms and provide an answer etc as described.</li>

 <li>Symbolic machine instruction: give two examples</li>

 <li>Machine instruction: give two examples and write their symbolic equivalents</li>

 <li>Assembler directive: give two examples.</li>

 <li>Pseudo instruction: give two examples and provide its implementation using real instructions.Note in your answer only use symbolic machine instructions.</li>

</ol>

<strong> </strong>

<strong>Part 2. Using MARS, a MIPS simulator    (15 points, A, B, C each part: 5 points)</strong>



<ol>

 <li><strong><u> Examine the controls and options in MARS</u></strong></li>

 <li>Open the MARS simulator. Take a few minutes to explore each of the windows (Edit &amp; Execute; MARS Messages &amp; Run I/O; Registers, Coproc 1 and Coproc 2). Look at each of the controls on the pull-down menus from the task bar at the top (File, Edit, Run, Settings, Tools, Help) and discuss what you think it does.  Change the run speed to 1 instuction/sec using the slide bar at the top.</li>

</ol>




<ol start="2">

 <li>Now, starting from the left, slowly put the mouse over each of the icons in the row across the top, to see the action that it will cause (but don’t click the icon). Determine which actions, represented by the icons, also can also be selected from a pull-down menu. Click the “?” icon (or choose it from the Help pull-down menu) and in the Help window that open, click each of the tabs and briefly look at the Help contents for that topic. Note that the MIPS tab offers a box with scroll bar, and 6 tabs of its own. Similarly, the MARS tab opens a window with 8 tabs. Be sure to look at each of these.</li>

</ol>




<ol start="3">

 <li>On the top menu, Tools offers a list of tools in the pull-down menu. Open each of these and look at it briefly to begin to understand the range of additional capabilities of MARS</li>

</ol>




<ol>

 <li><strong><u> Using a simple program in MARS</u></strong></li>

 <li>Load in Program1 (Generates “hello world”), using File &gt; Open, or the appropriate icon button. In the Edit window, examine this program, and learn what it does. Try to understand how it does it.</li>

</ol>




<ol start="5">

 <li>Assemble the program, using Run &gt; Assemble , or the appropriate icon button. In the Execute window, examine the code portion of memory (called Text Segment) and the data portion of memory (called the Data Segment). Note the beginning address of each, and the contents of each. Knowing that 2 hex characters represent one byte, and remembering  that ASCII characters are each coded as one byte,  determine which characters are stored in which locations in the Data Segment.  Examine the initial values of the registers—which ones are non-zero?  Make a note of their values. Read the messages in the MARS Messages window. Check the Run I/O window.</li>

</ol>




<ol start="6">

 <li>Set the Run Speed bar to 1 instruction/second. Now run the assembled program, using Run &gt; Go, or the appropriate icon button. What happens to the yellow highlight bar in the Text Segment during execution? What is written in the MARS Messages window? In the Run I/O window?  Compare the final values of the non-zero registers—did you expect to find $1, $4, and $2 changed by the program?  What is the final value of the $pc register?</li>

</ol>




<ol start="7">

 <li>Now edit the Program1 so that it produces a different output: Hello &lt;name of your TA&gt;   Choose one of the TAs names or the Tutor’s name, and make it print out that name. Then <u>call that TA or Tutor over to show your output</u>.</li>

</ol>




<ol>

 <li><strong><u> Finding and fixing errors in MARS</u></strong></li>

 <li>Load in Program2 (Conversion program), assemble it, and run it, providing the necessary input from the keyboard. What does this program do? Examine the MIPS assembly program to understand how it does it.</li>

</ol>




<ol start="9">

 <li>Edit the program by changing li $v0, 5 to li v0, 5 . Then assemble it and read the error message. Then fix the error and re-assemble it.</li>

</ol>




<ol start="10">

 <li>Edit the program by changing li $v0, 5 to $li v0 . Then assemble it and read the error message. Then fix the error and re-assemble it. Now run the program, at 1 instr/sec, and make note of the value of $v0 after the 2nd syscall is completed.</li>

</ol>




<ol start="11">

 <li>Edit the program by changing mul $t0, $v0, 9 to mul $t0, $t0, 9 . Then assemble it and run it, and explain why the output value is what it is. Then fix the error and re-assemble it and re-run it, to verify that Program2 again works correctly.</li>

</ol>




<ol start="12">

 <li>Change the Run speed back up to the maximum. Assemble the program, and instead of hitting the normal Run button, instead hit the “Run 1 step at a time” icon (looks like &gt;1) repeatedly, to single-step through the program. Notice that you can go slowly, examining the memory and registers after each step, or go quickly. This single-step mode is good for debugging. <u>Explain to the TA or Tutor</u> how you could use it to help find a logical error or typo error that accidently passed the assembler’s syntax check.</li>

</ol>




<strong>Part 3. </strong><strong><u>Using breakpoints in MARS, fixing logic errors and using jal and jr instructions </u></strong><strong>(20 points)</strong>




<ol>

 <li><strong><u> Fix the errors of the Fibonacci Program</u></strong></li>

</ol>

Load in Program3 (Fibonacci program), which says it is a fibonacci number finder, implemented using a loop (iteratively, not recursively).  The program has several errors, syntax and logical, that you must find and fix.  After getting it to assemble correctly, note that it runs, but gives the wrong value of fib(7), which should be 13.




To find and fix logical errors, you need to go through the code determining what the values are of the critical registers at the places in the program where they are changed.  In long programs, and especially programs with loops, it would take too long to single-step through the whole program. Instead, you must set breakpoints, and run up to those points and stop. Since the value of $v0 is where the fibonacci number is being accumulated in this program, you should set a breakpoint in the fib function wherever $v0 is changed. This way you can look at its value and determine if it is being caluclated correctly.  To set a breakpoint at an instruction, check the Bkpt box in the left-hand column next to the instructions you want to break at. Then hit Run.




[Hint: if you are not sure if the state of the machine at the breakpoint will include the effect of that instruction or not, you should experiment and learn by setting breakpoints in pairs, both at an instruction of interest, and after it, to see when the actual change in values takes place].




When you have the Program3 debugged and running correctly, <u>call the TA or Tutor to show</u> how breakpoints work, <u>and show that it calculates</u> any Fibonnacci number.




<ol>

 <li><strong><u> Extend the Fibonacci Program</u></strong></li>

</ol>

Extend the corrected Fibonacci program such that it gets a positive input integer number if it is an odd number like 7 it finds the corresponding 7th Fibonacci number, if it is an even number like 4 it finds the factorial of that number like 4!

<strong>Part 4. Using MIPS for mathematical calculations Program 4 (15 points)</strong>

Write a program that prompts the user for one or more integer input values, reads these values from the keyboard, and computes a mathematical formula such as (<strong><em>a different formula will be given on the board by the TA that includes all four operations and Mod</em></strong>):




X= (A * B + C  – D  ) Mod E




When the computation is finished, the program should print the result along with an explanatory comment to the user via the display.




<strong>Part 5. Using MIPS for implementing a program with a simple menu that involve loops Program 5 (20 points)</strong>

Create an array of maximum size of 100 elements. Ask the user to enter the number of elements and then the elements one by one. Perform the following operations by providing a menu (no GUI just comment based menu) to the user.  Implement the following in the form of separate subprograms. The use of $s registers is optional

<ol>

 <li>Find summation of numbers stored in the array which is less than an input number.</li>

 <li>Find summation of numbers out of a value range specified by two numbers and display that value.</li>

 <li>Display the number of occurrences of the array elements divisible by a certain input number.</li>

 <li></li>

</ol>

<strong>Optional</strong>: Use syscall with 9 in $v0 for dynamic storage allocation for the array.



Download Link: https://assignmentchef.com/product/solved-cse12-assignment-1
<br>
Problem #0

First read and sign the Integrity of Scholarship agreement for CSE 12 here:

Problem #1

The purpose of this problem is to get you more comfortable on the command line. For parts A and B, you may use any program you like to edit your java files (e.g., Dr. Java, vim, or even Eclipse), but we would like you to compile the program, run some junit tests, and generate Javadocs via the command line.

Download following Files from the Class Website and save them to your HW1 directory:

Counter.java

CounterTest.java

Counter.pdf

HW1-Answers.txt

<strong>A.</strong>​ Look at the file Counter.pdf. This is a PDF of documentation created using javadoc. Using whatever editor you like (vim, Dr. Java, or even Eclipse), modify Counter.java with appropriate javadoc comments, so that it generates <u>similar </u><u>​         </u>​documentation.    Replace the author field with your name.  By similar, we are not asking for exact wording, but ALL methods must be documented using javadoc

Next generate the javadocs for this file via the command line, and place all of the documentation files in a subdirectory called doc in your HW1 directory.  If you do not know how to do this, and don’t know where to start, try Googling “javadoc command line” (without the quotes).  I recommend skipping the StackOverflow link and going to the official Java page.  The section on “options” will be particularly useful.

You need to get comfortable with reading documentation to find out information for yourself.

Any piazza posts in the vein of “how to do create javadoc…” will be removed by

TAs/Tutors/Staff.  It’s a skill to read documentation on the web, and sorting out when you see conflicting “information.”

Look at the generated Counter.html file to be sure it was generated appropriately, and matches what is in Counter.pdf (with your name as the author).  When you turn in Counter.java, we will run javadoc on your file to create the required documentation.




In addition, place the following information in your HW1-Answers.pdf file

<ul>

 <li>What command line is used to create the javadoc documentation in HW1/doc?</li>

 <li>What command-line flag is used to to create the author and version entries for the class</li>

</ul>

<ol>

 <li>​Download the File CounterTest.java file. Most of the file is already complete, and you should be able to compile and run it.   However, there are some ‘TODO:’  marked in comments where you are to complete the code. These completions including adding comments at the top of the file and completing the code to properly run some of the unit tests against the Counter class defined in part A.   When you run the unit tests, they should be <u>​meaningful </u>​tests and print out the following when running from the command prompt. A meaningful test is something that will verifies a particular input/output.</li>

</ol>




.Checking Default Counter Value is Zero

.Checking Proper Increment

.Checking Multiple Increments

.Checking Reset

.Checking Decrement

Time: 0.002

OK (5 tests)

<ol>

 <li>The following are 4 possible ways to run the testing code from the command line, some work, some do not. ​<strong>Note: this is JUnit 3, not JUnit 4</strong>​.  In your HW1-Answers file tell us if the command line properly runs the code. If it does not run the code, briefly describe why.  Feel free to use Google and any other internet site that helps you understand why some of these work and some of these fail.

  <ol start="4">

   <li>java -cp ‘.:/usr/share/java/junit4.jar’ junit.runner.JUnitCore CounterTest</li>

   <li>java -cp ‘.:/usr/share/java/*’ junit.runner.JUnitCore CounterTest</li>

   <li>java -cp ‘.:/usr/share/java’ junit.runner.JUnitCore CounterTest</li>

   <li>java -cp ‘.:/usr/share/java/junit4.jar’ JUnitCore CounterTest</li>

   <li>java -cp ‘.:/usr/share/java/junit.jar’ JUnitCore CounterTest</li>

  </ol></li>

</ol>

<ol start="2">

 <li>Modify Counter.java so that your <u>​Reset test fails</u>​. ​<strong>The version  of Counter.java that does not pass  Reset test is the version you should turn in</strong>​. To be clear.</li>

</ol>

Counter.java must ​<em>compile</em>​ but it should fail a reasonable Reset test.  We will run your tests against an error-free version of Counter.java to insure that all tests pass. Then we will run your tests against your turned in version of Counter.java to see the failed Reset test.

In addition, place the following information in your HW1-Answers.pdf file.  Again, feel free to look up these answers using Google or any other web resource.

<ul>

 <li>-cp and -classpath are “command-line switches” to the java and javac command to set</li>

</ul>

Java’s classpath. What is another way to set the classpath without using a command-line switch? (hint: read

http://docs.oracle.com/javase/tutorial/essential/environment/paths.html)

<h1>Problem #2</h1>

Create two java programs called ReverseArray.java and ReverseList.java. These programs are to provide the identical functionality, but using different implementations.

<ul>

 <li>Read a file of text ​<em>once, </em>​line-by-line. Read each line of the file as a java String. The name of the file is specified as a command line argument.</li>

 <li>Print the file to ​<u>standard output</u><u>​</u> in reverse line order. That is, the last line of the file is printed first, next-to-last is printed next, and finally the first line is printed last (you do not reverse the text on each line)</li>

 <li>If the file does not exist, print “​<em><u>File Not Found” to standard error</u></em>​ (it should use java Exception handling in a correct try..catch block.  Nothing should be written to standard out in this case</li>

 <li>If a file is not supplied on the command line print a “usage” statement to standard error (Nothing should be printed to standard out)</li>

 <li>Your programs should generate no exceptions under (almost) any circumstances. Try to break with bad input. One type of input we will NOT test is giving your programs non-text files (also known as “binary files”).  You do not need to check if a file is a text file.</li>

</ul>

If a file called manywords.txt exists, then to print the lines in reverse order, one would give the unix command

$ java ReverseArray manywords.txt

OR

$ java ReverseList manywords.txt

You can download two example files and outputs from the assignment folder

<ul>

 <li>txt, this is a 5 line text-based input file</li>

 <li>rev.txt, this is what the reversed output should look like</li>

 <li>txt, this is a text version of the US Declaration of Independence ● declaration.rev.txt this is the reversed version of the declaration. txt file</li>

</ul>

$ java ReverseList short.txt

(this should give you the identical file in short.txt.rev)

$ java ReverseList declaration.txt

(this should give you the identical file as declaration.rev.txt)

$ java ReverseList

usage: ReverseList &lt;filename&gt;

(the program prints this when no file is given)

you should test your program output for both ReverseList and ReverseArray

<strong><em>Using commands to validate your output is identical to the sample outputs. </em></strong>

In this course, you should become familiar with some unix command-line tools to validate that your code is doing what it should do.

<ol>

 <li>Capturing standard output (stdout) of a program and saving to a file using the “&gt;” (redirection) operator of the bash shell.</li>

</ol>

First run your program and capture its output to a file.

$ java ReverseList declaration.txt &gt; myoutput.txt

(this runs the java program ReverseList and puts the output in the file named “myoutput.txt”)

<ol start="2">

 <li>Then, use the ​diff​ command to highlight any differences.</li>

</ol>

$ diff declaration.rev.txt myoutput.xt

(if there are no differences, then the diff command will not produce any output. That’s what you want! If there are differences, diff will print out where it finds the problem. Any difference (even if you add a space at the beginning of a line, or an extra line at the end of your output) is notated by diff




You can also view differences side-by-side, in the vi editor)

$ vimdiff declaration.rev.txt myoutput.txt

(This will open the vi editor and highlight the differences, if any)

<ol>

 <li>Look up how to</li>

 <li>Redirect standard error (stderr) to a file in the bash shell</li>

 <li>Redirect stdout and stderr to the same file in the bash shell</li>

</ol>

<u>Specifics and Hints:</u>

<em>Program organization: </em>​You will write the code in the main method of each class, though you might choose to implement helper methods to make the code simpler.  When you create helper methods, make sure they are also declared as static.

In HW1-answers.pdf answer the following

<ul>

 <li>Why must the main method of java program be declared ​static</li>

</ul>

<em>How are ReverseArray and ReverseList different?</em>​   ReverseArray is implemented using an Array of Strings to store the file contents before printing (You may NOT use the ArrayList class or similar to implement ReverseArray, you MUST use normal arrays).   ReverseList is implemented using a LinkedList of String type (i.e. LinkedList&lt;String&gt;) from the Java Collections Framework.   We will be talking about Linked Lists and the Java Collections Framework in more detail in the next week or two, but for now we want you to use the documentation in the Javadocs API to figure out how to create and work with objects of type LinkedList&lt;String&gt;.

<em>Implementation details for ReverseArray:</em>​  You should initially create an array that can reference 100 Strings.  If your file is longer than 100 lines (it WILL be when graded, so test this yourself!), when your program would read the 101st line, there isn’t space to store it before printing. This should NOT cause an exception. Instead, create a new array of Strings with the ability to reference 200 Strings, copy the references from the old array into the new array and then continue reading.  If file is longer than 200 lines, extend again by 100 slots in the array of Strings.

Commenting/Javadoc

<ol>

 <li>Your ReverseList and ReverseArray programs must be commented in javadoc style.</li>

 <li>Your code MUST BE INDENTED properly. You may use either spaces or tabs to indent your code, but please be consistent.   If you use spaces, use at least 4 spaces to indent.</li>

 <li>Other comments in your code are at your discretion. You should comment code if the comment aids in understanding how the code works. Too many comments is as bad as too few.  In general, a short comment at the beginning of a block of code is all that is warranted. For example, you might comment a block of code with</li>

</ol>

<h2>// Read file line-by-line and store in auto-expanding array</h2>

<ol start="4">

 <li>If we have not given hard and fast “rules” on how something should be done in your program/code, you aren’t going to lose points for coding one way or another. There is more than one solution to any programming problem.</li>

</ol>




<h1>Problem #3</h1>

True/False.   Create a text file (using a unix text editor like vi, or using a program like Microsoft Word and saving your file as a plain text (txt) file) called ​<strong>Problem3.txt </strong>​and create answers with the number of the question followed by either the word True or False. One answer/line.  eg.

<ol>

 <li>True</li>

 <li>False</li>

</ol>

and so on.  This allows us to grade this part electronically.

This part is open book and open notes.  You may use Google to help you determine the answers to these questions, and you may run any Java code to help you determine the answers.  However, you may not ask your classmates for the answers nor may you give the answers to any of your classmates.  The point is to ​<em>understand</em>​ the answers, as we assume that you have this knowledge from CSE 11 or CSE 8B and we will build on it.

<table width="631">

 <tbody>

  <tr>

   <td width="26">1.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">An instance variable declared as private can be seen  only by the class in which it was declared and all its sub classes</td>

  </tr>

  <tr>

   <td width="26">2.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">If a class C is declared as abstract, then  private C myC = new C();  is valid.</td>

  </tr>

 </tbody>

</table>




<table width="631">

 <tbody>

  <tr>

   <td width="26">3.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">A variable declared as static cannot ever be modified, once  it has been declared and initialized.</td>

  </tr>

  <tr>

   <td width="26">4.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">The following is a legal statement:  double x = 5;</td>

  </tr>

  <tr>

   <td width="26">5.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">Code that does not explicitly handle checked exceptions, results in a compilation error.</td>

  </tr>

  <tr>

   <td width="26">6.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">The declaration FilledOval[][] A = new FilledOval[20][30];  creates 600 FilledOval instances using the FilledOval() constuctor.</td>

  </tr>

  <tr>

   <td width="26">7.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">A  class that uses the Swing toolkit and wants to both display and be notified of changes to a JSlider must implement the ActionListener interface.</td>

  </tr>

  <tr>

   <td width="26">8.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">method declarations void A(double x, integer k){};  and void A(integer k, double x) {}; have identical signatures</td>

  </tr>

  <tr>

   <td width="26">9.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">The binary search algorithm  will work properly on all integer arrays.</td>

  </tr>

  <tr>

   <td width="26">10.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">if X is any valid, defined java object, then Object tmp=X; is a valid statement.</td>

  </tr>

  <tr>

   <td width="26">11.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">(“Give me Liberty”.split(“ “).length)​ evaluates to 3</td>

  </tr>

  <tr>

   <td width="26">12.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">“”.format(“%d %s
”,14, “shopping days left”);​ is a valid statementt.</td>

  </tr>

  <tr>

   <td width="26">13.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">If the following statements are the only two statements in a method,String X = “thing one”;  and String Y = ”thing one”; thenX.equals(Y) evaluates to  true, but X == Y evaluates to false within that method.</td>

  </tr>

  <tr>

   <td width="26">14.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">A class declared as final cannot be inherited via the extends keyword.</td>

  </tr>

  <tr>

   <td width="26">15.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">consider the statement: String S = “Out of Gas”;  then the statement: S[7] = ‘g’;  will change “Gas” to “gas”.</td>

  </tr>

  <tr>

   <td width="26">16.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">boolean primitive variables can only be assigned values: true, false, or null.</td>

  </tr>

  <tr>

   <td width="26">17.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">You can index into an array with a variable of type double as long as the there are no digits past the decimal point.</td>

  </tr>

  <tr>

   <td width="26">18.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">The constructor of the super class is only called when the constructor of  the sub class explicitly calls super(); as its first line.</td>

  </tr>

  <tr>

   <td width="26">19.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">Any for loop can be rewritten using a while loop.</td>

  </tr>

  <tr>

   <td width="26">20.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">It is legal to define more than one class in a java source file.</td>

  </tr>

  <tr>

   <td width="26">21.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">A class can implement multiple interfaces</td>

  </tr>

  <tr>

   <td width="26">22.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">int i =  Math.sqrt(4.0);​  is a valid statement.</td>

  </tr>

  <tr>

   <td width="26">23.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">the ​protected ​keyword can only be applied to instance variables.</td>

  </tr>

  <tr>

   <td width="26">24.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">Consider the statement:  ​throw new IllegalArgumentException(); This always causes the program to immediately exit.</td>

  </tr>

  <tr>

   <td width="26">25.</td>

   <td width="19">T</td>

   <td width="24">F</td>

   <td width="562">Suppose  you have the following declaration: ​int xyz = 4;​ Then, in the body of a  switch statement block</td>

  </tr>

  <tr>

   <td width="26"> </td>

   <td width="19"> </td>

   <td width="24"> </td>

   <td width="562">case xyz: System.out.println(“4”); break;  ​ is legal.</td>

  </tr>

 </tbody>

</table>






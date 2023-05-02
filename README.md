Download Link: https://assignmentchef.com/product/solved-comp9313-assignment-1-mapreduce
<br>
<span style="font-size: 2.61792em; letter-spacing: -1px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Problem Statement</span>




Given a set of text documents (i.e. text files) in input, create an index with the list of <em>ngrams</em> (e.g.

bigrams) contained in these documents along with the number of times the ngrams were found across all documents and the list of files where the ngrams appear.




<h1>Input</h1>

<strong> </strong>

The list of files is provided in a directory (you can have an arbitrary number of files and file names), for example:




/tmp/input/

file01.txt              file02.txt              file03.txt

…




The directory must be in your local file system (we will not use HDFS for this assignment). We provide a set of sample files here:

<a href="https://webcms3.cse.unsw.edu.au/COMP9313/19T2/resources/28190">https://webcms3.cse.unsw.edu.au/COMP9313/19T2/resources/28190</a>




<h1>Output</h1>




The output consists in a file that contains the list of <em>ngrams</em> (e.g. bigrams) identified in the documents in input, along with the number of times the <em>ngram</em> was found across all documents and the list of files where the ngrams where found. For example:




a collection  1  file01.txt a network   1  file01.txt a part     1  file03.txt hadoop is   2  file01.txt file03.txt …




In the example above, the <em>bigram</em> hadoop is was found 2 times in total, and it was found in files file01.txt and file03.txt.




<h1>Program Arguments</h1>

Your Java program <em>must</em> receive 4 arguments:




<table width="600">

 <tbody>

  <tr>

   <td width="144">            <strong><em>args[0]</em>:</strong></td>

   <td width="456">The value <em>N </em>for the ngram. For example, if the user is interested only in  bigrams, then <em>args[0]=2</em>.</td>

  </tr>

  <tr>

   <td width="144">            <strong><em>args[1]</em>:</strong></td>

   <td width="456">The minimum count for an ngram to be included in the outputfile. For example, if the user is interested only in ngrams that appear at least  10 times across the whole set of documents, then <em>args[1]=10</em>.</td>

  </tr>

  <tr>

   <td width="144">            <strong><em>args[2]</em>:</strong></td>

   <td width="456">The directory containing the files in input. For example, <em>args[2]=”/tmp/input/” </em></td>

  </tr>

  <tr>

   <td width="144">            <strong><em>args[3]</em>:</strong></td>

   <td width="456">The directory where the output file will be stored. For example,</td>

  </tr>

 </tbody>

</table>

<em>args[3]=”/tmp/output/” </em>




Notice that the order of the arguments above is important. When we test your code, we will assume that the arguments are in the right order, as explained above.




<h1>Building your Program</h1>




Your program will be built using <em>Apache Maven</em>, and we assume that the <em>only</em> dependency to be used in your project is<em> hadoop-core, version 1.2.1</em> (do not add and/or rely on other dependencies in your project). In the link below, we provide a Maven project template that you should use for developing your solution:




<a href="https://webcms3.cse.unsw.edu.au/COMP9313/19T2/resources/28189">https://webcms3.cse.unsw.edu.au/COMP9313/19T2/resources/28189</a>




Your code must be included (in its entirety) in the file Assignment1.java. If you use multiple Java classes in your solution, all these classes must be entirely defined within the file Assignment1.java. You must ensure that the code you submit can be compiled and packaged using Apache Maven (we recommend you use the project template provided above). Any solution that has compilation errors will receive no more than 5 points for the entire assignment.

<strong> </strong>

<h1>Assignment Submission</h1>

<strong> </strong>

<strong><em>Deadline:</em></strong> 05 July 2019 20:59:59




Log in to any CSE server (e.g. williams or wagner) and use the <em>give command</em> below to submit your solution:




$ give cs9313 assignment1 z9999999.zip




where you must replace z9999999 above with your own zID. The zip file above must contain the following:

<ul>

 <li>The file Assignment1.java containing your Java code</li>

 <li>A PDF document (maximum 1 page, 10 points font-size Arial) that explains your solution (use of figures is highly encouraged to explain your solution).</li>

</ul>




You can also submit your solution using WebCMS, or Give: <a href="https://cgi.cse.unsw.edu.au/~give/Student/give.php">https://cgi.cse.unsw.edu.au/~give/Student/give.php</a>




If you submit your assignment more than once, the last submission will replace the previous one. To prove successful submission, please take a screenshot and keep it for your own record. If you face any problem while submitting your code, please e-mail the Course Admin (Maisie Badami, <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="c1acefa3a0a5a0aca881b2b5b4a5a4afb5efb4afb2b6efa4a5b4efa0b4">[email protected]</a>)




<strong>Late submission penalty </strong>

<strong> </strong>

10% reduction of your marks for the 1st day, 30% reduction/day for the following days.

<strong> </strong>

<h1>Assessment</h1>




Your source code will be manually inspected and marked based on readability and ease of understanding. We will run your code to verify that it produces correct results. The code documentation (i.e. comments in your source code) and solution explanation (PDF document) are also important. Below, we provide an indicative assessment scheme (maximum mark: 25 points):




<table width="350">

 <tbody>

  <tr>

   <td width="225">Result correctness</td>

   <td width="125">15 points</td>

  </tr>

  <tr>

   <td width="225">Documentation (PDF document)</td>

   <td width="125">5 points</td>

  </tr>

  <tr>

   <td width="225">Code structure and source code documentation (comments)</td>

   <td width="125">5 points</td>

  </tr>

 </tbody>

</table>






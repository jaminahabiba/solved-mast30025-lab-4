Download Link: https://assignmentchef.com/product/solved-mast30025-lab-4
<br>
We model an individual’s income at age 30 against the number of years of formal education with a linear model. The following data is collected:

Years of formal education (<em>x</em>)        Income ($k) (<em>y</em>)

8                                                     8

12                                                  15

14                                                  16

16                                                  20

16                                                  25

20                                                  40

Where possible, solve the following questions in two ways: using matrix calculations as detailed in the lectures, and using the lm command in R.

<ol>

 <li>Plot the data; is a linear model appropriate?</li>

 <li>Write down the linear model in matrix form.</li>

 <li>Find the normal equations for this model.</li>

 <li>Solve the normal equations to obtain the least squares estimates of the parameters. Add the fittedregression line to your plot (using curve for example).</li>

 <li>This model is a simple linear regression model. Use the standard linear regression formulae,</li>

</ol>

to estimate the parameters again (where the bar indicates the mean). Check that you have the same answers as above.

<ol start="6">

 <li>Calculate the sample variance <em>s</em><sup>2</sup>.</li>

 <li>Estimate the average income of a person who has had 18 years of formal education.</li>

 <li>Calculate the standardised residuals, leverage, and Cook’s distance for the first observation. Youmay need the R functions rstandard, influence, and distance.</li>

</ol>

Check your numbers against the diagnostic plots produced by R.

<ol start="9">

 <li>We know that the least squares estimator <strong>b </strong>is an unbiased estimator for <em>β</em>. Show that <strong>t</strong><em><sup>T</sup></em><strong>b </strong>is an unbiased estimator for <strong>t</strong><em><sup>T</sup></em><em>β</em>, where <strong>t </strong>is a vector of constants.</li>

</ol>

<h1>R exercises</h1>

Read Sections 5.1–5.3 of spuRs, then attempt the exercises below.

<ol>

 <li>The (Euclidean) length of a vector <em>v </em>= (<em>a</em><sub>0</sub><em>,…,a<sub>k</sub></em>) is the square root of the sum of squares of its coordinates, that is. Write a function that returns the length of a vector.</li>

 <li>Last week you wrote a program to calculate <em>h</em>(<em>x,n</em>), the sum of a finite geometric series. Turn this program into a <em>function </em>that takes two arguments, <em>x </em>and <em>n</em>, and returns <em>h</em>(<em>x,n</em>).</li>

</ol>

Make sure you deal with the case <em>x </em>= 1.

<ol start="3">

 <li>In this question we simulate the rolling of a die. To do this we use the function runif(1), which returns a ‘random’ number in the range (0,1). To get a random integer in the range {1<em>,</em>2<em>,</em>3<em>,</em>4<em>,</em>5<em>,</em>6}, we use ceiling(6*runif(1)), or if you prefer, sample(1:6,size=1) will do the same job.</li>

</ol>

1

<ul>

 <li>Suppose that you are playing the gambling game of the Chevalier de M´er´e. That is, you arebetting that you get at least one six in four throws of a die. Write a program that simulates one round of this game and prints out whether you win or lose.</li>

</ul>

Check that your program can produce a different result each time you run it.

<ul>

 <li>Turn the program that you wrote in part (a) into a function sixes, which returns TRUE if you obtain at least one six in <em>n </em>rolls of a fair die, and returns FALSE That is, the argument is the number of rolls <em>n</em>, and the value returned is TRUE if you get at least one six and FALSE otherwise.</li>

</ul>

How would you give <em>n </em>the default value of 4?

<ul>

 <li>Now write a program that uses your function sixes from part (b), to simulate <em>N </em>plays of the game (each time you bet that you get at least one six in <em>n </em>rolls of a fair die). Your program should then determine the proportion of times you win the bet. This proportion is an estimate of the <em>probability </em>of getting at least one six in <em>n </em>rolls of a fair die.</li>

</ul>

Run the program for <em>n </em>= 4 and <em>N </em>= 100, 1000, and 10000, conducting several runs for each <em>N </em>value. How does the <em>variability </em>of your results depend on <em>N</em>?

The probability of getting no 6’s in <em>n </em>rolls of a fair die is (5<em>/</em>6)<em><sup>n</sup></em>, so the probability of getting at least one is 1 − (5<em>/</em>6)<em><sup>n</sup></em>. Modify your program so that it calculates the theoretical probability as well as the simulation estimate and prints the difference between them. How does the <em>accuracy </em>of your results depend on <em>N</em>?

<ul>

 <li>In part (c), instead of processing the simulated runs as we go, suppose we first store the resultsof every game in a file, then later postprocess the results. You should read spuRs Chapter 4 to see how to read and write text files.</li>

</ul>

Write a program to write the result of all <em>N </em>runs to a textfile sixes_sim.txt, with the result of each run on a separate line. For example, the first few lines of the textfile could look like

TRUE

FALSE

FALSE TRUE FALSE

. .

Now write another program to read the textfile sixes_sim.txt and again determine the proportion of bets won.

This method of saving simulation results to a file is particularly important when each simulation takes a very long time (hours or days), in which case it is good to have a record of your results in case of a system crash.



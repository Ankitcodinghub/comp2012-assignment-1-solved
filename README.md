# comp2012-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [COMP2012 Assignment 1 Solved](https://www.ankitcodinghub.com/product/comp2012-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124244&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COMP2012 Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
The coefficient for the third term is -7, and its exponent is 0. Note that we always omit the variable instead of writing “x^0” for exponent 0.

We will be using a linked list to store the polynomial. The struct we use is defined within the Polynomial class in polynomial.h as follows:

struct Term {

int coefficient; int exponent;

Term* next;

} * head; //linked list of terms, nodes are always sorted by exponen

It has the following properties:

A node represents a term in the polynomial. We also always keep the linked list sorted so that terms with larger exponents will appear earlier in the list than the other terms with smaller exponents.

Nodes/terms with 0 coefficient will NOT be stored.

No two nodes/terms should have the same exponent.

The head should point to nullptr when the polynomial is simply zero “0” (instead of having 1 term of exponent 0 and coefficient 0).

We also assume the following for this assignment:

We deal with single-variable polynomials only, and that variable is always named “x”. Exponents are integers in the range [0, 2047], but coefficients can be any positive and negative integer.

When the coefficient is/becomes 0, we consider the term non-existent, and we won’t store/print that term.

For example, if we add “3*x^2 + 1” to “-3*x^2 + 7”, the result would be simply “8” (i.e. 1 node/term in the resulting linked list) instead of “0*x^2 + 8” (2 nodes/terms).

For simply zero which is represented by an empty linked list (head points to nullptr), we print “0” even though the linked list has nothing in it.

To illustrate, the linked list for the example polynomial “2*x^3 + 6*x – 7” looks like this:

With all the specifications above, there will only be one unique linked list and string representation for any polynomial.

If you need further clarifications of the requirements, please feel free to post on the Piazza (via Canvas) with the pa1 tag. However, to avoid cluttering the forum with repeated/trivial questions, please do read all the given code, webpage description, sample output, and latest FAQ (refresh this page regularly) carefully before posting your questions. Also, please be reminded that we won’t debug for any student’s assignment for the sake of fairness.

Download

Skeleton code: skeleton.zip

The Polynomial Class

A Polynomial object represents a single-variable polynomial as specified in the introduction section. It supports various simple operations such as addition and multiplication which are usable via member functions that will be implemented by you. You should also read the main.cpp and sample output for test cases of the member functions to help yourself understand what exactly each of them does.

For simplicity, you can assume all input parameters are valid.

Data member

Term* head

It points to the head node of the linked list that stores the polynomial. Please read the introduction section for a detailed description of the linked list.

Member functions

Polynomial add(const Polynomial&amp; another) const

Polynomial subtract(const Polynomial&amp; another) const

Polynomial multiply(const Polynomial&amp; another) const

int evaluate(int valueOfX) const

Calculate the value of the polynomial when the variable “x” has the specified value of x. Refer to the given test cases for examples.

int compare(const Polynomial&amp; another) const

Return 1 if this polynomial is larger than another, or return -1 if this polynomial is smaller, or return 0 if both are the same. The polynomial comparison for two polynomials p1 and p2 is defined as follows:

The two polynomials are compared term by term. We always start with the first terms of both, and move to the later terms for both polynomials at the same time. Then first we should see if the “current terms” exist for both polynomials because they can have differnet numbers of terms.

If “current terms” exist for both polynomial, we can compare them as follows. If the exponent of the current term of p1 is larger than that of p2, p1 is considered as larger. The reverse is also true.

If the exponents are the same, we compare their coefficients instead. That is, if the coefficient of the current term of p1 is larger than that of p2, p1 is considered as larger. The reverse is also true.

If both their exponents and coefficients are the same, we cannot decide yet, so we proceed to the next terms for both polynomials (i.e. p1’s 2nd term vs p2’s 2nd term, then p1’s 3rd term vs p2’s 3rd term, and so on) until there is no more later term for one of the polynomials.

If there is no more term for one of the polynomials only, then the longer polynomial is considered as larger.

If there is no more term for both polynomials at the same time, that implies the two polynomials have the same number of terms (and they have the very same terms really), then we consider they are the same.

Refer to the given test cases for examples.

Optional task to think about

The following constructor is optional and will NOT be graded. It is not even given in the header file. If you want to have extra practices, you can add this constructor yourself after you have finished and submitted your assignment.

Polynomial(const char s[])

This constructs the polynomial according to the given C-string that stores the string representation of the polynomial. Since this task is optional and will NOT be graded, you are free to use anything you want. Please do NOT include this in your solution submitted for assignment 1.

Sample Output and Grading Scheme

There are 22 given test cases of which the code can be found in the given main function.

These 22 test cases are first run without any memory leak checking (they are numbered #1 #22 on ZINC). Then, the same 22 test cases will be run again, in the same order, with memory leak checking (those will be numbered #23 – #44 on ZINC). For example, test case #30 on ZINC is actually the given test case 8 (in the given main function) run with memory leak checking.

About memory leak and other potential errors

Here is a summary of the test cases for your information.

Please submit one cpp file only: polynomial.cpp. Submit the file to ZINC. ZINC usage instructions can be found here.

Notes:

In the grading report, pay attention to various errors reported. For example, under the “make” section, if you see a red cross, click on the STDERR tab to see the compilation errors. You must fix those before you can see any program output for the test cases below.

Make sure you submit the correct file yourself. You can download your own file back from ZINC to verify. Again, we only grade what you uploaded last to ZINC.

Compilation Requirement

It is required that your submissions can be compiled and run successfully in our online autograder ZINC. If we cannot even compile your work, it won’t be graded. Therefore, for parts that you cannot finish, just put in dummy implementation so that your whole program can be compiled for ZINC to grade the other parts that you have done. Empty implementations can be like:

In this particular PA, it is probably related to misuse of dynamic memory. Good luck with bug hunting!

Q: For the print function, should coefficient 1 or -1 be printed? That is, should it be “-1*x” or “-x” for a term with coefficient -1 and exponent 1?

A: No, as you can see in the sample output (test case #3). “-x” should be printed. However, if the exponent is 0, then the term should be printed, e.g. “1”, “-1”, “x^2 + 1”, “x^2 – 1”, etc.

Q: For the print function, if the first term has a negative coefficient, should we be adding a space between the negative sign and the coefficient? That is, should it be “- 90*x^2” or “-90*x^2”? Should it be “- x” or “-x”?

A: No, as you can see in the sample output (test case #3). “-90*x^2” and “-x” should be printed.

Q: For the first example of the array constructor, should the result be “5*x^2 – 6*x + 7” since the exponent 1 shouldn’t be printed?

Q: Are “x” or “x – 5” larger?

A: “x – 5” is larger according to our description which states that when we reach a term in p1 but not in p2, p1 is considered as larger. Note that polynomial “x” must be represented by a linked list of 1 node/term (0s are never stored), so “x – 5” having the very same first term and an additional second term is considered as larger.

(Fixed a typo in this FAQ at 9 19am Mar 16, bolded: “x – 5” is definitely larger.)

Q: Will we be asked to print or operator on a polynomial with some nodes/terms that have 0 coefficients?

A: You can assume the polynomials given by us are always valid in all test case, meaning they follow the specifications we stated including “nodes/terms with 0 coefficient will NOT be stored.”.

Q: Can one of the operands be “0”? What is the result of multiplication with “0”?

A: Yes, in that case, the polynomial will have its head point to nullptr as we described. An empty linked list represents a valid polynomial “0” which can be printed as described. The result of multiplication with “0” (which is represented by a polynomial with an empty linked list) is “0” (which is represented by a polynomial with an empty linked list).

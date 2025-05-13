# ppl212-homework-3-solved
**TO GET THIS SOLUTION VISIT:** [PPL212 Homework 3 Solved](https://www.ankitcodinghub.com/product/ppl212-homework-3-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92021&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;PPL212 Homework 3 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 0px;">
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
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 2">
<div class="section">
<div class="layoutArea">
<div class="column">
Part I: Theoretical Questions

<ol>
<li>Is let in L3 a special form? Justify your answer.</li>
<li>In L3, what is the role of the function valueToLitExp?</li>
<li>The valueToLitExp function is not needed in the normal evaluation strategy
interpreter (L3-normal.ts). Why?
</li>
<li>The valueToLitExp function is not needed in the environment-model interpreter.
Why?
</li>
<li>What are the reasons that would justify switching from applicative order to normal order
evaluation? Give an example.
</li>
<li>What are the reasons that would justify switching from normal order to applicative order
evaluation? Give an example.
</li>
<li>In general, and as seen in class, substitution requires renaming. However, when the
term that is substituted is “closed” (i.e., it does not contain free variables) then no renaming is required and naive substitution is correct.

<ol>
<li>Prove it.</li>
<li>Write evaluation rules for naive substitution</li>
</ol>
</li>
<li>Draw an environment diagram for the following computation. Make sure to include the
lexical block markers, the control links and the returned values.

<pre>     (define a 2)
     (define goo
</pre>
<pre>      (lambda (x)
        (lambda (y)
</pre>
<pre>          (/ x y))))
     (define foo
</pre>
<pre>      (letrec
          ((f (goo a))
</pre>
<pre>           (g (lambda (x) (f x))))
        (lambda (x)
</pre>
(if (= x 0) x

<pre>              (g x)))))
     (foo (foo 0))
</pre>
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="section">
<div class="layoutArea">
<div class="column">
Part II: Value Store

In this part, you are given most of the implementation of the programming language L2.1. This language has almost the same syntax as the L2 language taught in class. The main difference is in the choice of evaluation model: it implements the Environment Model (L2 was implemented using the Substitution Model).

You are asked to change the implementation of the environment of L2.1 with two main features:

<ol>
<li>1. Add a set! expression support</li>
<li>2. Implement the mutation using a Value Store.</li>
</ol>
The Value Store

The value store plays the part of the heap in the execution: it is allocated dynamically during the execution and holds the actual value. The environment will now contain only the names of the variables and addresses of the value in the value store. The store is a partial function from these addresses to the values. Mutations occur only at the store. To do that, the value store will be implemented as an array of Box&lt;Value&gt; type.

Impact on the Evaluation

Store API

Functions for managing the store need to be added: makeStore, extendStore, applyStore.

Allocating Memory

The store needs to be extended whenever memory needs to be allocated. You need to figure out where, during the evaluation, this should be done.

Applying Environment

Since the environment holds only pointers to the store, and the actual values reside in the store, the process of fetching the values needs to be changed.

What to do

<ul>
<li>● Add set! to the syntax</li>
<li>● Complete the Store api</li>
<li>● Think when the store needs to be extended, and modify the code accordingly</li>
<li>● Pay attention to the global environment and define expressions</li>
<li>● Pay attention to closures and the environment they hold</li>
<li>● Make sure all the tests run
בהצלח
</li>
</ul>
</div>
</div>
</div>
</div>

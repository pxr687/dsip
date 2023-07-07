# "Data Science and Machine Learning in Practice" module notes
* Module will be taught from 2nd Oct 2023 and runs for 9 weeks
* Everyone  on the module will know up to: multiple linear regression, 
k-nearest neighbours, single-predictor logistic regression
* Two 1.5 hour sessions per week, one 2 hour online lab per week.

# Module rubric

> You have already studied the foundations of data science in Quant 1B.
> This module follows on from those modules, but with a focus on real-world 
> applications of data science, working in teams to make useful, extensible and 
> reproducible data science analyses and reports on a wide variety of data, 
> including data from databases, big data, spatial data such as weather and 
> climate data, data from public services and data scraped from web pages and 
> other interfaces.  You will learn how to use the standard tools of the trade in
> collaboration and data science coding, such as text editors, version control 
> and Github, as well as the standard process for collaboration and learning in 
> code, such as code testing, code review and automated testing for each code 
> change.  You will also learn how and when to use the base libraries for data 
> science analysis, such as Statsmodels, Scikit-learn, and others.  When you 
> finish the course, you will have the training you need to join mature data
> analysis teams in industry and academia, and to set up or lead your own teams,
> using these tools and processes.

# Module plan

Week 1:
* Session 1: The Problem with Notebooks (introducing scripts + VS code).
  Show a bad data analysis project, where everything that can go wrong with
  "sending notebooks via email" does go wrong. Motivate using scripts; exercises
  involves using scripts to perform a simple analysis. 
* Session 2: Collaboration, reproducibility and testing (git, github, assert
  statements). Exericse involves adding tests to analysing from session 1,
  collaborating using github.
* Lab: 

# My original vague module plan thoughts

PR's original vague thoughts about content (can be deleted when no longer 
needed):

Compilation of vague module ideas from our discussion yesterday:

Unifying ideas behind module structure: 
* introduce (generalized) linear models - representing traditional 
statistical methods - first from a computational perspective, and
then from a formula-based perspective
* add a "machine learning flavour" to the traditional methods e.g. 
test/train splits, cross validation
* use that "machine learning flavour" to introduce machine learning
methods, with an emphasis on developing a flexible modelling toolkit,
selecting methods appropriate for a given research question/aim
               
# Part 1: GLMs

Multiple linear regression
* Introduce multiple predictor linear regression
* Introduce dummy coding via a dummy coded predictor variable (this
 will link nicely with logistic regression? E.g. but what if want to use
a binary categorical variable as our outcome?)

Logistic regression
* introduce single predictor logistic model (using existing textbook page)
* once the computational approach has been shown, show the likelihood
 formula (e.g. how we can obtain the same parameter estimates via the 
formula-based approach), use that as a springboard for the next topic
                 
How to read a formula: the mathematics of the linear model
* gentle intro, linking python functions (np.sum etc) to their
 equivalent mathematical notation (summation symbol etc.)
* python-based demonstrations of all the rules that will be used to
 show the mathematics of the linear model (e.g. where students can
 change the input values and see that the rule is always true, e.g.
 distribution of summation signs etc.)
* Just a note: it is possible to print latex equations with "live"
 variables, might be useful in this part...
* show mathematics relevant to linear model: algebra of sums; 
 proofs for z score distribution (mean of 0, SD of 1)
                 
Poisson regression: 
* use new formula reading skills to show how to fit a single predictor 
Poisson GLM by minimizing it’s negative log likelihood formula.

GLM sum-up:
* Emphasise that generalized linear models all fit a linear regression line/surface on some scale
e.g. on the scale of the link function (log odds, or log etc.). So the principles for including
multiple predictors are the same as for the linear regression model (can be dummy coded,
can be continuous) etc, essentially the linear model is being adjusted (generalized) to let
it be used with different types of outcome variable. This gives a flexible modelling framework,
use this “modelling mindset” as a link to the next section…
               
# Part 2: Model Comparison and Model Building 

* add a “machine learning flavour” to the techniques covered thus far
* test train splits, theory and practice (overfitting etc.)
               * cross validation, theory and practice
               * model comparison metrics (possibly keep it fairly simple here?)
               * illustrate model comparison with GLM(s) covered up until this point 
  (linear, logistic, poisson)
* use simulation to show why test/train splits etc. are important, e.g.
   using population data simulate what happens if different labs do and
   don’t use these techniques
               - use this section as a springboard into machine learning in next section
               
# Part 3: Machine Learning
*  introduce K-means classifier (maybe modify existing page to use test/train split,
and cross validation)
* show model comparison of k-means classifier vs logistic classifier to link
back to Part 1 and Part 2
* introduce another machine learning method (maybe a method for 
predicting a continuous outcome? then do model comparison with 
linear regression? Again, to link back to Part 1 and Part 2)

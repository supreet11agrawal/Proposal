# GSoC 2019 Proposal Supreet Agrawal
## Title

#### Implementing Stochastic Processes and Extending Bivariate Distributions
## Abstract
Sympy, being a Computer Algebra System offers great functionality and extensive support for symbolic computing. Probability and Statistics have an importance which has been recognised in most, if not all areas of science. SymPy implements univariate probability spaces in great detail, but spaces involving multiple random variables are not implemented with much detail, and random processes are not implemented at all.

As a CAS, it is essential that Sympy provides more support in the field of Probability and Statistics. One of the significant areas of interest in Probability is Stochastic Processes which have applications in various ranging from basic sciences to cryptography, signal processing and even financial markets.

My work in Sympy during summer would be to extend the support for bivariate distributions and introduce Stochastic Processes in Sympy. Later work will include adding support to export expressions of random variables to external libraries such as PyMC3 and PyStan.
## About Me

### Personal

__Name__: Supreet Agrawal

__Email Id__: 
* supreeta@iitk.ac.in *(Primary)*
* supreet11agrawal@gmail.com
 
 __Phone Number__: +91 8766372649
 
 __Gitter Usename__: [supreet11agrawal](https://gitter.im/supreet11agrawal)
 
 __Location__: Kanpur, U.P., India ([Maps](https://www.google.co.in/maps/place/Indian+Institute+of+Technology+Kanpur/@26.5144225,80.2389891,15z/data=!4m5!3m4!1s0x399c3701c4a8be71:0x3afbe880abc38436!8m2!3d26.5123383!4d80.2328995?hl=en))
 
 __Timezone__: IST ([GMT/UTC +5:30](https://www.timeanddate.com/time/zones/ist))
 
 __University__: Indian Institute of Technology, Kanpur ([Webpage](http://www.iitk.ac.in))

### Programming Background

I am a third-year undergraduate student of Chemical Engineering at Indian Institute of Technology, Kanpur, India.

Despite being a student of Chemical Engineering department, my primary interest has always been in Mathematics and Computer Science. Because of this interest, I have taken multiple courses in the Mathematics department and the Computer Science department.

Few of these courses are :
* Probability and Statistics
* Linear Algebra and Complex Analysis
* Fundamentals of Computing
* Game Theory and Mechanism Design
* Computational Methods in Engineering

Apart from these courses, I have audited various MOOCs and Institute Courses to learn more about the field.

Some of these being :
* [Computing Laboratory](https://cse.iitk.ac.in/pages/CS251.html)
* [Divide and Conquer, Sorting and Searching, and Randomized Algorithms](https://www.coursera.org/learn/algorithms-divide-conquer/home/welcome)
* [Python Functions, Files, and Dictionaries](https://www.coursera.org/learn/python-functions-files-dictionaries/home/welcome)
* [Graph Search, Shortest Paths, and Data Structures](https://www.coursera.org/learn/algorithms-graphs-data-structures)

As I have mentioned above, my coursework in Probability and Statistics helped me learn a lot in the field and will bring help to me directly in the Summer of Code project.

I am using Ubuntu 18.04 (LTS) and Atom for writing all of my code. I am using this setup for the last two years, and in this duration, I have become quite comfortable with it. For the purpose of debugging, I use *pdb*, to which I was introduced via [Kalevi Suominen](https://github.com/jksuom) while working on an issue.

I was introduced to Python two years ago. However, I am relatively new in terms of object oriented programming. Before working in Python, my programming experience was confined to C and C++. In comparison to these languages, Python is much more intuitive. In my opinion, Python is more expressive than any other language I have used. According to me, list comprehension is one of the best features which I have used.

My favourite feature about Sympy is its ability to compute asymptotic series expansions of functions around a point. I came across this feature while getting acquainted with the library. Sympy's ability to compute series expansions left me awestruck and was one of the primary reasons that inspired me to learn more about Sympy.
```
>>> x, n, t = symbols('x n t')
>>> pprint(log(x-t).series(x, x0 =t/n), use_unicode = False)
                                2                              3                                           4                                                           5                        
                ⎛    t⎞          2 ⎛    t⎞                      3 ⎛    t⎞                                   4 ⎛    t⎞                                                   5 ⎛    t⎞                         
              n⋅⎜x - ─⎟         n ⋅⎜x - ─⎟                     n ⋅⎜x - ─⎟                                3⋅n ⋅⎜x - ─⎟                                               12⋅n ⋅⎜x - ─⎟                         
   ⎛     t⎞     ⎝    n⎠            ⎝    n⎠                        ⎝    n⎠                                     ⎝    n⎠                                                     ⎝    n⎠                         
log⎜-t + ─⎟ - ───────── - ─────────────────────── - ───────────────────────────────── - ──────────────────────────────────────────────── - ───────────────────────────────────────────────────────────────
   ⎝     n⎠    n⋅t - t      ⎛ 2  2        2    2⎞      3  3      2  3        3      3       4  4       3  4       2  4         4       4       5  5        4  5        3  5        2  5          5       5
                          2⋅⎝n ⋅t  - 2⋅n⋅t  + t ⎠   3⋅n ⋅t  - 9⋅n ⋅t  + 9⋅n⋅t  - 3⋅t    12⋅n ⋅t  - 48⋅n ⋅t  + 72⋅n ⋅t  - 48⋅n⋅t  + 12⋅t    60⋅n ⋅t  - 300⋅n ⋅t  + 600⋅n ⋅t  - 600⋅n ⋅t  + 300⋅n⋅t  - 60⋅t 

                     
                     
    ⎛       6       ⎞
    ⎜⎛    t⎞       t⎟
 + O⎜⎜x - ─⎟ ; x → ─⎟
    ⎝⎝    n⎠       n⎠


```
I am reasonably comfortable with Git and Github as they were part of the course curriculum of one of the courses I audited. I have been using these over the past months for contributing to Sympy and otherwise making me quite comfortable with them.

## The Project
### Motivation
My primary motivation towards this project is my interest in the field of probability and statistics. Through this project, I would like to improve my grasp on the field and work on implementing this vital part of the field of probability on a wide scale platform.

I have been working with Sympy for about the last two months. Moreover, in my experience, I haven't seen a better work environment. I was just fascinated by everybody's behaviour and willingness to help each other in the process. In these past two months, my knowledge about python and object oriented programming has increased manifold. I want to continue working on Sympy after the GSoC period as well because of the reasons I mentioned above.
### Implementation Plans
As implementing stochastic processes is not an easy task; I would like to break the process into smaller parts which will help me provide a better insight to solve the problems that remain.

More or less, the project can be broken into 4 stages:

#### Stage 1
---
Implementing basic probabilistic functions such as `quantile`, `median` and `mode`.
Currently, Sympy does not offer support for finding these averages. Mean is supported in terms of expectation but standard functions for median and mode might be useful too. I will implement these essential functions before moving further as these are one of the most basic yet critical average values when it comes to Statistics.

__Quantile__

It can be viewed as `solve(cdf(X)(z) - p, z)`. Here, `X` is the distribution, `z` is the random variable and `p`. This function should work more robustly for continuous distributions which are most widely used.

For discrete cases, however, the situation changes and more theoretical research needs to be done before implementation.

__Median__

It can be considered a particular case of `Quantile` for which `p` is `1/2`.

Alternatively, this can be calculated by using something like `min(solveset(Eq(cdf(X)(z), S.Half), z, domain = S.Reals)` where `X` is the density of a distribution.

__Mode__

This can be viewed something like `z` for which `density(X)(z) == max(density(X)(x))`. This can also be implemented by checking `min` of `solveset(Eq(density(X)(z).diff(z)))` which satisfies `density(X)(z).diff(z, 2) < 0`. However, this method won't be able to find the mode for distributions which have mode as global maxima; for example, Exponential Distribution. For such distributions, the former method might be more useful. Currently, finding global maximum and maxima of a function is not possible in Sympy. I am working on this issue in [#16239](https://github.com/sympy/sympy/issues/16239) and will continue with it once the proposal is finalised.

__Entropy__

As of now, Entropy of a distribution cannot be evaluated in Sympy. Following is the High-Level idea of implementing probability:
```
if X.is_discrete:
    return summation(density(X)*log(density(X)))
elif X.is_continuous:
    return integrate(density(X)*log(density(X)))
```
Note: This is a high level idea just to show basic functioning.

__Theoretical Research__

In this period I would like to brush up the concepts of Stochastic processes and work on developing a basic methodology for implementing them in Sympy.

#### Stage 2
---

In this period, I would work upon [`JointRV`](https://github.com/sympy/sympy/blob/master/sympy/stats/joint_rv_types.py#L22). As of now, the set for each component for a `JointRV` is equal to the Real set, which can not be changed. Work will be done on adding support for custom sets which the users can provide.

Also, looking at the `joint_rv.py`, one can see that various functions need to be implemented for making joint distributions more robust. Primary examples which need utmost priority are [`where`](https://github.com/sympy/sympy/blob/fb7ed3c7d4dc437745db366f28c55d5963c55f0a/sympy/stats/joint_rv.py#L127), [`compute_density`](https://github.com/sympy/sympy/blob/fb7ed3c7d4dc437745db366f28c55d5963c55f0a/sympy/stats/joint_rv.py#L130), [`sample`](https://github.com/sympy/sympy/blob/fb7ed3c7d4dc437745db366f28c55d5963c55f0a/sympy/stats/joint_rv.py#L133) and [`probability`](https://github.com/sympy/sympy/blob/fb7ed3c7d4dc437745db366f28c55d5963c55f0a/sympy/stats/joint_rv.py#L136).

Implementing `compute_density` isn't much of a challenge. `marginal_distribution` works by finding integral over all the other random variables (other than the one for which marginal distribution needs to be calculated) over the `S.Reals` domain. As I have mentioned above, this `S.Reals` is set dafault and cannot be changed by the user. Thus by changing limits to `lower_bound of x` to `x` for each random variable `x`, cdf can be calculated.

Similarily, `where` can also be broken into two parts using `P(A/B) = P(Intersection(A, B))/P(B)`. The same has been implemented for univariate distributions. Once all these functions are implemented `probability` will just show results on the basis of these.

Also, implementing multivariate distributions will help me understand more how I should implement stochastic processes. In this period I would like to introduce a few more multivariate distributions to Sympy.

A typical bivariate distribution will look like:

```
class XYZDistribution(JointDistribution):

    _argnames = ['arg1', 'arg2']
    
    @property
    
    def set(self):
    
        # set on which the distribution is valid will be defined here
    
    @staticmethod
    
    def check(self, arg1, arg2):
    
        #checking if valid parameters are entered
        
    def pdf(self, arg1, arg2):
    
        arg1, arg2 = self.arg1, self.arg2
        
        # pdf defined
        
    def marginal_distribution(self, arg1, arg2):
    
        arg1, arg2 = self.arg1, aelf.arg2
        
        # marginal distribution defined here
```

#### Stage 3
---

I would start working on stochastic distributions in this period. A new file `stochastic_types.py` will contain all the different types of stochastic processes.

For each different process, there will be a different class which stores different information related to the process in the form of objects. I will start with Markov chains during this stage.

The problems which will be addressed by the class `MarkovChain` will be as follows:
 * To find the state matrix after any general number of steps, say `t`
 * To find the Stationary Matrix
 * To find the Limiting Matrix (For Absorbing Markov Chain)
 * To find the Fundamental Matrix (For Absorbing Markov Chain)
 * More properties related to Fundamental Matrix (If time permits):
   * Expected number of steps before being absorbed
   * Variance on the number of steps before being absorbed
   * Probability of visiting a transient state
   * Probability of being absorbed in an absorbing state

The user will give the initial state in the form of a row matrix. A square transition matrix will also be provided by the user.

Crude functioning of class MarkovChain will be as follows:
```
class MarkovChain(Basic):

    def __new__(transition, state0 = None): 
    
    #None if the user needs just properties related to Transition matrix
    
        if state0 != None and not (isinstance(state0, Matrix)):
        
            raise ValueError()
            
        if not isinstance(transition, Matrix):
        
            raise ValueError()
            
        if sum(a) != 1:
        
            raise ValueError()
            
        # transition is not len(a)*len(a) matrix results in error
        
        for j in range(len(a)):
        
            if sum transition[j] != 1:
            
                raise ValueError()
    
    def init(self):
    
        return self.args[1]
    
    def trans(self):
    
        return self.args[0]
   
    def state(self, t):
    
        if self.init != None
        
            return self.init()*self.trans()**t
            
        # We can do this by using either state0*transition**t or using a loop multiplying
        # state matrix continuously with transition.
        
        # I would prefer loop as it will take something like O(t*n**2) complexity and former
        # method will have O(t*n**3) complexity
    
    def stationary(self):
    
        temp = self.trans().T
        
        a = max(temp.eigenvects())[2][0]
        
        return a/sum(a)
    
    def fundamental(self):
    
        temp = self.trans()
        
        flag = 0
        
        arr = []
        
        for i in range(len(temp)):
        
            if temp[i][i] == 1:
            
                flag = 1
                
                arr.append(i)
                
        if flag != 1:
        
            return ValueError()
            
        else:
        
            for i in len(temp):
            
                temp[i].pop(arr(i))
                
                temp.pop(arr(i))
                
                for j in range(len(arr)):
                
                    arr[j] = arr[j]-1
                    
            return (eye(len(temp))-temp)**-1
```
The basic idea here is to make an object of `MarkovChain` class and use this class for evaluating different outcomes.

#### Stage 4
---

I would start working on the implementation of Random Walks during this period. The first problem that I would like to mention here is that Sympy is not a simulation software, as told by [Mr Fransesco Bonazzi](https://github.com/Upabjojr). I agree and thus think that we cannot implement a simulation of Random Walk andd tell the user the path taken for a particular case. Here, we need to compute the properties of a given random walk and not simulate it and tell the user results for a particular trial.

I would start with Simple Random Walks as they are most basic and useful. After that 1D random walks(Bernoulli Walk) and 2D random walks will be implemented. If time permits then random walks can also be implemented for a graph of any general `n` degrees.

I have listed below the functionalities I think Sympy's Random Walk classes can have. Further improvements will be made with the help of the mentor.
__Simple Random Walk__

Questions addressed in this class can be listed as:
* Probability that the position is `d`(`d` is the distance from the starting point in a fixed direction) after `N`steps
* Any general `t`th order of moment of the distribution
* Mean of distribution
* Skewness
* Kurtosis
* Expected value of being at an absolute distance `d` after `N` steps

A crude prototype of class for implementation of Simple Random Walk is as follows:

```
class SimpleRandomWalk(Basic):

    def position(d, N):
    
        if ((N-d)%2 != 0):
        
            return 0
            
        else:
        
            return binomial(N, d)/2**N
            
    def moment(t, N):
    
        d = Symbol('d', real = True)
        
        return summation((d**t)*position(d, N), (d, -N, N))
        
    def mean():
    
        return 0
        
    def skewness():
    
        return 0
        
    def kurtosis(N):
    
        return (-2)/N
        
    def expectedPosition(N):
    
        return summation(Abs(d)*position(d, N), (d, -N, N))
    
```

__1D Random Walk__ implemented in Sympy will work as follows:
* The user gives `p`; the probability of taking a step to the right; as an input
* The user can ask for questions such as
  * After any general `N` steps, the probability of being at a fixed point(`s` steps from the original point in a fixed direction)
  * The probability of taking a particular order of steps(i.e. `n1` steps to the right and `n2` steps to the left)
  * Expected number of revisits to a point
  * If `N` steps walked, then
    * Expected number of steps to the right
    * Expected number of steps to the left
    * Variance
    * Standard deviation

Following is the crude prototype for class of 1D Random Walk:

```
class OneDRandomWalk(Basic):

    def position(self, d, N):
    
        if (N-d)%2 != 0:
        
            return 0
            
        else:
        
            return binomial(N, (d+N)/2)*self.p**((N+d)/2)*selfq**((N-d)/2)
            
    def expectedRight(self, N):
    
        return self.p*N
        
    def expectedLeft(self, N):
    
        return self.q*N
        
    def variance(self, N):
    
        return N*self.p*self.q
        
    def std(N):
    
        return sqrt(variance(N))
```

__2D Random Walk__
This is more complicated to implement as compared to others. I'll have to develop a strong foundation of 2D random walks beforehand so that their implementation could be done more easily. Keeping end users in mind, it will be better to implement a robust symmetric 2D random walk as compared to a slaggy and unnecessarily complicated 2D random walk functionality.

Thus, my primary focus will be to implement symmetric 2D random walks and then move forward with the unsymmetric part.

Functionalities planned to be implemented for 2D random walk are listed below:
* Probability of coming back at the origin after the `N` steps
* Expected distance after `N` steps
* Expected number of steps taken to move to a distance `d` from the origin

Please note that the list above is incomplete. The functionality of 2D Random Walk class will be extended much more than this, but theoretical research is required for the same. The community bonding period will be a good time for studying it and discussion of ideas with the mentor.

In this period, implementation of Stochastic Processes continuous in time will also be studied and if possible, implemented. However, considering the complexity of such processes and limited amount of time; I have not included them in the timeline. I will continue to work on them after GSoC.

#### Stage 5
---

__Exporting expressions of Random Variables to external libraries__

The idea here is to make Sympy random variables exportable to libraries such as PyStan and PyMC3. These libraries are quite efficient in terms of probabilistic calculations and will thus increase the robustness of Sympy stats module as well.

For any distribution, the aim will be to make a PyMC3/PyStan model which takes Sympy random variables as parameters.
For PyMC3, (last year's proposal (Stage 5 of The Project))[https://github.com/sympy/sympy/wiki/GSoC-2018-Application-Akash-Vaish:-Improving-Probability-and-Random-processes#the-project] has an excellent idea of implementation.

The function mentioned in the proposal (Normal distribution as an example) was: 

```
import sympy.stats as ss

import pymc3 as pm

def convert_normal(normal_rv):

    """

    Given parameter is a sympy normal RV, which will be converted to

    a PyMC3 random variable. The PyMC3 RV is returned.

    """

    converter = pm.Model()

    name = str(normal_rv.args[0])

    mu, sd =  (int(arg) for arg in ss.density(normal_rv).args)

    with converter: #initialize model

        pm_normal = pm.Normal(name, mu, sd)

    return pm_normal
```
Usage:

```
>>> N = ss.Normal('N', 0, 1)

>>> x = convert_normal(N)

>>> type(x)

<class 'pymc3.model.FreeRV'>
```

However, I had a few changes in mind. This function does not work for symbolic parameters; i.e. `ss.Normal('N', mean, std)` as `int(arg)` in the line `mu, sd =  (int(arg) for arg in ss.density(normal_rv).args)` will not work for symbols. If we pass them directly, that is `mu, sd =  (arg for arg in ss.density(normal_rv).args)`, then it might create a problem in PyMC3. Discussion with mentor in the community bonding period would most likely give a feasible solution.

For PyStan, `pystan.stan` will be used for modelling. 

### TimeLine

My semester will end on 30th April; hence I am not including the time before 30th April 2019 in the timeline. In this period, however, I would like to work on the stats module and try to stay ahead of the timeline.

Listed below is the tentative timeline I would follow:

***
__Pre Selection Period + Community Bonding Period__
***

__May 1 - May 27__

The goal in this period would be to (More goals are set here considering the long period) :
* Get to know my mentor and other organisation members well, and get a clear idea of the workflow during the project.
* Brushing up of concepts involved in the compound distributions
* Completion of Stage 1
* Discuss better way of implementation and the possibilities of extending Stochastic processes
* Brushing up basics of random walks from _Principles of Random Walk by Spitzer F._

***
__The Coding Period__
***

__May 27 - May 31__ _(Week 1)_

* Work on including custom set support in joint distributions
* Theoretical Research on Markov Chains and ways to implement them _from Chapter 1 of Markov Chains by Norris J._
* Buffer Period: Completion of the remaining work and documentation improvement before moving to stage 2

__May 31 - June 20__ _(Week 2, 3)_

* Add more bivariate continuous distributions to Sympy and add test cases for them
* Study about other possible Stochastic processes which can be implemented in Sympy
* Theoretical research on continuous time Markov Chains and discussion of ways to implement them with mentor.
* Completion of Stage 2

__June 20 - June 24__ _(Week 4)_

* Start working on implementation of Markov Chains
* Study two dimensional recurrent random walk and the green function associated with it
* Buffer Period: Completion of the remaining work and documentation improvement before Phase 1 Evaluation

***
__Phase 1 Evaluation__
***

__June 24 - July 8__ _(Week 5, 6)_

* Continue with Markov Chain implementation in Sympy
* Theoretical research and start working on implementation of other stochastic processes
* Discuss and develop ways of implementing a general class for Random walks in Sympy

__July 8 - July 15__ _(Week 7)_

* Adding test cases of Markov Chains
* Start on implementation of Simple Random Walk
* Theoretical research on Random Walk on a Half line and discussion with mentor about possibilities of including them in Sympy
* Completion of Stage 3

__July 15 - July 22__ _(Week 8)_

* Adding test cases for Simple Random Walk and checking for vulnerabilities and thus improvement
* Development of more formal methods for implementation of 2D Random Walks
* Buffer Period: Completion of the remaining work and documentation improvement before Phase 2 Evaluation

***
__Phase 2 Evaluation__
***

__July 22 - August 5__ _(Week 9, 10)_

* Implementation of 2D Random Walks in Sympy
* Theoretical study of Random Walks on an Interval
* Implementation of other stochastic processes about which research would have been done previously

__August 5 - August 12__ _(Week 11)_

* Adding test cases and improvements to 2D random walks
* Discussion with mentor regarding future work and further possiblities of adding more processes including continuous time processes
* Completion of Stage 4

__August 12 - August 19__ _(Week 12)_

* Work on exporting random variables to external libraries
* Discussion with mentor about future possible improvements to the stats module
* Completion of Stage 5

__August 19 - August 26__ _(Week 13)_

* Buffer Period: Completion of any backlog and documentation improvement before marking the completion of the project
* Final Report Submission

***
__Final Submission__
***

### Time Commitments

Before Summer, time spent on Sympy may vary depending on the academic activities. Mostly it will be 3-4 hours a day.

* __Working Hours__: 18:00-23:00 IST or 12:30-17:30 UTC

During Summer, on an average, I would be able to spend 7-8 hrs working on GSoC project daily; summing up to 50-60 hours per week
* __Working Hours__: 13:00-23:00 IST or 07:30-17:30 UTC

After Summer, as it will be beginning of new semester, I will be able to spend relatively more time on Sympy. On an average, I will work for 5-6 hours per day.
* __Working Hours__: Will vary according to college timetable. 

Summing up, on an average I would be able to give 40-50 hours per week in the period of GSoC.

### Post GSOC period

I will continue my work in Sympy and on the stats module and work on introducing new Stochastic Processes. I would also work upon increasing robustness of the module and improving the multivariate distributions.

Post GSoC, one important thing which can be changed is to make unevaluated version of `probability`. This can be understood as `Integral` which is the unevaluated version of `integrate`. `doit()` will be used to evaluate the probability explicity in this case. This approach was a result of discussion with [Mr. Fransesco Bonazzi](https://github.com/Upabjojr) and I am quite excited to work upon this.

## Contributions to Sympy
### Pull requests
The following are the lists of merged/open pull requests I have created(listed in chronological order)

* [#15841](https://github.com/sympy/sympy/pull/15841) Numbers: Removed the redundant checks of igcd method and simplified it.

* [#15958](https://github.com/sympy/sympy/pull/15958) Stats: Disabled non-valid probability inputs by Bernoulli, Coin and FiniteRV distibutions.

* [#16093](https://github.com/sympy/sympy/pull/16093) Core: Improved handling of Unicode text.

* [#16108](https://github.com/sympy/sympy/pull/16108) Stats: Improved parameter handling by Benini distribution.

* [#16154](https://github.com/sympy/sympy/pull/16154) Travis: Added a flag which reduced the output log so compilation errors could be found easily. (This PR used [#16156]() for testing the correctness of change)

* [#16159](https://github.com/sympy/sympy/pull/16159) Stats: Improved parameter handling and documentation of continuous distributions.

* [#16183](https://github.com/sympy/sympy/pull/16183) Stats: Completed the parameter handling improvement by continuous distributions.

* [#16189](https://github.com/sympy/sympy/pull/16189) Core: Added a function `unchanged` which checks if the expression remains unchanged.

* [#16220](https://github.com/sympy/sympy/pull/16220) Core: Replaced redundant checks in `core/tests/test_arit.py`

* [#16312](https://github.com/sympy/sympy/pull/16312) Stats: F Distribution parameter checking and test cases addition

* [#16314](https://github.com/sympy/sympy/pull/16314) Stats: Added a function `mean` which can be used to calculate arithmetic average

* [#16461](https://github.com/sympy/sympy/pull/16461) Stats: Restored changes in docs which were made by me in an old PR

* [#16473](https://github.com/sympy/sympy/pull/16473) Caculus: Added functions `stationary_points`, `minimize`, `maximize` which are used frequently in calculus.

### Issues opened
The following are the list of the issues opened by me(listed in chronological order)

* [#15903](https://github.com/sympy/sympy/issues/15903) Stats: Non-valid probability allowed by Finite Distributions resulting in wrong results

* [#15904](https://github.com/sympy/sympy/issues/15904) Stats: Finite Distributions were not added to Sympy docs

* [#16107](https://github.com/sympy/sympy/issues/16107) Stats: Non-valid parameters were allowed by continuous distributions

* [#16215](https://github.com/sympy/sympy/issues/16215) Core: Enhancing `unchanged` function to work for expressions like `exp(x)*exp(y)`

* [#16239](https://github.com/sympy/sympy/issues/16239) Functions: Sympy not able to evaluate Global maximum and maxima of a function

* [#16469](https://github.com/sympy/sympy/issues/16469) Calculus: Unexpected results while using `continuous_domain` and `function_range`

### Code Reviews
Code reviewing is one of the important tasks which helps new contributors learn more about Sympy. Though I was unable to find any major changes in the pull requests made by other contributors, I tried my best to help as much as I can and will continue to do so.
* [#16096](https://github.com/sympy/sympy/pull/16096#pullrequestreview-208620762) Suggested a fellow contributor to add test cases for checking if Unicode text was handled properly.

* [#16250](https://github.com/sympy/sympy/pull/16250#pullrequestreview-215008578) Suggested a minor correction in conditional statements

* [#16325](https://github.com/sympy/sympy/pull/16325#pullrequestreview-215960157) An assertion statement was giving error. Suggested how to write it correctly.

## References
* [Sympy docs](https://docs.sympy.org/latest/index.html)

* [Past year proposals](https://github.com/sympy/sympy/wiki/GSoC-2018-Current-Applications)

* [Wikipedia](https://www.wikipedia.org/)

* [Wolfram Mathworld](http://mathworld.wolfram.com)

* [Stack Exchange](https://math.stackexchange.com)

* Principles of Random Walk by _Spitzer F._

* Markov Chains by _Norris J._

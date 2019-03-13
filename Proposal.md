# GSoC 2019 proposal Supreet Agrawal
## Title

#### Sympy: Implementing Stochastic Processes
## Abstract
Sympy, being a Computer Algebra System, offers great functionality and extensive support for symbolic computing. Probability and Statistics has importance which has been recognised in most, if not all areas of science. SymPy implements univariate probability spaces in great detail, but spaces involving multiple random variables are not implemented with much detail and random processes are not implemented at all.

As a CAS, it is essential that Sympy provides more support in the field of Probability and Statistics. One of the major fields in Probability is Stochastic Processes which have applications in various ranging from basic sciences to cryptography, signal processing and even financial markets.

My work in Sympy during summer would be to extend the support for multivariate distributions and introduce Stochastic Processes in Sympy.
## About Me

### Personal

__Name__ : Supreet Agrawal

__Email Id__ : 
* supreeta@iitk.ac.in *(Primary)*
* supreet11agrawal@gmail.com
 
 __Phone Number__ : +91 8766372649
 
 __Gitter Usename__ : [supreet11agrawal](https://gitter.im/supreet11agrawal)
 
 __Location__ : Kanpur, U.P., India ([Maps](https://www.google.co.in/maps/place/Indian+Institute+of+Technology+Kanpur/@26.5144225,80.2389891,15z/data=!4m5!3m4!1s0x399c3701c4a8be71:0x3afbe880abc38436!8m2!3d26.5123383!4d80.2328995?hl=en))
 
 __Timezone__ : IST ([GMT/UTC +5:30](https://www.timeanddate.com/time/zones/ist))
 
 __University__ : Indian Institute of Technology, Kanpur ([Webpage](http://www.iitk.ac.in))

### Programming Background

I am a third year undergraduate student of Chemical Engineering at Indian Institute of Technology, Kanpur, India

I am using Ubuntu 18.04 (LTS) and Atom for writing all of my code. I am using this setup for last two years and in this duration I have become quite comfortable with it. For the purpose of debugging, I use *pdb*, to which I was introduced via [Kalevi Suominen](https://github.com/jksuom) while working on an issue.

Despite being a student of Chemical Engineering department, my main interest has always been in Mathematics and Computer Science. Beacuse of this interest I have taken multiple courses in Mathematics department and Computer Science department.

Few of these courses are :
* Probability and Statistics
* Linear Algebra and Complex Analysis
* Fundamentals of Computing
* Game Theory and Mechanism Design
* Computational Methods in Engineering

Apart from these courses, I have audited various MOOCs and Institute Courses to learn more about the filed.

Some of these being :
* [Computing Laboratory](https://cse.iitk.ac.in/pages/CS251.html)
* [Divide and Conquer, Sorting and Searching, and Randomized Algorithms](https://www.coursera.org/learn/algorithms-divide-conquer/home/welcome)
* [Python Functions, Files, and Dictionaries](https://www.coursera.org/learn/python-functions-files-dictionaries/home/welcome)
* [Graph Search, Shortest Paths, and Data Structures](https://www.coursera.org/learn/algorithms-graphs-data-structures)

As I have mentioned above, my coursework in Probability and Statistics helped me learn a lot in the field and will bring help to me directly in the Summer of Code project.

I was introduced to Python two years ago. However, I am relatively new in terms of object oriented programming. Prior to working in Python, my programming experience was confined to C and C++. In comparison to these languages, Python is much more intuitive. In my opinion, Python is more expressive than any other language I have used. According to me, list comprehension is one of the best features which I have used.

My favourite feature about Sympy is it's ability to compute asymptotic series expansions of functions around a point. I came across this feature while getting acquainted with the library. Sympy's ability to compute series expansions left me awestruck and was one of the primary reasons that inspired me to learn more about Sympy.
```
>>> x, n, t = symbols('x n t')
>>> pprint(log(x-t).series(x, x0 =t/n))
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
I am fairly comfortable with Git and Github as I have been using these over the past months for contributing to Sympy and otherwise.

## The Project
### Motivation
My main motivation towards this project is my interest in the field of probability and statistics. Through this project I would like to improve my grasp on the field and work on implementing this important part of the field of probability on a wide scale platform.
### Implementation Plans
As implementing stochastic processes will not be an easy task; I would like to break the process into smaller parts which will help me provide a better insight to solve the problems that remain.

I would like to break the period into 5 stages 

#### Stage 1
---
Implementing basic probabilistic functions such as `mean`, `median` and `mode`.
Currently Sympy does not offer support for finding these averages. I would like to implement these basic functions before moving further as these are one of the most basic yet important values when it comes to Statistics.

__Mean__

It can be viewed simply as `E(X)`.

__Median__

This can be calculated by using something like `min(solveset(Eq(cdf(X)(z), S.Half), z, domain = S.Reals)`

__Mode__

This can be viewed something like `z` for which `density(X)(z) == max(density(X)(x))`. This can also be implemented by checking `min` of `solveset(Eq(density(X)(z).diff(z)))` which satisfies `density(X)(z).diff(z, 2) < 0`. However, this method won't be able to find mode for distributions which have mode as global maxima, for example Exponential Distribution. For suvh distrbutions, former method might be more useful.

__Theoretical Research__

In this period I would like to brush up the concepts of Stochastic processes and work on developing a basic methodology for implementing them in Sympy.

#### Stage 2
---

Implementing multivariate distributions will help me understand more how I should implement stochastic processes. In this period I would like to introduce a few more multivariate distributions to Sympy.

In this period, I would also like to work upon [`JointRV`](https://github.com/sympy/sympy/blob/master/sympy/stats/joint_rv_types.py#L22). As of now, the set for each component for a `JointRV` is equal to the set of all integers, which can not be changed. I will try to add support for custom sets which will be provided by the user.

#### Stage 3
---

I would start working on stochastic distributions in this period. A new file `stochastic.py` will contain all the different types of stochastic processes.

For each different process, there will be a different class which stores different information related to the process in form of objects. I will start off with Markov chains during this stage.

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
The user will give the initial state in form of a row matrix. A square transition matrix will also be provided by the user.

Crude functioning of class MarkovChain will be as follows:
```
class MarkovChain(Basic):
    def __new__(transition, state0 = None): #None if the user needs just properties related to Transition matrix
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
    def state(self, t):
        return state0*transition**t
        # We can do this by using either state0*transition**t or using a loop multiplying state matrix continuously with transition
        # I would prefer loop as it will take something like O(t*n**2) complexity and former method will have O(t*n**3) complexity
    def stationary(self):
        temp = transition.T
        a = max(temp.eigenvects())[2][0]
        return a/sum(a)
    def fundamental():
        temp = transition
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
#### Stage 4
---

I would start working on implementation of Random Walks during this period. The first problem that I would like to mention here is that Sympy is not a simulation software, as told by [Mr. Fransesco Bonazzi](https://github.com/Upabjojr). I totally agree and thus think that we cannot implement a simulation of Random Walk and tell user the path taken for a particular case. I have listed below the functionalities I think Sympy's Random Walk classes can have. Furthur improvements will be made with the help of mentor.

As solving for any general degree of graph is quite complicated and they are not used that often, I would start with Simple Random Walks as they are most basic and useful. After that 1D, 2D random walks will be implemented. If time permits then it can also be implemented for a graph of any general `n` degrees.

__Simple Random Walk__

Questions addressed in this class can be listed as:
* Probability that the position is `d`(`d` is the distance from the starting point in a fixed direction) after `N`steps
* Any general `t`th order of moment of distribution
* Mean of distribution
* Skewness
* Kurtosis
* Expected value of being at an absolute distance `d` after `N` steps

A crude prototype for implementation of Simple Random Walk is as follows:

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
* The user will give `p`; the probability to take a step to the right; as an input
* The user can ask for questions such as
  * After any general `N` steps, the probability of being at a fixed point(`s` steps from the original point in a fixed direction)
  * The probability of taking a particular order of steps(i.e. `n1` steps to the right and `n2` steps to the left)
  * If `N` steps walked, then
    * Expected number of steps to the right
    * Expected number of steps to the left
    * Variance
    * Standard deviation

Following is the crude prototype for 1D Random Walk:

```
class OneDRandomWalk(Basic):
    def position(self, d, N):
        if (N-d)%2 != 0:
            return 0
        else:
            return binomial(N, (d+N)/2)*self.p**((N+d)/2)*selfq**((N-d)/2)
    def expectedRight(self, p, N):
        return self.p*N
    def expectedLeft(self, N):
        return self.q*N
    def variance(self, N):
        return N*self.p*self.q
    def std(self, N):
        return sqrt(variance(N))
```

__2D Random Walk__



### TimeLine

My semester will end on 30th April; hence I am not including the time before 30th April, 2019 in the timeline. In this period, however, I would like to work on stats module and stay ahead of timeline.

Listed below is the tentative timeline I would follow:

__Pre Selection Period + Community Bonding Period__
***
__May 1 - May 27__

The goal in this period would be to
* Get to know my mentor and other organisation members well, and get a clear idea of the workflow during the project.
* Brush up of concepts involved
* Completion of Stage 1
* Discuss better way of implementation and the possibilities of extending Stochastic processes

__The Coding Begins__
***
__May 27 - May 31__

Buffer Period : Completion of the remaining work and documentation improvement before moving to stage 2

__May 31 - June 20__

Add support 

__June 20 - June 24__

Buffer Period : Completion of the remaining work and documentation improvement before Phase 1 Evaluation

__Phase 1 Evaluation__
***
__June 24 - July 15__

__July 15 - July 22__

Buffer Period : Completion of the remaining work and documentation improvement before Phase 2 Evaluation

__Phase 2 Evaluation__
***
__July 22 - August 12__

__August 12 - August 26__

* Buffer Period : Completion of any backlog and documentation improvement before marking the completion of project

* Final Report Submission


### Time Commitments
Before Summer, time spent on Sympy may vary depending on the academic activities. Mostly it will be 3-4 hours a day.
* __Working Hours__: 18:00-23:00 IST or 12:30-17:30 UTC

During Summer, on an average, I would be able to spend 7-8 hrs working on GSoC project daily; summing up to 50-60 hours per week
* __Working Hours__: 13:00-23:00 IST or 07:30-17:30 UTC

After Summer, as it will be beginning of new semester, I will be able to spend relatively more time on Sympy. On an average, I will work for 5-6 hours per day.
* __Working Hours__: Will vary according to college timetable. 
### Post GSOC period
I would like to continue my work on stats module and work on introducing new Stochastic Processes. I would also work upon exporting random variables to other libraries.

## Contributions to Sympy
### Pull requests
The following are the lists of merged/open pull requests I have created(listed in chronological order)

* [#15841](https://github.com/sympy/sympy/pull/15841) Numbers: Removed the redundant checks of igcd method and simplified it.
* [#15958](https://github.com/sympy/sympy/pull/15958) Stats: Disabled non valid probability inputs by Bernoulli, Coin and FiniteRV distibutions.
* [#16093](https://github.com/sympy/sympy/pull/16093) Core: Improved handling of Unicode text.
* [#16108](https://github.com/sympy/sympy/pull/16108) Stats:Improved parameter handling by Benini distribution.
* [#16154](https://github.com/sympy/sympy/pull/16154) Travis: Added a flag which reduced the output log so compilation errors could be found easily. (This PR used [#16156]() for testing the correctness of change)
* [#16159](https://github.com/sympy/sympy/pull/16159) Stats: Improved parameter handling and documentation of continuous distributions.
* [#16183](https://github.com/sympy/sympy/pull/16183) Stats: Completed the parameter handling improvement by continuous distributions.
* [#16189](https://github.com/sympy/sympy/pull/16189) Core: Added a function `unchanged` which checks if the expression remains unchanged.
* [#16220](https://github.com/sympy/sympy/pull/16220) Core: Replaced redundant checks in `core/tests/test_arit.py`
### Issues opened
The following are the list of the issues opened by me(listed in chronological order)

* [#15903](https://github.com/sympy/sympy/issues/15903) Stats: Non valid probability allowed by Finite Distributions resulting in wrong results
* [#15904](https://github.com/sympy/sympy/issues/15904) Stats: Finite Distributions were not added to Sympy docs
* [#16107](https://github.com/sympy/sympy/issues/16107) Stats: Non valid parameters were allowed by continuous distributions
* [#16215](https://github.com/sympy/sympy/issues/16215) Core: Enhancing `unchanged` function to work for expressions like `exp(x)*exp(y)`
* [#16239](https://github.com/sympy/sympy/issues/16239) Functions: Sympy not able to evaluate Global maximum and maxima of a function
### Code Reviews
Code reviewing is one of the important tasks which helps new contributors learn more about Sympy. Though I was unable to find any major changes in the pull requests made by other contributors, I am trying my nest to help as much as I can.
* [#16096](https://github.com/sympy/sympy/pull/16096#pullrequestreview-208620762) Suggested a fellow contributor [Divyanshu Thakur](https://github.com/divyanshu132) to add test cases for checking if Unicode test was handled properly.

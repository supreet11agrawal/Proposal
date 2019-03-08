# GSoC 2019 proposal Supreet Agrawal
## Title

#### Sympy: Implementing Stochastic Processes
## Abstract

Sympy is a Comuputer Algebra System
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

I am using Ubuntu 18.04 (LTS), and Atom for writing all of my code. I am using this setup for last 3 years and in this duration I have become quite comfortable with it. For the purpose of debugging, I use *pdb*, to which I was introduced via [Kalevi Suominen](https://github.com/jksuom) while working on an issue.

Despite being a student of Chemical Engineering department, my main interest has always been in Mathematics and Computer Science. Beacuse of this interest I have taken multiple courses in Mathematics department and Computer Science department.

Few of these courses are :
* Probability and Statistics
* Linear Algebra and Complex Analysis
* Fundamentals of Computing
* Game Theory and Mechanism Design
* Computational Methods in Engineering

As I have mentioned above, my coursework in Probability and Statistics helped me learn a lot in the field and will help me directly in the Summer of Code project.

I was introduced to Python two years ago. However, I am relatively new in terms of object oriented programming. Prior to working in Python, my programming experience was confined to C and C++. In comparison to these languages, Python is much more intuitive. In my opinion, Python is more expressive than any other language I have used. According to me, list comprehension is one of the best features which I have used.

My favourite feature about Sympy is it's ability to compute asymptotic series expansions of functions around a point. I came across this feature while getting acquainted with the library. Sympy's ability to compute series expansions left me awestruck and was one of the primary reasons that inspired me to learn more about Sympy.
```
>>> x = Symbol('x')
>>> t = Symbol('t')
>>> pprint(log(x-t).series(x), use_unicode = False)
    5      4      3      2                       
   x      x      x      x     x              / 6\
- ---- - ---- - ---- - ---- - - + log(-t) + O\x /
     5      4      3      2   t                  
  5*t    4*t    3*t    2*t                       

```
I am fairly comfortable with Git and Github as I have been using these over the past months for contributing to Sympy and otherwise.
# Add project details
## Contributions to Sympy
### Pull requests
The following are the lists of merged/open pull requests I have created(listed in chronological order)

* [#15841](https://github.com/sympy/sympy/pull/15841) Numbers: Removed the redundant checks of igcd method and simplified it
* [#15958](https://github.com/sympy/sympy/pull/15958) Stats: Disabled non valid probability inputs by Bernoulli, Coin and FiniteRV distibutions
* [#16093](https://github.com/sympy/sympy/pull/16093) Core: Improved handling of Unicode text
* [#16108](https://github.com/sympy/sympy/pull/16108) Stats:Improved parameter handling by Benini distribution
* [#16154](https://github.com/sympy/sympy/pull/16154) Travis: Added a flag which reduced the output log so compilation errors could be found easily (This PR used [#16156]() for testing the correctness of change)
* [#16159](https://github.com/sympy/sympy/pull/16159) Stats: Improved parameter handling and documentation of continuous distributions
* [#16183](https://github.com/sympy/sympy/pull/16183) Stats: Completed the parameter handling improvement by continuous distributions 
* [#16189](https://github.com/sympy/sympy/pull/16189) Core: Added a function `unchanged` which checks if the expression remains unchanged.
### Issues opened
The following are the list of the issues opened by me(listed in chronological order)

* [#15903](https://github.com/sympy/sympy/issues/15903) Stats: Non valid probability allowed by Finite Distributions resulting in wrong results
* [#15904](https://github.com/sympy/sympy/issues/15904) Stats: Finite Distributions were not added to Sympy docs
* [#16107](https://github.com/sympy/sympy/issues/16107) Stats: Non valid parameters were allowed by continuous distributions
### Code Reviews
Code reviewing is one of the important tasks which helps new contributors learn more about Sympy. Though I was unable to find any major changes in the pull requests made by other contributors, I am trying my nest to help as much as I can.
* [#16096](https://github.com/sympy/sympy/pull/16096#pullrequestreview-208620762) Suggested a fellow contributor [Divyanshu Thakur](https://github.com/divyanshu132) to add test cases for checking if Unicode test was handled properly.

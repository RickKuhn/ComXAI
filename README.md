# ComXAI

### Files stored here
CCMtools - some small Python utilities for mapping csv files with string values for variables into int values, and back to original string values.  This is done for faster processing by other tools. An input model should be created defining parameters and values, where column headings are parameter names and values are listed in columns.  Example given in the README for the tools.

Faultloc2 - this is the code for ComXAI, originally created from the fault location tools because the fault location problem maps directly to this approach for explainable AI, as discussed in the paper "Combinatorial Methods for Explainable AI", below.

## Introduction - Explainability, Verification, and Validation for Artificial Intelligence and Autonomous Systems
AI algorithms are increasingly used in safety-critical applications, such as autonomous driving and robotics.  Unfortunately, methods developed for ultra-reliable software, such as avionics, depend on measures of structural coverage that do not apply to neural networks or other black-box functions often used in machine learning.  A different approach that can be used is to ensure that all relevant combinations of input values have been tested and verified for correct operation. Our combinatorial coverage measures provide an efficient means of achieving this type of verification, and validating it in real-world use.  (see presentation Risk, Assurance, and Explainability for Autonomous Systems). 

Artificial intelligence and machine learning (AI/ML) systems typically equal or surpass human performance in applications ranging from medical systems to self-driving cars, and defense.  But ultimately a human must take responsibility, so it is essential to be able to justify the AI system's action or decision.  What combinations of factors support the decision?  Why was another action not taken?  How do we know the system is working correctly?  We consider explainability to be part of the larger problem of verification and validation for autonomous systems and artificial intelligence.

Our combinatorial methods and tools for assurance and dependability in AI and autonomous systems address both verification and validation. 

## Verification
Input space model measurement - To ensure that rare combinations are included in autonomous systems testing, we can apply covering arrays for all t-way combinations of parameter values, or measure the coverage of tests that are applied (in the case of random testing, or to evaluate coverage at higher strengths when a t-way covering array is used. (see link [1] below for background and [2] for case studies where covering arrays have been applied to autonomous vehicle testing)

https://csrc.nist.gov/Projects/automated-combinatorial-testing-for-software/coverage-measurement

https://csrc.nist.gov/Projects/automated-combinatorial-testing-for-software/case-studies-and-examples/autonomous-vehicles

### Sequence coverage measurement 
Sequences of events are a significant factor in system failure.  We have developed methods and tools to measure t-way event sequence coverage, to supplement measurement of input combination coverage.  These methods can be used for all software, but are particularly important for evaluating correct operations for autonomous systems. Measures can be applied to events in the environment, the system, and to system/environment interactions.

### Rule based systems testing 
By transforming rules in expert systems into k-DNF (disjunctive normal form where no term contains more than k literals), we can produce covering arrays that can be automatically mapped into test oracles for every rule, up to k=7 literals per logic term. (see [4] and [5] in papers below)

## Validation
Explainability - If we cannot explain or justify decisions of an AI application, then it is difficult to trust the system.  (see [1], [2], [3] in papers below)  Even black-box components such as neural nets can be hard to trust based only on a track record of use, as these systems are "brittle", in the sense that small changes can result in enormous errors, such as adversarial imaging where a stop sign is interpreted as a speed limit sign.

Combinatorial methods make possible an approach to producing explanations or justifications of decisions in AI/ML systems. This approach is particularly useful in classification problems, where the goal is to determine an object’s membership in a set based on its characteristics. These problems are fundamental in AI because classification decisions are used for determining higher-level goals or actions. Explainability is a necessary but not sufficient condition for assurance in these systems. 

We use a conceptually simple scheme to make it easy to justify classification decisions: identifying combinations of features that are present in members of the identified class but absent or rare in non-members. The method has been implemented in a prototype tool called ComXAI, which we are currently applying to machine learning problems.  Explainability is key in both using and assuring safety and reliability for autonomous systems and other applications of AI and machine learning. (see presentation Explainable AI)

## Papers and Presentations

DR Kuhn, R Kacker, Y Lei, D Simos, "Combinatorial Methods for Explainable AI", Intl Workshop on Combinatorial Testing, Porto, Portugal, March 23-27, 2020.

R. Kuhn, R. Kacker, Explainable AI, NIST presentation.  PDF Explainable AI   PPT Explainable AI  

D R Kuhn, R Kacker, Risk, Assurance, and Explainability for Autonomous Systems, Advancements in Test and Evaluation of Autonomous Systems (ATEAS) workshop, Dayton, OH, Oct, 2019. NIST presentation. 

DR Kuhn, D Yaga, R Kacker, Y Lei, V Hu, Pseudo-Exhaustive Verification of Rule Based Systems, 30th Intl Conf on Software Engineering and Knowledge Engineering, July 2018.

R. Kuhn, R. Kacker, An Application of Combinatorial Methods for Explainability in Artificial Intelligence and Machine Learning. NIST Cybersecurity Whitepaper, May 22, 2019. 


 

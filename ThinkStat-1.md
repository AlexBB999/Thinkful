THINKFUL IMMERSION


Python for data scientists IV: Intermediate statistics in Python

4.1


Drill set 1

1-Calculate the probability of flipping a balanced coin four times and getting each pattern: HTTH, HHHH and TTHH.

2-If a list of people has 24 women and 21 men, then the probability of choosing a man from the list is 21/45. What is the probability of not choosing a man?

3-The probability that Bernice will travel by plane sometime in the next year is 10%. The probability of a plane crash at any time is .005%. What is the probability that Bernice will be in a plane crash sometime in the next year?

4-A data scientist wants to study the behavior of users on the company website. Each time a user clicks on a link on the website, there is a 5% chance that the user will be asked to complete a short survey about their behavior on the website. The data scientist uses the survey data to conclude that, on average, users spend 15 minutes surfing the company website before moving on to other things. What is wrong with this conclusion?

ANSWERS

1 -- all probabilities the since flips are independentDrill set 1

1/2 x 1/2 x 1/2 x 1/2 = 1/16

2 -  1-21/45= 24/25

3 - dependent  P(A ∩ B) = P(A) * P(B | A)
P(crash and travel) = P(travel) * P(crash/travel)= 1% * .005% = .01 * .00005 = .000005

4 - Users may visit site without clicking on link
Have chosen a homogeneous sample

=====================================================

Drill Set 2

A diagnostic test has a 98% probability of giving a positive result when applied to a person suffering from Thripshaw's Disease, and 10% probability of giving a (false) positive when applied to a non-sufferer. It is estimated that 0.5 % of the population are sufferers. Suppose that the test is now administered to a person whose disease status is unknown. Calculate the probability that the test will:

1 -Be positive
2 - Correctly diagnose a sufferer of Thripshaw's
3 - Correctly identify a non-sufferer of Thripshaw's
4 - Misclassify the person

Now it's time to use Bayes' rule to compute some conditional probabilities. 
First, look over the numbers and estimate each of the four probabilities, using your intuition. 
Then, calculate the probabilities using Bayes' rule.

ANSWERS:

1 - guess  .05*.98 + .95 * .01= .0585

WAY WRONG

P(positive)=P(positive|not infected) +P (positive|infected)
P(positive|not infected) = p(not infected|positive)*


Using Bayes Rule:

P(Infected| Positive Test) = P(Positive Test| Infected) * P(Infected) / P(Positive Test)

P(A | B) = P(B | A) * P(A) / [P(A)*P(B|A) + P(A~)*P(B|A~)]

P(Infected|Positive)= P(Positive|Infected)*P(Infected)/ (P(Positive|Infected)*P(Infected) + P(Not Infected)*P(Positive|Not Infected))
			=.98*.005/(.98**.005+ .995*.1)
			
			
	
P(Positive|Infected)=P(Infected|Positive)*P(Positive)/[]

P(Positive|Infected) = P(Infected|Positive Test) * P(Positive) / (P(Infected|Positive))
                    
                    
P(infected)=.005
P(not infected)=.995
P(positive|infected)=.98
P(positive|not infected)= .1

3:
P(Negative| not infected)= P(not infected|negative )* P(not infected)/P(not infected/negative)

P(A | B) = P(B | A) * P(A) / [P(A)*P(B|A) + P(A~)*P(B|A~)]=.9*.995/[.9*.995+p(positive)*.995]
														    .9*.995/(.9*.995+..1044*.995)

P(not Trip/Non infected) =.9
P(not infected)=.995
P(Trip)=.005


.9*.995/.995

4 Misclassify

P(positive]not infected) + p(negative|infected)
.1(.995) +.02 (.005)
.0995+.0001=.0996
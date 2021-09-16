# Naked Statistics
## Stripping the dread from the data
### Charles Wheelan
	
	- **Checked out:** 08SEP21
	- **Finished reading:**

## Chapter 1: What's the point?

- **Summary statistics:** ease of comparison at the expense of oversimplification

- **Index:** simplifies complex things, HDI, QB rating, subjective in what is condsidered and relative weights.

- **Inference:** relies on sampling; small sampkes can provide great, accurate numbers, but subject to bias and error.

###Risk and probability

- Detective work identify relationships

- **Truth?** Building circumstantial evidence with imperfect data.

- Numerous reasons intellectuially honest people may disagree about statistical results or implications.

- Questions beset by issues defining terms / criteria "Best ____"; "Economic health of the middle class" relies on definitions of health and class.

- Like detective work. Smart and honest people will often disagree about what the data is telling us.

### Point of learning statistics
- Summarize huge data sets
- Make better decisions
- Answer important social questions
- Recognize patterns
- Catch cheaters / prosecure criminals
- Evaluate the effectiveness of policies, programs, drugs, procedures, or other innovations
- Spot those being dishonest with statistics

## Chapter 2: Descriptive Statistics
### Who was the best baseball player of all time?

**Concepts:** frequency distribution; normal distribution; measures of central tendency; variance; standard deviation

## Chapter 3: Deceptive Desctiption
### "He's got a great personality!" and other true but grossly misleading statements

- Statistically accurate and true statements may mask and obscure other information in a misleading way.
- May not be technically a lie, but could be so innacurate as to be untruthful.
- **The use of statistics to describe complex phenomenon is inexact, even if the underlying math is exact.**

### Accuracy v. Precision

- **Accuracy:** measure of whether a figure is broadly consistent with the truth
- **Precision:** reflects the exactitude with which we can express something. 41.3 miles is more precise than "about 40 miles" 

- More precise is generally better, but no degree of precision can make up for inaccuracy.
	- Precision can mask inaccuracy by giving a false sense of certainty - either inadvertantly or deliberately.

- Answers depend on how question is framed and how terms are defined. 
- "What is the health of US manufacturing?"
	- Employment in the manufacturing sector has steadily declined (~103 M to 88M 2000-2010)
	- Output, or total value of goods produced and sold, has grwon pretty seeadily over the same period (with a blip from 2008 recession, but bounced back robustly)
	- So - health of manufacturing for who? The workers? Or factory owners making more products with fewer people?

### Mean v Median

- Different measures of central tendency can paint a different picture of what is going on 
- Can be used to 'lie' with true figures
- Important to select which is more accurate or relevant

- **Median** Less sensitive to outliers; 

- **Mean:** 

### Percentaegs
- Don't lie, but can exaggerate
	- Very low starting point can have a huge percentage change which represents a negligible actual change
	- Convsely, with very large numbers (i.e., defense budget) a seemingly small percentage can still represent a huge number
		- 4% of the defense budget = $28B which is > than the entire NASA budget or ~~ to Department of Labor + Department of Treasury
	- A "10% raise for everyone" may sound fair.
		- $100,000 raise for boss making $1M
		- $5,000 raise for worker making $50,000
			- *Same percent raise ***20x difference*** in absolute size*

### Tough questions
- How to define **school quality**?
	- Test scores?
	- Very different backgrounds / abilities
- Reclassify things
	- Dropouts "moved away" or other category 
	- Houston Rod Page reported 1.5% dropout rate using schemes like this when actual figure was estimated to be 25-50%
- Testing
	- 10th grade is an important test.
	- Efforts were taken ro prevent the worst students from taking the test
		- One student held back in 9th grade three times, then promoted directly to 11th grade
- Physician mortality scorecards (NY State)
	- Unintended consequence of Doctors not operating on sickest patients.
	- Prople who would most benefit from certain procedures denied access

- **INDEX Stats** suffer from all of the pitfalls of other discriptive stats plus distortions from combining indicators into a single number.

- **Peer Assessment** factor for US News & World Reports college index
	- Notoriously unreliable
	- Chief Justice of Michigan Supreme court sent out a servey to 100 lawyers asking them to rank ten law schools in order of quality
		- Penn State was consistently rated in the middle *despite the fact that Penn State did not have a law school at the time*

---
**Summary**
- Statistical malfeasance has little to do with bad math.
- Impressive calculations can obscure nefarious motives
- The fact that you've calculated the mean correctly will not alter the fact that the median is a more accurate indicator (or the other way around)
- JUdgement and integrity are surprisingly important
- Detailed knowledge of statistics does not deter wrongdoing any more than a detailed knowledge of the law averts criminal behaviotr

### Correlation

- **Netflicks Recommendations** based on past ratings and rathings of others with similar taste can lead to shockingly accurate precictions

- **r^2** Correlation ceofficient -1..0..1

- Example:
	- HS HPA 0.56 corrolation to first year of college GPA
	- SAT also around 0.56 to freshman year GPA
	- Using HS GPA and SAT together leads to 0.64 correlation to First Year college GPA
- Correlation is not equal to causality.
- 2006 Netflix announces $1M prize to algorithm for 10% improvement in recommendations.
	- Training set of 100M ratings from 18k films and 480k customers
	- Thousands of teams from 180 countries submitted entries
	- 2009, seven-person team of statisticians and programmers from the US, Austria, Canada, and Israel won
		- Paper explaining algorithm is 92 pages long

## Chapter 5: Basic Probability
### Don't buy the extended warranty on your $99 printer

- Binomial experiment aka Bernoulli Trial; flip a coin

- **Expected Value:** payoff; sum of all the events weighted by the probablility
- Probability not deterministic
	- Good decision can end badly
	- Undsound decision may pay off in the short term
	- *But probability always triumphs in the end.*
	
# Naked Statistics
## Stripping the dread from the data
### Charles Wheelan
    
- **Checked out:** 08SEP21
- **Finished reading:**

## Chapter 1: What's the point?

- **Summary statistics:** ease of comparison at the expense of oversimplification

- **Index:** simplifies complex things, HDI, QB rating, subjective in what is considered, and relative weights.

- **Inference:** relies on sampling; small samples can provide great, accurate numbers, but subject to bias and error.

### Risk and probability

- Detective work identify relationships

- **Truth?** Building circumstantial evidence with imperfect data.

- Numerous reasons intellectually honest people may disagree about statistical results or implications.

- Questions beset by issues defining terms/criteria "Best ____"; "Economic health of the middle class" relies on definitions of health and class.

- Like detective work. Smart and honest people will often disagree about what the data is telling us.

### Point of learning statistics
- Summarize huge data sets
- Make better decisions
- Answer important social questions
- Recognize patterns
- Catch cheaters / prosecute criminals
- Evaluate the effectiveness of policies, programs, drugs, procedures, or other innovations
- Spot those being dishonest with statistics

## Chapter 2: Descriptive Statistics
### Who was the best baseball player of all time?

**Concepts:** frequency distribution; normal distribution; measures of central tendency; variance; standard deviation

## Chapter 3: Deceptive Description
### "He's got a great personality!" and other true but grossly misleading statements

- Statistically accurate and true statements may mask and obscure other information in a misleading way.
- May not be technically a lie, but it could be so inaccurate as to be untruthful.
- **The use of statistics to describe complex phenomenon is inexact, even if the underlying math is exact.**

### Accuracy v. Precision

- **Accuracy:** measure of whether a figure is broadly consistent with the truth
- **Precision:** reflects the exactitude with which we can express something. 41.3 miles is more precise than "about 40 miles." 

- More precise is generally better, but no degree of precision can make up for inaccuracy.
    - Precision can mask inaccuracy by giving a false sense of certainty - either inadvertently or deliberately.

- Answers depend on how the question is framed and how terms are defined. 
- "What is the health of US manufacturing?"
    - Employment in the manufacturing sector has steadily declined (~103 M to 88M 2000-2010)
    - Output, or the total value of goods produced and sold, has grown pretty steadily over the same period (with a blip from the 2008 recession, but bounced back robustly)
    - So - health of manufacturing for who? The workers? Or factory owners making more products with fewer people?

### Mean v Median

- Different measures of central tendency can paint a different picture of what is going on 
- Can be used to 'lie' with true figures
- Important to select which is more accurate or relevant

- **Median** Less sensitive to outliers; 

- **Mean:** 

### Percentages
- Don't lie, but can exaggerate
    - Very low starting point can have a huge percentage change which represents a negligible actual change
    - Conversely, with very large numbers (i.e., defense budget) a seemingly small percentage can still represent a huge number
        - 4% of the defense budget = $28B, which is > than the entire NASA budget or ~~ to Department of Labor + Department of Treasury
    - A "10% raise for everyone" may sound fair.
        - $100,000 raise for boss making $1M
        - $5,000 raise for worker making $50,000
            - *Same percent raise ***20x difference*** in absolute size*

### Tough questions
- How to define **school quality**?
    - Test scores?
    - Very different backgrounds/abilities
- Reclassify things
    - Dropouts "moved away" or other categories 
    - Houston Rod Page reported a 1.5% dropout rate using schemes like this when the actual figure was estimated to be 25-50%
- Testing
    - 10th grade is an important test.
    - Efforts were taken to prevent the worst students from taking the test
        - One student was held back in 9th grade three times, then promoted directly to 11th grade
- Physician mortality scorecards (NY State)
    - Unintended consequence of Doctors not operating on sickest patients.
    - People who would most benefit from certain procedures denied access

- **INDEX Stats** suffer from all of the pitfalls of other descriptive stats plus distortions from combining indicators into a single number.

- **Peer Assessment** factor for US News & World Reports college index
    - Notoriously unreliable
    - Chief Justice of Michigan Supreme court sent out a survey to 100 lawyers asking them to rank ten law schools in order of quality
        - Penn State was consistently rated in the middle *despite the fact that Penn State did not have a law school at the time*

---
### Summary
- Statistical malfeasance has little to do with bad math.
- Impressive calculations can obscure nefarious motives
- The fact that you've calculated the mean correctly will not alter the fact that the median is a more accurate indicator (or the other way around)
- JUdgement and integrity are surprisingly important
- Detailed knowledge of statistics does not deter wrongdoing any more than a detailed knowledge of the law averts criminal behavior

### Correlation

- **Netflicks Recommendations** based on past ratings and ratings of others with similar taste can lead to shockingly accurate predictions

- **r^2** Correlation ceofficient -1..0..1

- Example:
    - HS HPA 0.56 correlation to the first year of college GPA
    - SAT also around 0.56 to freshman year GPA
    - Using HS GPA and SAT together leads to a 0.64 correlation to First Year college GPA
- Correlation is not equal to causality.
- 2006 Netflix announces a $1M prize to an algorithm for 10% improvement in recommendations.
    - Training set of 100M ratings from 18k films and 480k customers
    - Thousands of teams from 180 countries submitted entries
    - 2009, a seven-person team of statisticians and programmers from the US, Austria, Canada, and Israel won
        - The paper explaining algorithm is 92 pages long

## Chapter 5: Basic Probability
### Don't buy the extended warranty on your $99 printer

- Binomial experiment aka Bernoulli Trial; flip a coin

- **Expected Value:** payoff; the sum of all the events weighted by the probability
- Probability is not deterministic
    - Good decision can end badly
    - Unsound decision may pay off in the short term
    - *But probability always triumphs in the end.*

    ## Chapter 5 1/2
    ### The Monty Hall Problem

    - Famous probability problem from *Let's Make a Deal*
    - Contestant Choose Door 1, Door 2, or Door 3
        - After selecting the door, the host opens one other door revealing no prize
        - Ask contestants if they want to switch doors
    - Correct answer is switching doors:
        - Currently, 1/3 chance of victory
        - 2/3 chance to win if switches
    - Counterintuitive. The host knows what is behind all doors. By switching after, the contestant gets to pick two doors instead of one. 
    - Gut instincts on probability can lead you astray

## Chapter 6: Problems with Probability
### How overconfident math geeks nearly destroyed the global financial system

- **Statistics cannot be any smarter than the people who use them**
- **VaR** Value at Risk Model
    - Theoretically combined the elegance of an indicator with the power of probability
    - Assumed range of possible outcomes: share goes up or down       - Over one week - expected to be similar, smaller chance raise/fall 10%, even smaller chance 25% delta, etc.
    - Based on past performance, quants assigned threshold for max value lost on a position over the time period with 99% CI
    - Can determine the risk for individual traders as well as the aggregate risk of the firm
    - Blamed for the onset and severity of the financial crisis in 2008
    - Underlying risk, more challenging to identify and model
        - False precision lead to a false sense of security
        - Analogous to a broken speedometer (which could be worse than no speedometer at all)
    - All models based on past market data
    - But the future doesn't always look like the past
    - No real reason to assume market from 1980-2005 would be a perfect indicator of 2005 onward
    - Models assigned 0% probability to large declines in housing prices - never happened before
    - Greenspan:
    >"The whole intellectual edifice, however, collapsed in the summer [of 2007] because the data input into the risk management models generally covered only the past two decades, a period of euphoria. Had instead the models been fitted more appropriately to historic periods of stress, capital requirements would have been much higher, and the financial world would be in far better shape, in my judgment."
    - 99 out of 100: Models didn't say how much over or how bad the 1% case could be
    - Tail risk... A small percentage of a catastrophic outcome
        
### Fundamental Errors      

1. Confused precision with accuracy (Exact and wrong)
2. Estimates of the underlying probabilities were wrong.
3. Neglect of "tail risk." Failed to define or limit the range of possibilities in that 1% case

### Results
- Worst global financial crisis since the Great Depression
- Destroyed Trillions of dollars of wealth in the US
- Unemployment > 10%
- Waves of home foreclosures and business failures

## Common issues

### Assuming events are independent when they are not

- Two fair coin heads 1/2 * 1/2 = 1/4
- One jet engine malfunctioning 1/100,000
    - Both engines (1/100,000)^2? or 1: 10 billion?
        - **NO**
        - Flock of geese hit both engines
        - Weather conditions contribute to failure
        - Maintenance issue
        - Design flaw
        - If one fails, p(other fail) >>> 1:100,000
- Example
    - SIDS: Sudden infant death syndrome
    - Medical mystery. Poorly understood
        - Led to suspicion
        - Sometimes used to cover up parental negligence or abuse
    - British prosecutors and courts focused on multiple instances of SIDS
        - "One infant death is a tragedy, two are suspicious, and three are murder
        - 1:8,500 incidence 2 x (1/8500)^2= 1 in 73 million
        - Flaw assumes events are random and not linked b some unknown factor
### Not understanding when events **ARE** independent

- Different error occurs when events are independent, but not treated as such.
- Casino. "Due" or "Hot"
- Gamblers Fallacy. Even if you flip heads 1,000,000 times in a row, p(H) next flip still = 0.5
- Notion of streaks in sports. "Hot hand" 
    - Rigorous analysis shows *no evidence for a positive correlation between the outcomes of successive shots*

### Clusters Happen

- Can be a pure chance even with multiple, simultaneous, improbable events
- Probability of five people at the same office or church contracting the same rare form of Leukemia may be one in a million, but there are millions of offices and churches. 
- When anomalous events are viewed out of context, it's easy to assume that something other than randomness must be responsible

### Prosecutor's fallacy

1. DNA sample found a the scene of a crime matches a sample taken from the defendant.
2. There is only a 1:1,000,000 chance it can match anyone else.

Neglects context.
- *Defendant 1:* Spurned lover arrested three blocks away carrying the murder weapon
- *Defendant 2*: Convicted of a similar crime in a different state several years ago; in a database of violent felons

*The chances of finding a one in a million coincidental match are relatively high if you compare a sample to a database with millions of people*

### Regression to the mean

*Sports Illustrated* jinx: Individuals or organizations featured perform worse after being featured on the cover.

More statistically sound reasoning: future after some anomalously good stretch (20 game winning streak) then future performance reverts back to the normal, mean.

Outliers in either direction are likely to be followed with outcomes more consistent with the long-term average

The performance consists of some underlying talent-related effort plus a degree of luck, good or bad.

### Statistical Determination

When is it okay to act on what probability tells us is likely to happen?

European regulators decided insurers can't charge men and women different rates based on sex - discriminatory. 

Statistically, men are more likely to crash - women pay more for annuities because they live longer on average.

Predictive models are leading to profiling. 

What can and should we do with this kind of information becomes a philosophical and legal question, not a statistical one. Is it okay to discriminate if the data tell us we'll be right far more often than wrong? 
    - People who buy birdseed less likely to default on credit cards

Our ability to analyze data has grown more sophisticated than our thinking about what we ought to do with the results. 

Like to think of numbers as "cold, hard facts"; calculations can give us the *right* answer. 

**For all the elegance and precision of probability, there is no substitute for thinking about what calculations 

## Chapter 7: The Importance of Data
### Garbage in Garbage Out


- Spring 2012 *Science* study about spurned fruit flies turning to alcohol
- Two groups of male flies:
    - One provided virgin females
    - One mixed with mated females indifferent to their advances
    - Both offered normal yeast and sugar fare as well as yeast and sugar + 15% EtOH
    - Spurned, frustrated flies drank more alcohol
- Good study design and data leads to clear story, not fancy statistical tricks
- Data : Statistics :: O-Line : Quarterback
    - In front of every star QB is a good set of blockers
    - Usually don't get much credit
    - Without them, never see a star QB
- **Garbage in, garbage out**

### Things we ask of our data

1. Demand a sample that is representative of some larger group or population
    - Voters attitudes towards candidate or measure
    
2. Provide some sourve of comparison
    - Is a new medicine more effective than a current treatment
    - Are ex-convicts who receive job training less likely to return to prison
    - Do students who attend charter schools perform better than similar students attending regular public school

- Inferences made from reasonably large, properly drawn samples can be every bit as accurate as trying to elicit the same information from the entire population
    - Easiest way to gather a representative sample is randomly
    - Simple random sample
    - Each observation must have an equal chance of being included
    - Drawing marbles out of an urn
- Practical challenges
    - How do you randomly select 100 people as a representative sample for a phone interview
    - Not everyone even has a phone: so, poorest not included
    - Others may be more prone to screen calls or not answer
    - Properly drawn sample will look like th population it was drawn from
    - Spoonful of soup will tell you what the pot tastes like

### Takeaways
1. Representative sample is an important thing
    - Opens the door to some powerful statistical tools
2. Getting good samples is harder than it looks
3. Many of the most egregious statistical assertions are caused by good statistical methods applied to bad samples (not the opposite)
4. Size matters and bigger is better (bowl of soup even better indicator of pot than spoonful)
    - BUT, bigger sample will not make up for errors (or bias) in its composition
    - A bad sample is a bad sample

### Difference testing

- Goal is to find two groups of subjucts who are boradly similar except for whatever 'treatment' we are testing
- Physical and biological sciences, it is straightforward to create treatment and control groups
- When humans are involved, it gets trickier
    - We can't force people to do things we make lab rats do
    - Do repeated concussions cause serious neurological problems later in life?
        - Important question, but can't take a group of people and bash them over the head
    - Challenging to create treatment and control groups that vary *only* by the treatment being tested
        - Randomization is the gold standard
        - Randomly assigned to treatment or control group

### Sometimes we collect data "just because"

- No specific idea what we will do with the data, but suspect it will come in handy at some point
- Crime scene detective collecting all evidence captured to sort later for clues
    - Some will be useful
    - Some will not
    - No idea which is which before you start digging
    - If we knew exactly what info was useful, we probably wouldn't be doing the study in the first place
- Framingham, Mass 67,000 people long-running longitudinal heart study
    - Useful for exploring causal relationships
# catsim - Computerized Adaptive Testing Simulator

## Quick start

**catsim** is a computerized adaptive testing simulator written in Python 3.4 (with modification in Python 3.8). It allow for the simulation of computerized adaptive tests, selecting different test initialization rules, item selection rules, proficiency reestimation methods and stopping criteria.

Computerized adaptive tests are educational evaluations, usually taken by examinees in a computer or some other digital means, in which the examinee's proficiency is evaluated after the response of each item. The new proficiency is then used to select a new item, closer to the examinee's real proficiency. This method of test application has several advantages compared to the traditional paper-and-pencil method, since high-proficiency examinees are not required to answer all the easy items in a test, answering only the items that actually give some information regarding his or hers true knowledge of the subject at matter. A similar, but inverse effect happens for those examinees of low proficiency level.

*catsim* allows users to simulate the application of a computerized adaptive test, given a sample of examinees, represented by their proficiency levels, and an item bank, represented by their parameters according to some Item Response Theory model.

<!-- ## Installation

Install it using `pip install catsim`. -->

## Computerized Adaptive Testing Lifecycle

![catsim](https://douglasrizzo.com.br/catsim/_images/graphviz-9e87416897233367d784b773084646a57761b919.png)

## Important links

- Official source code repo: <https://github.com/douglasrizzo/catsim>
- HTML documentation (stable release): <http://douglasrizzo.github.io/catsim>
- Issue tracker: <https://github.com/douglasrizzo/catsim/issues>

## Dependencies

- In the `requirements.txt` file.

## Files structures

### catsim/initialization.py

- Randomly initializes the first estimate of an examee's proficiency with `RandomInitializer`, the distribution is either `normal` or `uniform`.
- Initializes fixed point with `FixedPointInitializer`.

### catsim/selection.py

- Select item by Maximum information with `MaxInfoSelector`.
- Select item that random from a set of item have information equally to the maximum one with `MaxInfoGroupWithRandomSelector`
- Select item in a linear order (not present item) with `LinearSelector`.
- Randomly select item with `RandomSelector`.
- Cluster-based Item selection with `ClusterSelector`.
- Stratified selection with `StratifiedSelector`.
- Alpha Stratified selection method with `AStratifiedSelector`.
- Alpha Stratified selection and divide to block with `AStratifiedBBlockingSelector`.
- Maximum information stratification (MIS) with `MaxInfoStratificationSelector`.
- Maximum information stratification with block with `MaxInfoBBlockingSelector`.
- 5-4-3-2-1 Selector with `The54321Selector`.
- Randomsque Selection with `RandomesqueSelector`.
- Interval integration selection with `IntervalIntegrationSelector`.

### catsim/estimation.py

- Maximum log-likelihood function with `HillClimbingEstimator`
- Minimize negative log-likelihood function with `DifferentialEvolutionEstimator`
- Ability estimation using `BayesianEstimator`

### catsim/stopping.py

- Maximum length item stop rule with `MaxItemStopper`.
- Minimum error for ability estimation with `MinErrorStopper`.
- Minimum confidence that ability estimated exceeds a threshold `MinConfidenceStopper`.

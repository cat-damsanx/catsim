# catsim - Computerized Adaptive Testing Simulator

## Quick start

**catsim** is a computerized adaptive testing simulator written in Python 3.4. It allow for the simulation of computerized adaptive tests, selecting different test initialization rules, item selection rules, proficiency reestimation methods and stopping criteria.

Computerized adaptive tests are educational evaluations, usually taken by examinees in a computer or some other digital means, in which the examinee's proficiency is evaluated after the response of each item. The new proficiency is then used to select a new item, closer to the examinee's real proficiency. This method of test application has several advantages compared to the traditional paper-and-pencil method, since high-proficiency examinees are not required to answer all the easy items in a test, answering only the items that actually give some information regarding his or hers true knowledge of the subject at matter. A similar, but inverse effect happens for those examinees of low proficiency level.

*catsim* allows users to simulate the application of a computerized adaptive test, given a sample of examinees, represented by their proficiency levels, and an item bank, represented by their parameters according to some Item Response Theory model.

## Installation

Install it using `pip install catsim`.

## Important links

- Official source code repo: <https://github.com/douglasrizzo/catsim>
- HTML documentation (stable release):
    <http://douglasrizzo.github.io/catsim>
- Issue tracker: <https://github.com/douglasrizzo/catsim/issues>

## Dependencies

catsim depends on the latest versions of NumPy, SciPy, Matplotlib and
scikit-learn, which are automatically installed from pip.

To run the tests, you'll need to install the testing requirements
pip install catsim[testing].

To generate the documentation, Sphinx and its dependencies are needed.

## Files structures

### catsim/estimation.py

- Maximum log-likelihood function using Hill Climbing
- Minimize negative log-likelihood function using Differential Evolution
- Estimate using Bayesian Estimator catsim -- Computerized Adaptive

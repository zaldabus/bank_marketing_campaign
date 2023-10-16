
![Bank Marketing Campaign](./images/readme_hero.jpeg)


# Comparing Classifiers Against Bank Marketing Campaigns

This repo is a data modeling exercise based a dataset initially from the [ICU Dataset Repository](https://archive.ics.uci.edu/dataset/222/bank+marketing). The dataset in question is provided from a direct marketing campaign by a Portuguese banking institution to determine critical factors related to whether clients would subscribe to a term deposit.

The purpose of this exercise was to compare the performance of four different classifiers, K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines.

## Installation

### Dependencies:
```yml
- Python: 3.11.3
- Anaconda: 2.4.0
- Jupyter Notebook: 6.5.4
- Matplotlib: 3.7.1
- Seaborn: 0.12.2
- Pandas: 1.5.3
- Numpy: 1.24.3
- Scikit-Learn: 1.2.2
- Imbalanced-Learn: 0.11.0
```

The easiest way to install Anaconda is from the [online download source](https://www.anaconda.com/download). See the [installation page](https://docs.anaconda.com/free/anaconda/install/index.html) for more details on installation process. After downloading open Anaconda Navigator to download Jupyter Notebook

Additional dependencies can be installed from the command line using Conda:

```bash
  conda install -c matplotlib seaborn pandas numpy scikit-learn imbalanced-learn
```

After installing dependencies, run a new Jupyter Notebook instance from root of project:

```bash
  jupyter notebook
```

## Lessons Learned

Certain trends were observed over the course of model training and optimization.

First, SVM performed the worst in regards to training time. This demonstrates the weakness of SVM when m >> n (samples greater than features). The rule of thumb threshold for SVM is for sample sizes up to 10,000. In the case of this exercise, particularly after over-sampling to balance for dependent variable outcomes, the number of samples was approximately 73,000. This clearly demonstrates the weakness of SVM.

Decision Tree and Logistic Regression were a close place for second, followed by K Nearest Neighbor. The difference was much smaller amongst these three classifiers, though the difference would become more noticeable as the sample size continues to scale.

Looking at scoring, after training optimization Decision Tree returned the highest score for training and the second highest score for test datasets, though it also had the largest disparity between the two. This shows that while tree-based classifiers can achieve high scoring performance, significantly higher effort is required to avoid overfitting issues.

While it was not considered a required part of the exercise, in terms of which classifier could be considered the best for the problem set, my opinion is that Decision Tree would be most appropriate. First, Decision Tree had one of the highest scoring performance. Second, and more importantly, the problem set of this exercise is to "determine the main characteristics that affect success". As such, using a model with easily interpretable results is highly beneficial. Amongst the four clasifiers in question, Decision Tree stands out on this point having various tools available to examine the different features obsesrved.

As a follow up exercise, it would be beneficial to examine the tree created based on this data to gain a better understanding of how the different factors play into a client's decision.


## Authors

[@zaldabus](https://github.com/zaldabus)


## License

[MIT License](https://choosealicense.com/licenses/mit/)
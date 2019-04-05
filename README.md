# Algorithm to detect Close Submitters in Online Environments

This algorithm was presented as part of the publication "A data-driven method for the detection of close submitters in online learning environments" presented in the 26th International Conference on World Wide Web and co-authored by José A Ruipérez-Valiente, Srecko Joksimović, Vitomir Kovanović, Dragan Gašević, Pedro J Muñoz-Merino, Carlos Delgado Kloos. The original [paper](WWW_DataDrivenMethod.pdf) is in this repo.

## Overview

Online learning has become very popular over the last decade. However, there are still many details that remain unknown about the strategies that students follow while studying online. In this study, we focus on the direction of detecting 'invisible' collaboration ties between students in online learning environments. Specifically, the paper presents a method developed to detect student ties based on temporal proximity of their assignment submissions. This can help multiple account cheating and authorized collaborations (passing answers to other peers) in online environments.


## How to use

The algorithm is easy enough to be used by others and its provided as a Jupyter notebook ([close_submitters.ipynb](close_submitters.ipynb)). Follow the next steps:

1. You need to compute a submission matrix where every row corresponds to an student, every column to an assignment in a course, and the value of the cell is the timestamp of the last submission of the student to that assignment. More details in the [paper](WWW_DataDrivenMethod.pdf), but I also have included a [example of submission matrix](example_submission_matrix.csv).
2. There are few parameters to configure the algorithm:
   * *distance_metric*: Metric that is used to compare distances between vectors of submission timestamps from.
   * *minPercentageCommonItems*: Mean percentage of items in common between two accounts to be kept in the analysis, otherwise it will return a NaN for the couple.
   * *minPercentageCommonItems*: Min percetange of items from total submitted for an account to keep it within the analysis.
   *  *minPercentageCommonItems*: Names of columns (assignments), to be kept in the analysis.
   *  *timeThreshold*: Time threshold in minutes for close submitters.


## Citation

If you use the algorhtm please cite as:

> Ruipérez-Valiente, J. A., Joksimović, S., Kovanović, V., Gašević, D., Muñoz-Merino, P. J., & Delgado Kloos, C. (2017, April). A data-driven method for the detection of close submitters in online learning environments. In Proceedings of the 26th International Conference on World Wide Web Companion (pp. 361-368). International World Wide Web Conferences Steering Committee.

## Help or collaboration

The algorithm was written by José A Ruipérez-Valiente, if you need help or want to propose a collaboration you can [reach me through here](http://joseruiperez.me/contact.html).
# Machine learning challenge

This is a small challenge for the machine learning class of the complex systems master 
at ENS Lyon. There are two challenges: a classification challenge and a regression challenge. In both cases, the training data
is provided in the format of torch .pt files, that can be loaded with the `torch.load` function.

## Classification challenge

The inputs are points in 2 dimensional space, and the outputs are labels 0, 1, 2 and 3 (i.e., there are 4 classes).

## Regression challenge

The inputs are points in 2 dimensional space, and the outputs are real numbers. 


# Submission

For each problem (classification and regression), you will have to provide a python script
that takes as input a file containing the inputs, and outputs a file containing the predictions. 

The python file should be named `SURNAME_{problem}.py` where `{problem} = classification` or `{problem} = regression`
and should be called with the following command line:

```
python SURNAME_{problem}.py input_file
```

The script should generate a `SURNAME_{problem}.pt` torch file on the current folder
with a single tensor of size (N, 1) where N is the number of inputs. Submissions that fail to follow this format will
receive a score of 0.

The scripts should be sent to me by email by the 17th of October.


# Evaluation

The evaluation will be done by comparing the predictions of your script with the true labels on the test set.
The score will be calculated as

SCORE = test accuracy * 15 + ranking * 5.

- The test accuracy will be calculated as the fraction of correct predictions on the test set for the classification problem,
and as the mean squared error on the test set for the regression problem, normalized to be between 0 and 1.

- The ranking will be calculated by comparing your submission with the other submissions, 
and giving a score of k/N to the k-th best submission, where N is the number of submissions.
Note that the final SCORE is a number between 0 and 20.

# Mushroom-Dataset-DSG-problem-statement
The aim of this problem is to predict the class(poisonous or edible) of a mushroom given various variables (for eg. color and shape of the mushroom

### Identifying variable types and missing values(if any)
The target variable for the problem is 'class' which contains two categories- edible(e) and poisonous(p)
Description of various features is given in the repo as file 'Data Description.docx'
Detailed analysis of variables-
| Variable                   | dtype  | type     | no.of classes |
|----------                  |------- |------    |---------------|
| cap-shape                  | object |nominal   |  6            |
| cap-surface                | object |nominal   |  4            |
| cap-color                  | object |nominal   |  10           |
| bruises                    | object |nominal   |  2            |
| odor                       | object |nominal   |  9            |
| gill-attachment            | object |nominal   |  2            |
| gill-spacing               | object |nominal   |  3            |
| gill-size                  | object |ordinal   |  2            |
| gill-color                 | object |nominal   |  12           |
| stalk-shape                | object |nominal   |  2            |
| stalk-root                 | object |nominal   |  4            |
| radius                     | int64  |continous |  continous    |
| stalk-surface-above-ring   | object |nominal   |  4            |
| stalk-surface-below-ring   | object |nominal   |  4            |
| stalk-color-above-ring     | object |nominal   |  9            |
| stalk-color-above-ring     | object |nominal   |  9            |
| veil-color                 | object |nominal   |  4            |
| weight                     | int64  |continous |  continous    |
| ring-number                | object |ordinal   |  3            |
| ring-type                  | object |nominal   |  5            |
| spore-print-colo           | object |nominal   |  9            |
| population                 | object |nominal   |  6            |
| habitat                    | object |nominal   |  7            |

### Visualizations
Univariate analysis and bi-variate analysis is carried out for different variables using boxplots(for continous), scatterplots(for continous) and using seaborn factorplot and countplots for various inferences about  categorical features

### Data Pre-processing
Nominal features were one hot encoded using pandas getdummies method, ordinal feature were mapped using manual dictionaries
Missing values for weight were imputed using median of weights, whereas missing-values for stalk-root were imputed using<br> random-forest calssifier
New features were engineered by taking inferences from visualizations

### Modelling
One of the algorithms was selected from the following-
1)SVC
2)Random-Forest-classifier
3)Extra-trees Classifier
4)Logistic Regression

using cross-validation as a measure to select the suitable algorithm.
Random-forest classifier was finally used to make predictions on test-set






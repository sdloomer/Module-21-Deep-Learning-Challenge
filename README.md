# Module-21-Deep-Learning-Challenge
Neural Network Report

1. Purpose
    * The purpose of this analysis is to determine whether prospective clients will be successful in their endeavors if they are funded by Alphabet Soup using a neural network for predictions.

2. Results
    * Data Preprocessing
        * Target variable: The target variable that we will be predicting is the "IS_SUCCESSFUL" column
        * Feature variables: The feature variables are every other column in the dataframe
        * Variables to be removed: We are able to remove the "EIN" and "NAME" features/columns because they are irrelevant and are neither targets nor features to be considered.
    * Compiling, Training, Evaluating
        * I originally began with three layers, two hidden layers consisting of 16 neurons each and an output layer. I decided on using the "relu" activation function for both hidden layers because it is considered universal and a good starting point.
        * Unfortunately, I was not able to achieve target performance! I came very close, however, with an accuracy of around 73%.
        * For optimization, I made five adjustments:
            1. adjusted the cutoff value for the application counts to be replaced (from 100 to 1000).
            2. adjusted the cutoff value for the classification counts to be replaced as well (from 100 to 1000).
            3. added two more hidden layers for a total of 4 hidden layers and 5 total layers.
            4. increased the number of neurons in each layer (two hidden layers from 16 to 100).
            5. increased the number of epochs from 100 to 200.
3. Summary
    * The overall results of the optimized learning model are okay, with an accuracy of 73% and a loss of 63% (loss actually increased here from 56% in the initial model!). I would recommend optimizing the model further, perhaps utilizing even more hidden layers with an increased number of neurons (there are over 30,000 rows of data in the original CSV file, therefore a good model needs to be able to handle such large amounts of data with ease). I might also suggest using a different activation function as well; while ReLU is a good starting point, we might consider using the leaky ReLU function instead which characterizes normalized nonlinear values that are negative as well as positive (which we saw when we scaled the data). Because of these shortcomings, this model still needs some work and I would not recommend using it for any professional purposes.
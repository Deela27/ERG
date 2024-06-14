# ERG (this readme is for the ERG-complete file)
# Always remember to set x back to 0 after every run because the function it runs on the dataset depends on it.
# Steps before you run the function:
# 1. Check the Environment tab on the right to ensure x is 0.
# 2. Change file path to where your folder of csv files is. Make sure they are in alphabetical order. I recommend using A,B,C... to name the files so that step1 is A, Step3 is B and so on and forth.
# 3. Check the if conditions in the for loop to ensure they correspond to the order in which you performed your ERGs. x is the run number, that's why it starts from 0, so if you only performed steps 1,3,5,9, as opposed to steps 1,3,5,7,9, your condition for the first if condition will be x<=3 because that's where your first stage without a waves ends.
# 4. When you are done, save the dataframe in a csv file by running the function below the for loop.(check the path you are storing the file in and update the name of the file for each run)
# 5. Run the indicated code to empty the dataframe after every full run.

# The if conditions for the for loop are based on the following steps and ERG procedure:
# 1. The steps that were performed were 1,3,5,7,9,11,13,15,17,19,21,22,24 for dark adapted state.
# 2. 15,16,17,18,19,20,21,22,23,24 for the light adapted state, so all in all, 23 steps.
# The DA1to9 function only calculates b wave amplitude and impicit time, so I applied it to steps 1 to 11, which is when x is from 0-5.
# The DA13to24 function calculates b-wave and a-wave amplitudes and implicit times in the dark adapted state, so I apply it to steps 13-24, which is when x is 6 - 12.
# The LA function calculates b-wave and a-wave amplitudes and implicit times in the light adapted state, so I applied it to all the steps conducted in the light adapted state ie 15-24. which are any steps after x>=13.

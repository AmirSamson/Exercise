﻿# Exercise
This is a repo for tasks related to the exercise.

---------
## Exercise 1: 

1.   It does not print the fruit at the correct index, why is the returned result wrong?
2.   How could this be fixed?

#### Problem check and answer: 

The issue with the code is that all the fruits all in a set and the problem with a set is that it is not in an order. So, for returning the correct fruit name for each fruit id, we should use a List instead of a Set.

--------
## Exercise 2 

1   Can you spot the obvious error?
2   After fixing the obvious error it is still wrong, how can this be fixed?

#### Problem check and answer: 

The obvious error is:

 ```coords[:, 0], coords[:, 1], ... = coords[:, 1], coords[:, 1], ... ```

it should be:

 ```coords[:, 0], coords[:, 1], ... = coords[:, 1], coords[:, 0], ....```

Also, by printing out the "swapped_croods", we would get all the Y coordinates as all the X coordinates, which is wrong. (regarding that we only needed them to be flipped.)
And as a solution, we can copy each coords on the other side, so that we wouldn't have the same columns of Y(s) where the X column sits.

-------
## Exercise 3

1   For some reason the plot is not showing correctly, can you find out what is going wrong?
2   How could this be fixed?

#### Problem check and answer: 

For this matter, we can use the 'pandas' library to simplify the process of reading the CSV file and work with the data.

-------
## Exercise 4

1   Changing the batch_size from 32 to 64 triggers the structural bug.
2   Can you also spot the cosmetic bug?

#### Problem check and answer: 

The issue arises from the mismatch in the size of the labels provided to the loss function when training the discriminator. This happens because the generator generates samples with a different batch size than the real samples.

To fix this, we should adjust the size of the generated samples labels to match the batch size of the generator
As for the cosmetic bug, the code contains unnecessary try-except blocks and duplicated data loading for the MNIST dataset.

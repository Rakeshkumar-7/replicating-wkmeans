# Replicating <a href="https://ieeexplore.ieee.org/abstract/document/1407871">W-k-means</a> for Noise Reduction in clustering data

Replicated the W-k-means algorithm as proposed in its paper by Huang et. al

## Working demo
- Used a dummy dataset with two features x and y with 3 clusters
  ![Dummy dataset](https://github.com/Rakeshkumar-7/replicating-wkmeans/blob/main/images/x_y.png)
- Induced a random noise feature named "noise". Here's the noise plotted alongside the features x and y
  x vs noise             |  y vs noise
  :-------------------------:|:-------------------------:
  ![x vs noise](https://github.com/Rakeshkumar-7/replicating-wkmeans/blob/main/images/x_noise.png) |  ![y vs noise](https://github.com/Rakeshkumar-7/replicating-wkmeans/blob/main/images/y_noise.png)
- Ran the W-k-means algoirthm
  
  ![W-k-means result](https://github.com/Rakeshkumar-7/replicating-wkmeans/blob/main/images/original.png)

  The algorithm successfully detects the noise as the noise column(3rd) has substantially lesser weightage(and hence "influence") of 0.072 on the final outcome as compared to the other features

- I've also tried to initialize the weights by making it inversely proportional to their p-value(lesser p-value indicates more importance) instead of uniform weight initialization and got slightly better results

  ![W-k-means p-value weights init result](https://github.com/Rakeshkumar-7/replicating-wkmeans/blob/main/images/p_value.png)

  This time, the weight of the noise is 0.055 which is a slight improvement compared to before

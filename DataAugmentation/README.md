**[Generative Teaching Networks (GTN)](https://arxiv.org/abs/1912.07768)**

[GTN](https://arxiv.org/abs/1912.07768) is composed of a generator (i.e. teacher), which produces synthetic data, and a student, which is trained on this data for some task.

this notebook exposure to the following concepts:
1. **End-to-End Data Augmentation.** Data augmentation refers to the generation of more data from existing data to augment the training set. Examples of this with images include operations like random cropping and flipping. In this sense, the generator performs data augmentation by synthesizing data as extra training data.
2. **Curriculum Learning.** The generator not only can synthesize data from random noise, but also can learn this random noise, or curriculum. By backpropagating through the inputs, the generator can be trained to select the curricula that it deems will be best for student learning.
3. **Meta-Learning.** Meta-learning refers to "learning to learn," a broad field that optimizes over different learning tasks to find the best way to learn. You're probably an example of a good meta-learner :). A GTN accomplishes this by training the generator to understand how the student learns, demonstrated via curriculum learning.
4. **Neural Architecture Search.** But wait, there's still more! The generator doesn't just guide student training, it also can help determine the optimal student architecture (i.e. which layers, network depth). This concept of learning the best architecture is called Neural Architecture Search, or NAS. Pretty convenient, huh!
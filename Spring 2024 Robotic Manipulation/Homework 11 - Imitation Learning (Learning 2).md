## Problem Definition
The author addresses challenges in collecting real-world data, which is significant for training models which can generalize tasks. Traditional data collection for robotics involves task specific data collection, which do not leverage learning from large and various datasets. In addition, task generalization requires a high capacity model such as transformer. However, robotic controllers can't be run real-time with it sufficiently.

## Why the state-of-the-art is not enough for this? Why does it fail?

## What is the clever idea of this paper?
This method is open-ended, task-agnostic training combined with high-capacity. This approach allows the model to absorb a wide range of data, enabling it to generalize across different tasks, environments, and objects without the need for large, task-specific datasets.
## How the idea is implemented
RT is includes  encod high-dimensional inputs and outputs into compact token representations. This allows for real-time control and inference by making the model efficient enough to run on actual robots. The model is trained on a large-scale dataset collected from real robots performing a variety of tasks, demonstrating the model's ability to learn from diverse data and generalize effectively​​.
##  How is success proved and measured?

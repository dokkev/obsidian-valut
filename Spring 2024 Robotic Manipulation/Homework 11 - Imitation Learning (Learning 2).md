## Problem Definition
The author addresses challenges in collecting real-world data, which is significant for training models which can generalize tasks. Traditional data collection for robotics involves task specific data collection, which do not leverage learning from large and various datasets. In addition, task generalization requires a high capacity model such as transformer. However, robotic controllers can't be run real-time with it sufficiently.

## Why the state-of-the-art is not enough for this? Why does it fail?

## What is the clever idea of this paper?
open-ended, task-agnostic training combined with high-capacity architectures. This approach allows the model to absorb a wide range of data, enabling it to generalize across different tasks, environments, and objects without the need for large, task-specific datasets. The RT-1 model is designed to leverage large, diverse datasets to solve downstream tasks either zero-shot or with minimal task-specific data​​.
## How the idea is implemented

##  How is success proved and measured?

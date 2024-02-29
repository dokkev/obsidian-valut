
## Case Study: Pendulum Example
- Tradition ML would try to use autoencoder to reduce the dimension of the video (Pendulum) into a minimal latent state and recreate the video with known variables.
- Physics-informed ML will try to learn the diff-eqn (EOM) for how those coordinates evolve in time.
- Either we can make the model to learn the equation or bake the equation into the model.


## Five States of Machine Learning

1. Decide on problem (What are we modeling?)
2. Curate Data (What Data will inform the model?)
3. Design an architecture (RNN, Autoencoder, DMD, SINDy..)
4. Craft a loss function (What models are good?)
5. Employ Optimization (What algorithms to train model?)

- Training model means that we use optimization to tweak the parameters of our architecture to turn and learn the parameters of this architecture to minimize the loss function, averaged over our data.
	- In detail, our architecture is some class of functions that you can use to represent the input output relationships you want to model. So there are parameters that you can tune (weights of NN). And we use optimization to turn those parameters of the architecture to minimize the loss function averaged over your training data.

- Each of these five stages give unique opportunities for embedding physics into the process, and some cases for discovering physics.


#### Decide on Problem
- If you are modeling a physical problem such as pendulum, you are already embeddeding physics into ML


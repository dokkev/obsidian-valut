
1. Decide on problem (What are we modeling?)
2. Curate Data (What Data will inform the model?)
3. Design an architecture (RNN, Autoencoder, DMD, SINDy..)
4. Craft a loss function (What models are good?)
5. Employ Optimization (What algorithms to train model?)




### Case Study: Pendulum Example
- Tradition ML would try to use autoencoder to reduce the dimension of the video (Pendulum) into a minimal latent state and recreate the video with known variables.
- Physics-informed ML will try to learn the diff-eqn (EOM) for how those coordinates evolve in time.
- Either we can make the model to learn the equation or bake the equation into the model.





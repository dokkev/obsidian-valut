### Reinforcement Learning
RL algorithms don't know the reward function. The environment provides reward function.


## Imitation Learning
- Transition model : p(x_t | x_t-1, u_t-1)
- demonstration, z = {(x0,u0),(x1,u1)...}

### Behavior cloning
 - minimize different between robot actions and expert demonstration
 - Easy to implement but brittle against situations not observed in expert demonstration
### DAgger
- Address distributional mismatch by simply asking the expert for more demonstration
- Better approximate expert policy
- Re-train policy at every step


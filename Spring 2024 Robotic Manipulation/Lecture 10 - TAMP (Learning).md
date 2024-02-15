LLM is not grounded in reality (lack of connection to the real context)

## SayCan
Task grounding (say) → LLM (find a cleaner, find a sponge...) -> Value Functions ← world grounding (Can)
### Related work
- LLM-based planning without grounding
- Fine-Tune LLM to Ground
- Learning-based Symbolic TAMP
- Hierarchical RL
### Problem Setting
- user provided natural language instruction
- current state: S
- Set of skills:  Π
- Goal is to compute task grounding (Say) and world grounding (Can)
### Task Grounding
- Prompt Engineering
- Instruction
- Score for relevant skills
### World Grounding using Value Functions
- Value function is trained via RL (Q-learning)
- 
# Robust Multi-Agent Reinforcement Learning via Minimax Deep Deterministic Policy Gradient 

This is the code for implementing the M3DDPG (mmmaddpg) algorithm. 
The code is modified from https://github.com/openai/maddpg

For Multi-Agent Particle Environments (MPE) installation, please refer to https://github.com/openai/multiagent-particle-envs

- To run the code, `cd` into the `experiments` directory and run `train.py`:

``python train.py --scenario simple``

- You can replace `simple` with any environment in the MPE you'd like to run.

### Command-line options

#### Environment options

- `--scenario`: defines which environment in the MPE is to be used (default: `"simple"`)

- `--max-episode-len` maximum length of each episode for the environment (default: `25`)

- `--num-episodes` total number of training episodes (default: `60000`)

- `--num-adversaries`: number of adversaries in the environment (default: `0`)

- `--good-policy`: algorithm used for the 'good' (non adversary) policies in the environment
(default: `"maddpg"`; options: {`"mmmaddpg"`, `"maddpg"`, `"ddpg"`})

- `--adv-policy`: algorithm used for the adversary policies in the environment
(default: `"maddpg"`; options: {`"mmmaddpg"`, `"maddpg"`, `"ddpg"`})

#### Core training parameters

- `--lr`: learning rate (default: `1e-2`)

- `--gamma`: discount factor (default: `0.95`)

- `--batch-size`: batch size (default: `1024`)

- `--num-units`: number of units in the MLP (default: `64`)

- `--adv-eps`: adversarial rate against competitors

- `--adv-eps-s`: adversarial rate against collaborators 


## Proximal Policy Optimization RL
This repo will automatically utilize PyTorch to use multiple GPUs if available.

### Installation using UV
```bash
uv venv
source .venv/bin/activate
uv sync
```

### To push to online providers:

#### huggingface
`huggingface-cli login` after creating an identity token at [huggingface.co](https://huggingface.co/kismet163/ReinforcePPO)

#### wandb
```bash
wandb login
```

## Running

###  Pybullet Cheetah Environment (default)
```bash
uv run main.py
```

###  Mujoco Walker2D Env with WandB tracking
```bash
uv run main.py --track --env-id "Walker2DMuJoCoEnv-v0"
```


### *** DEPRECATED (See Discrete Branch) *** ###
### Only for Discrete (see MAIN branch prior to PR)
```bash
uv run main.py --env-id "CartPole-v1"
```
to specify the CartPole-v1 environment instead. 

### Doom (todo)
Doom Environment
```bash
uv run main.py --env-id doom
```


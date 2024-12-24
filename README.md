## Proximal Policy Optimization RL
This repo is my implementation of PPO, mainly from the HuggingFace RL Course.

The main script will automatically utilize PyTorch to use multiple GPUs if available.

### Environments and Metrics
The environments are available from [PyBullet-Gym](https://github.com/benelot/pybullet-gym).
Unfortunately I could not get the Mujoco envs to work no matter what Gym and PyBullet / Mujoco combinations I used.
In the the mean time PyBullet will need to suffice as this is a known issue. 
At least until I can test [Genesis World Model](https://github.com/yizhouzhao/genesis/blob/main/examples/locomotion/go2_env.py) which can create massively parallel physics sims, capable of setting up vectorized gym-like environments (see example). 


HuggingFace Metrics (showing the results and a video of performance) at: [huggingface.co](https://huggingface.co/kismet163/ReinforcePPO)  
WandB (Weights & Biases) Metrics (showing training info such as the loss convergenge, GPU use, etc) at: [WandB.ai](https://wandb.ai/chance-cardona/PPO-RL?nw=nwuserchancecardona)  


### Installation (UV)
```bash
uv venv
source .venv/bin/activate
uv sync
```

### Login to Online Services:

#### huggingface
`huggingface-cli login` after creating an identity token at 

#### wandb
```bash
wandb login
```

## Running (Training and Evaluating)

###  Pybullet Cheetah Environment (default)
```bash
uv run main.py
```

###  Bullet Humanoid Env with WandB tracking
```bash
uv run main.py --track --env-id "HumanoidBulletEnv-v0"
```


### *** DEPRECATED (See Discrete Branch) ***
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


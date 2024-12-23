## Proximal Policy Optimization RL
This repo will automatically utilize PyTorch to use multiple GPUs if available.

### Installation using UV
```bash
uv venv
uv pip install -r requirements.txt --break-system-packages
```

### To push to huggingface
`huggingface-cli login` after creating an identity token at [huggingface.co](https://huggingface.co/kismet163/ReinforcePPO)


## Running
LunarLander Environment (default)
```bash
uv run main.py --env-id "CartPole-v1"
```

Doom Environment
```bash
uv run main.py --env-id doom
```


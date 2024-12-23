## Proximal Policy Optimization RL

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
python3 main.py
```

Doom Environment
```bash
python3 main.py -e doom
```


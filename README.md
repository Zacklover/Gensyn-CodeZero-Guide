# Gensyn-CodeZero-Guide
The cleanest, guide to run &amp; upgrade Gensyn RL-Swarm + CodeZero on Mac/Linux 
# 🚀 Gensyn RL-Swarm + CodeZero Guide (Mac & Linux)  
*The cleanest, battle-tested guide on the internet — made with Grok*

Tired of messy threads and outdated Notion docs? This repo gets your node running and upgraded in minutes.

Currently on the **CodeZero release** (latest as of December 2025).

## Why Run Gensyn RL-Swarm?
- Earn testnet points → future airdrop
- Help train frontier AI models on your GPU/CPU
- Fully decentralized — no AWS, no permission

## ⚡ One-Command Upgrade (Latest CodeZero)

```bash
# 1. Reattach to your screen
screen -r gensyn

# 2. Stop the node (Ctrl+C)

# 3. Go to folder
cd rl-swarm

# 4. Kill old environment
deactivate 2>/dev/null || true
rm -rf .venv

# 5. Pull latest CodeZero release
git switch main
git reset --hard
git clean -fd
git pull origin main

# 6. Rebuild venv
python3 -m venv .venv
source .venv/bin/activate

# 7. Launch (you're back online!)
./run_rl_swarm.sh

Common FixesIssue
Fix
"Terminated" error
→ See troubleshooting section below
Out of memory
Use a VPS with ≥16GB RAM or add swap
Node not submitting
Make sure port 3000 & 5000 are open + wallet configured

Troubleshooting "Terminated" ErrorRun this to see real logs:bash

tail -f ~/.gensyn/logs/*.log

Most fixes: restart screen session + re-run ./run_rl_swarm.shMade with  by the Gswarm


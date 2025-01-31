# AI Model UI

## Introduction
Intension is to explore easy way to interact with Open source models downloaded to local machine. All the notes here are with respect to my MacOS machine.
Found [Open WebUI](https://github.com/open-webui/open-webui) as one of the best as it allows to interact with multiple models at same time for comparision. Love that feature!

## Installation
You can install container managment software like [OrbStack](https://orbstack.dev/download) which come with docker. After installation, clone this git repo and you can open Terminal and run command
```
docker compose up -d
```


## Janus Pro on Mac OS (My notes)

### Step 1 - Install Anaconda
Using official [website](https://docs.conda.io/projects/conda/en/stable/user-guide/install/index.html#) download and install anaconda

### Step 2 - Create an conda environment
Open Terminal and execute below command
```
conda create --name janus python=3.12
```

### Step 3 - Switch to the new conda environment
```
conda activate janus
```

### Step 54 - Clone the Janus github repo
```
git clone https://github.com/deepseek-ai/Janus.git
cd Janus
```
(Optional) The default model is Janus-Pro-7B. If you wish to change to 1B model then modify the line in same file from ``model_path = "deepseek-ai/Janus-Pro-7B"`` to ``model_path = "deepseek-ai/Janus-Pro-1B"``

### Step 6 - Install all packages
```
pip install -e .
```

### Step 7 - Run Janus Pro
```
python generate.py
```

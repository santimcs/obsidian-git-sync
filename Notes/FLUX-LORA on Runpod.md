Go to RunPod

Use On-demand - Community Cloud

Runpod pytorch:2.2.0-py3.10-cuda12.1.1-devel-ubuntu22.04

1 x 4090

Change pod name to 4090 AI-toolkit

Set container & volume disk to 80 GB Disk
80 GB Pod Volume

Deploy On-Demand

Connect to Jupyter Lab [Port 8888]

goto https://github.com/ostris/ai-toolkit

1.Setup

copy these commands to workspace & run

git clone https://github.com/ostris/ai-toolkit.git
cd ai-**toolkit****
git submodule update --init --recursive
python -m venv venv
source venv/bin/activate
pip install torch
pip install -r requirements.txt
pip install --upgrade accelerate transformers diffusers huggingface_hub 

Stop the pod and start again
cd to ai-toolkit folder
pip install -r requirements.txt

### 2. Upload your dataset

[](https://github.com/ostris/ai-toolkit#2-upload-your-dataset)

- Create a new folder in the root, name it `NDR_BNI` or whatever you like.
- Drag and drop your .jpg, .jpeg, or .png images and .txt files inside the newly created dataset folder.

### 3. Login into Hugging Face with an Access Token

[](https://github.com/ostris/ai-toolkit#3-login-into-hugging-face-with-an-access-token)

- Get a READ token from [here](https://huggingface.co/settings/tokens) and request access to Flux.1-dev model from [here](https://huggingface.co/black-forest-labs/FLUX.1-dev).
- Run `huggingface-cli login` and paste your token.
- Answer Y
	under folder workspace create new folder name
		`NDR_BNI`
	double click new folder and drag required pictures to this dataset folder
	click plus tab and click text 
	Insert `NDR_BNI' into text file & create 3 more files with same content 

### 4. Training

[](https://github.com/ostris/ai-toolkit#4-training)

- Copy train_lora_flux_24gb.yaml config file located at `config/examples`  and rename it to NDR_BNI_test.yaml.
- Move it to config folder
- Edit the config following the comments in the file.
- Change `folder_path: "/workspace/NDR_BNI"` 
- Go to workspace & Run the file: `python run.py config/NDR_BNI_test.yaml`.
- Go to samples/output/NDR_BNI_test_1







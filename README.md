# CloudCap3D: Enhancing 3D In-Scene Descriptions via Point Cloud Integration and Efficient Text Filtering
![hrc7u-k1v2r](https://github.com/OpenMICG/CloudCap3D/blob/main/1.pdf)

# Usage

## 1. Requirements
    git clone https://github.com/OpenMICG/SwiftCraft3D.git

    cd SwiftCraft3D
    
    conda create -n SwiftCraft3D python=3.8

    conda activate SwiftCraft3D

    pip install torch==2.3.1 torchvision==0.18.1 torchaudio==2.3.1 --index-url https://download.pytorch.org/whl/cu121

    pip install -r requirements.txt

## 2. Train
Our training data is sourced from the [Objaverse dataset](https://objaverse.allenai.org/objaverse-1.0/), and the subtitles are derived from [Cap3D](https://github.com/crockwell/Cap3D?tab=readme-ov-file). Execute the following command to initiate the training:

    accelerate launch train.py  \
    --mixed_precision="fp16" \
    --pretrained_model_name_or_path="stabilityai/stable-diffusion-xl-base-1.0"  \
    --train_data_dir="/path/to/dataset" --caption_column="text"  \
    --resolution=1024 --random_flip  \
    --resume_from_checkpoint=latest \
    --train_batch_size=2 --num_train_epochs=10 --checkpointing_steps=1000  \
    --learning_rate=1e-06 --lr_scheduler="constant" --lr_warmup_steps=0  \
    --output_dir="/path/to/output"

## 3. Inference
The following command generates an OBJ file with vertex colors：

    python inference.py "input text" name

By executing the following command, a higher quality 3D mesh is generated and the OBJ, MTL, and PNG files are exported:

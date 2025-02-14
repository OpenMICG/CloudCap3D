# CloudCap3D: Enhancing 3D In-Scene Descriptions via Point Cloud Integration and Efficient Text Filtering
![](https://github.com/NZY7/HelloPrj/blob/master/compare.png)
We publicly release the CloudCap3D dataset. The motivation for creating this dataset is to address the issue of low-quality and semantically poor generated text caused by the lack of 3D point cloud data. We leverage the existing Objaverse dataset and expand it into CloudCap3D, a dataset with 3D object-text pairs, providing a large number of 3D object-text pairs with richer semantics.
The dataset can be used for 3D multimodal tasks.
# CloudCap3D Download
You can download CloudCap3D from [here](https://drive.google.com/file/d/1U1Na1bbrDP1hli3LzZAAFkn6XwfkC9L3/view?usp=sharing).
# Evaluation metric
Traditional evaluation metrics often focus narrowly on specific aspects, such as the alignment between a generated 3D object and the corresponding text, which may not accurately reflect human judgments. Recent research has highlighted the potential of using GPT-4V for evaluating text-to-3D object generation tasks, as it offers a more comprehensive assessment that better mirrors human preferences. Building on these findings, we have adopted and
refined the cue word methodology proposed in previous studies.
# Anckowledgement
This repo is based on [GPT-4](https://openai.com/index/gpt-4/), [CG3D](https://github.com/deeptibhegde/CLIP-goes-3D), [PointLLM](https://github.com/OpenRobotLab/PointLLM), [BLIP2](https://github.com/OpenRobotLab/PointLLM), [GPT-4V](https://github.com/3DTopia/GPTEval3D). We would like to express our gratitude for their outstanding work.

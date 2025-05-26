# DialogueMMT
DialogueMMT: Dialogue Scenes Understanding Enhanced Multi-modal Multi-task Tuning for Emotion Recognition in Conversations<br>
## Dataset
You need to process the data into the instruction tuning format as described in the paper.
| DataSet | Usage Modal |Task|
|----------|----------|----------|
| [MELD](https://github.com/declare-lab/MELD)  | Video&Texual|ERC&ASD|
| [EmoryNLP](https://github.com/emorynlp/character-mining)  |Texual |ERC|
| [IEMOCAP](https://sail.usc.edu/iemocap/) |Texual|ERC|
| [AffectNet](https://mohammadmahoor.com/affectnet/)  |Image|FER|
| [STAC](https://www.irit.fr/STAC/corpus.html)  |Texual|DDP|
| [Molweni](https://github.com/HIT-SCIR/Molweni)  |Texual|DDP|
## Backbone Model
You can use the following [link](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.2) to download the model.
## Run Steps
We utilize the codes from [here](https://github.com/DAMO-NLP-SG/VideoLLaMA2) to finetune model. You can run:
```bash
bash scrips/custom/finetune_lora.sh
```
You need to replace:
```bash
--model_path --vision_tower --pretrain_mm_mlp_adapter --data_path --output_dir
```
with your file_path
## Citation
Our code and datasets are based on [VideoLLaMA2](https://github.com/DAMO-NLP-SG/VideoLLaMA2). We appreciate the great help of this work. If you use the code of this work, please cite using this BibTeX:
```bash
@article{damonlpsg2024videollama2,
  title={VideoLLaMA 2: Advancing Spatial-Temporal Modeling and Audio Understanding in Video-LLMs},
  author={Cheng, Zesen and Leng, Sicong and Zhang, Hang and Xin, Yifei and Li, Xin and Chen, Guanzheng and Zhu, Yongxin and Zhang, Wenqi and Luo, Ziyang and Zhao, Deli and Bing, Lidong},
  journal={arXiv preprint arXiv:2406.07476},
  year={2024},
  url = {https://arxiv.org/abs/2406.07476}
}
```

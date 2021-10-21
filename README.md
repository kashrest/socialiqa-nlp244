# RoBERTa transformer model for Social IQA Social Commonsense Reasoning task
Project for NLP 244: Advanced Machine Learning course (NLP 244) with Professor Dilek Hakkani-Tur at UC Santa Cruz.
Incoporating knowledge graphs and commonsense task transfer learning, for the SocialIQA task [1].
Authors: Morgan Eidam, Tianxiao Jiang, and Kaleen Shrestha. 

# Instructions
Unzip the zip files containing the train/dev splits for the aNLI, HellaSwag, and SocialIQA tasks.

To replicate our code, run main.ipynb:
Run the optional cell at the top to download required packages if not installed.
Then, run all cells up to, but not including 'Phase 1'.

For all the experiments afterwards, they might require a checkpoint. If no checkpoint is present, you can fine-tune from scratch by commenting out the torch.load and model.load_state lines. Please modify the path to the checkpoint if checkpoints have been stored.

# Methodology
Our model is a RoBERTa-base model that is pretrained on both ATOMIC and ConceptNet using a masked language model objective, then finetuned on the HellaSwag task and dataset, aNLI task and dataset, and finally the Social IQA task and dataset.

# Results
Our best model (RoBERTa-base finetuned on: ATOMIC + ConceptNet --> HellaSwag --> aNLI --> Social IQA) achieves 71% accuracy on the Social IQA development test. Our hypothesis as to why accuracy is not improved from our baseline model (RoBERTa-base finetuned on only Social IQA) is that RoBERTa-base is pretrained on 160GB of data, and so the relatively few examples we trained on in each fine-tuning stage did not make a big-enough difference.

# Future work
It currently (October 2021) achieves ~20% accuracy on the Social IQA test set, and is still being investigated. Human performance on the Social IQA test set is 88.1% accuracy, while the leader on the leaderboard has 83.1%. It would be interesting to see how to improve the performance of computer models, and what innovative techniques might be required to bridge that gap.

# References
[1] Sap, Maarten et al. “Social IQA: Commonsense Reasoning about Social Interactions.” EMNLP 2019 (2019).
[2] Chang, Ting-Yun et al. “Incorporating Commonsense Knowledge Graph in Pretrained Models for Social Commonsense Tasks.” ArXiv abs/2105.05457 (2020): n. pag.
[3] Lourie, Nicholas et al. “UNICORN on RAINBOW: A Universal Commonsense Reasoning Model on a New Multitask Benchmark.” AAAI (2021).

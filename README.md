# socialiqa-nlp244
Project for NLP 244: Advanced Machine Learning course (NLP 244) with Professor Dilek Hakkani-Tur at UC Santa Cruz.
Incoporating knowledge graphs and commonsense task transfer learning, for the SocialIQA task [1].
Authors: Morgan Eidam, Tianxiao Jiang, and Kaleen Shrestha. 
Final paper: Not yet completed.

# Instructions
To replicate our code, run main.ipynb:
Run the optional cell at the top to download required packages if not installed.
Then, run all cells up to, but not including 'Phase 1'.

For all the experiments afterwards, they might require a checkpoint. If no checkpoint is present, you can fine-tune from scratch by commenting out the torch.load and model.load_state lines. Please modify the path to the checkpoint if checkpoints have been stored.

# References
[1] Sap, Maarten et al. “Social IQA: Commonsense Reasoning about Social Interactions.” EMNLP 2019 (2019).

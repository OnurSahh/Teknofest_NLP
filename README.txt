#Acikhack2023

We first downloaded a turkish bert model from hugginface. Then we finetuned it with these parameters:

|||
training_args = TrainingArguments(
        output_dir='./results',          # output directory
        num_train_epochs=5,              # total number of training epochs
        per_device_train_batch_size=4,   # batch size per device during training
        per_device_eval_batch_size=4,    # batch size for evaluation
        warmup_steps=500,                # number of warmup steps for learning rate scheduler
        weight_decay=0.01,               # strength of weight decay
        logging_dir='./logs',            # directory for storing logs
        logging_steps=10,
        evaluation_strategy='epoch'
)

trainer.train()

Epochs / Training Loss / Validation Loss / Accuracy

   1   / 0.254800      /  0.611020       /  0.916565
   2   / 0.016300      /  0.722202       /  0.902727
   3   / 0.000100      /  0.660347       /  0.923077
   4   / 0.000100      /  0.672700       /  0.929182
   5   / 0.000100      /  0.711997       /  0.927147
   
|||


TEKNOFEST_train.ipynb was used for fine tuning a turkish bert model.

Fine tuned huggingface model link can be found in the "model link.txt" file.

Required libraries can be seen in the "requirements.txt" file

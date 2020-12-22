The code base covers both the mid term and final report material. 

1. Final report work:
The final report work involves running the Bluebert model and the AbbreviationInfusion.ipynb file which can be found at this path: ./nlidata/

Since the model checkpoints files are huge in size, they have not been included in this submission. It can be provided upon request. 



2. Mid term report work:

The two folders contain the code to run train and test the BlueBERT model. 

It also contains the python notebook (.ipynb) files to perform data preprocessing as the BlueBERT model needs the files in the .tsv format instead of the .jsonl format. 


Instructions to run the Model:

-> Use the following set of commands:

  python bluebert/run_bluebert.py \
  --do_train=true \
  --do_eval=true \
  --do_predict=true \
  --task_name="mednli" \
  --vocab_file= $model_location/vocab.txt \
  --bert_config_file= $model_location/bert_config.json \
  --init_checkpoint= $model_location/model.ckpt-3509\
  --num_train_epochs=10.0 \
  --data_dir=/home/jupyter/nlidata/ \
  --output_dir= %output_location \
  --do_lower_case=true

**replace $model_location with the exact model path
** replace $output_location with the preferred output path

-> To run this you might need model checkpoints trained on our data which can be shared when required.

-> The data used for this model needs to be converted from json to tsv and the data preprocessing and evaluation part can be found in the folder nlidata/


-> To preprocess data according to the needs of the model, divide your data into train, test and dev and add them to the respective folder : nlidata/nliraw/ and run the train test.ipynb notebook file.



-> Evaluation can be performed using file evaluationMatrix.ipynb notebook file. 

-> We have also provided some utility files to perform minor functions like converting json to tsv which can be used as per the needs.

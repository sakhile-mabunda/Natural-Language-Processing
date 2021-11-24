# Natural-Language-Processing
Local Language NLP

How to run the code:

Step 1: ->Import the notebook to google colab

Step 2: ->depending on which tokenization strategy you want to run the model with
	->Under "Creating the JoeyNMT Config"
		if you want to run with char replace the data section with
		
		data:
    			src: "{source_language}"
    			trg: "{target_language}"
    			train: "data/{name}/train.char"
    			dev:   "data/{name}/dev.char"
    			test:  "data/{name}/test.char"
    			level: "char"
    			lowercase: False
    			max_sent_length: 100
    			src_vocab: "data/{name}/m_char.vocab"
    			trg_vocab: "data/{name}/m_char.vocab"

		else if it's bpe replace the data section with
		
		data:
    			src: "{source_language}"
    			trg: "{target_language}"
    			train: "data/{name}/train.bpe"
    			dev:   "data/{name}/dev.bpe"
    			test:  "data/{name}/test.bpe"
    			level: bpe
    			lowercase: False
    			max_sent_length: 100
    			src_vocab: "data/{name}/vocab.txt"
    			trg_vocab: "data/{name}/vocab.txt"

		else if it's bpe with drop out replace the data section with
		
		data:
    			src: "{source_language}"
    			trg: "{target_language}"
    			train: "data/{name}/train.dropout.bpe"
    			dev:   "data/{name}/dev.dropout.bpe"
    			test:  "data/{name}/test.dropout.bpe"
    			level: bpe
    			lowercase: False
    			max_sent_length: 100
    			src_vocab: "data/{name}/vocab.dropout.txt"
    			trg_vocab: "data/{name}/vocab.dropout.txt" 

		else if it's word replace the data section with
		
		data:
    			src: "{source_language}"
    			trg: "{target_language}"
    			train: "data/{name}/train.word"
    			dev:   "data/{name}/dev.word"
    			test:  "data/{name}/test.word"
    			level: word
    			lowercase: False
    			max_sent_length: 100
    			src_vocab: "data/{name}/m_word.vocab"
    			trg_vocab: "data/{name}/m_word.vocab" 

Step 3 : ->Run all cells
Step 4 : ->You will uploaad the evaluationg and training datasets on one of the cells
Step 5 : ->Sit back and wait for the model to run.

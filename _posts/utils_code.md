### parsing

* ./parsing/main.sh

### Entity Detection (After parsing)


* get_sentences_with_POS.py: 
	-input: the output of stanford parser
	-output: 1) a file for each sentence. 2) a file for each POS in sentence.

* entity_candidate_generation_using_Conll_Chunker: 
	-dependency: Textblob, textblob.np_extractors.ConllExtractor
	-input: a file for each sentence (output 1) from get_sentences_with_POS.py)
	-output: a file with each line represents a syntactized sentences and NP in it
	-**note: using Conll Chunker will automatically change the NP to lower case.**


* [NEW] entity_candidate_generation_using_Fast_Chunker:
	-input: a file for each **document**
	-output, a file with each line represents a sentence, showing the doc_id-sentence_id    syntactized sentences    NP in this sentences.
	-**Please change the NP Chunker in Textblob to avoid the lower case conversion**
	-**The function "def noun_phrases(self):" under path "~/anaconda/lib/python2.7/site-packages/textblob/blob.py"**

	






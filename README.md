# DBpedia-Chatlog-Analysis
Discourse analysis for DBpedia chatbot: http://chat.dbpedia.org/

#### Description of notebooks:

  1. [data_exploration.ipynb](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/data_exploration.ipynb) houses code for grouping chats w.r.t. user_id and for preliminary analysis, such as, finding average length of conversation and number of users.  

  2. In [analysis.ipynb](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/analysis.ipynb), we find -
      * the most used channel (web/slack/facebook messenger)
      * no. of failed responses per conversation and no. of questions that did not satisfy users 
      * Conversation length after a negative feedback
      * character length of user-requests
      * perform NER and find commonly asked topics - plot distribution
      * if coreferences exist
      * the language of user-requests
   
   3.  Use [dependency_parsing.ipynb](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/dependency_parsing.ipynb) to get the estimate of the number of complex questions asked and to prepare input (candidate pairs) for intent clustering. 
   
   4. The [clustering](https://github.com/dice-group/DBpedia-Chatlog-Analysis/tree/master/clustering) folder contains 2 implementations ([KMeans](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/clustering/K-means.ipynb) and [HDBSCAN](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/clustering/HDBSCAN.ipynb)) for finding the latent-intents in utterance representations. Use [get_sentence_embeddings.ipynb](https://github.com/dice-group/DBpedia-Chatlog-Analysis/blob/master/clustering/get_sentence_embeddings.ipynb), preferably on [Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb#recent=true), to fetch sentence embeddings for clustering user-requests based on their semantics. 

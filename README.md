# Scholarly, A voice-based search engine for research papers.

Google Scholar, Microsoft Academic, ResearchGate are the popular research-based search engines. But none of them have a voice search option. In this project, we will build a voice-based search engine which retrieves research papers from an index and provides the summary of first N papers, through voice and text. 

Method: 

We train a custom Automatic Speech Recognition(ASR) system using Transfer Learning, and use this to recognize voice based queries. 
The UI will be designed to integrate both text and voice based queries
The flask based APIs process the user queries and search the keywords from ElasticSearch Index. Refer the API list below:
API 1 - ASR API. Accepts the speech query from the UI
API 2 - Accepts the texts query from the UI (API 1 & 2 can be combined later)
API 3(Function) -  Preprocess the user query. This step involves stop word removal, stemming/lemmatization.
API 4 - Searches the preprocessed query from the ES index  and pushes the results to the UI
The UI displays the search results, including a summary and rank/score of each result
The read aloud API will read out the top N retrieved paper titles, location, and a brief summary of the paper.

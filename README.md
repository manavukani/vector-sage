# VectorSage

> Unlock knowledge from your documents with a powerful question-answering system.

VectorSage provides a robust question-answering framework for resolving ambiguities within your document sets. It leverages cutting-edge RAG framework with LangChain, Bedrock Vector Embeddings and Chroma DB to transform your files into a powerful question-answering system. You can load your documents, from scientific papers to legal contracts, and ask insightful questions. VectorSage will analyze the information and provide tailored responses, empowering you to discover knowledge across diverse domains.

![VectorSage](https://github.com/user-attachments/assets/a7e725b8-cc80-42cb-baae-1bd6e65aa8b7)


## Setup

1. Clone the repository, using the command:
``` bash
git clone https://github.com/manavukani/vector-sage.git
```

2. Install the dependencies using the following command:
```bash
pip install -r requirements.txt
```

3. Add your documents to the (data)[data] folder.


### Files and Their Functionality

#### 1. get_embedding_function.py
This file contains the function `get_embedding_function()` which initializes and returns the embedding function using BedrockEmbeddings. This function is crucial for embedding text data for the vector database. (You can check other embedding functions [here](https://python.langchain.com/v0.1/docs/integrations/text_embedding/))

#### 2. populate_database.py
This script is responsible for populating the vector database with documents. It includes functionality to load documents from a directory, split them into chunks, and add them to the Chroma vector store. It also provides an option to reset the database. (You can check how to load documents other than PDF [here](https://python.langchain.com/v0.1/docs/modules/data_connection/document_loaders/pdf/)).

#### 3. query_data.py
This script handles querying the vector database. It takes a query text as input, retrieves relevant documents from the vector store, and generates a response using a language model.


#### 4. test_rag.py
This script contains tests for the `query_rag` function. It uses predefined questions and expected responses to validate the functionality of the query system.

### Usage

1. **Populate the Database**:
   ```bash
   python populate_database.py --reset
   ```

2. **Query the Database**:
   ```bash
   python query_data.py "Your query here"
   ```

3. **Run Tests**:
   ```bash
   pytest test_rag.py
   ```


### Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

### Support
If you encounter any problems or have any suggestions, please open an issue in this repository.

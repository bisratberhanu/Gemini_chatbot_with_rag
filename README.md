# Chatbot with Gemini and RAG

## Overview

This project is a chatbot built using the Gemini framework and incorporates Retrieval-Augmented Generation (RAG) to enhance the chatbot's responses by retrieving relevant information from a knowledge base.
The research paper named [**Attention is All You Need**](https://arxiv.org/abs/1706.03762) is used as a RAG input.

The collab notebook includes basic code to interact with the chatbot and ask questions. The chatbot will respond with the answer to the question.

The code includes basic queries with out RAG and then shows the basic steps to implement RAG to enhance the chatbot responses.
the steps include:
- uploading a pdf file - which will be used as a knowledge base
- extracting the text from the pdf file
- creating chunks of text from the extracted text
- create embeddings for the chunks
- creating an  index for the embeddings
- creating a retriever
- storing in a vector database
- retrieving the answer to the question using the retriever

## Features

- **Natural Language Understanding**: Leverages google Gemini for understanding user queries.
- **Retrieval-Augmented Generation (RAG)**: Enhances responses by retrieving relevant documents from a knowledge base.

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/bisratberhanu/Gemini_chatbot_with_rag.git
    cd Gemini_chatbot_with_rag
    ```


2. **Set up environment variables**:
    Create a `.env` file in the root directory and add the necessary environment variables:
    ```env
    GEMINI_API_KEY=your_gemini_api_key
    ```
    - add the pdf file(attention is all you need) to the root directory

3. **usage**:
  - run all the cells of  google python notebook file
  - It is recomended to run the code in google colab notebook
  
5. **example**:
  - run the code in google colab notebook
  - enter the question you want to ask the chatbot
  ```python
    question = "Describe Random forest?"
    result = qa_chain({"query": question})
    Markdown(result["result"])
  ```
  - the chatbot will respond with the answer
  ```
  Random forest is a supervised learning algorithm that builds an ensemble of decision trees and outputs the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.
  ```
  
## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Gemini](https://gemini.com) for the natural language understanding framework.
- [RAG](https://arxiv.org/abs/2005.11401) for the retrieval-augmented generation concept.

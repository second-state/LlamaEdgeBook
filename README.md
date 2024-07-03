![License](https://img.shields.io/badge/license-MIT-green)

# LlamaEdgeBook: Generate entire books in seconds using OpenAI-like API server

**This project is from [Groqbook by Bkieger](https://github.com/Bklieger/groqbook)**
 
Groqbook is a streamlit app that scaffolds the creation of books from a one-line prompt using Llama3 on Groq. It works well on nonfiction books and generates each chapter within seconds. 

**We have made Groq book can work with any OpenAI-like API server, like LlamaEdge and GaiaNet node. We also improved the prompts to make it can generate book well.**

[Demo of LlamaEdgeBook](https://github.com/Bklieger/groqbook/assets/62450410/3adb11cd-8264-4289-a28a-49dc5b3cf453)
> Demo of LlamaEdgeBook using a GaiaNet node running Gemma-2-9b on NVIDA T4 


### How to run it

Before you run it, you will need to have access to an OpenAI-like API server.

* [Quick start with LlamaEdge](https://llamaedge.com/docs/user-guide/quick-start-command). Your LLM API base URL will be `http:localhost:8080` using LlamaEdge.
* [Qucik start with GaiaNet](https://docs.gaianet.ai/node-guide/quick-start). The base URL for your LLM API will be a publicly accessible one, employing GaiaNet.

**Step 1: set up the environment**

Use the following command line to get source code and install the necessary dependencies.

```
git clone https://github.com/second-state/LlamaEdgeBook.git
cd LlamaEdgeBook

pip install -r requirements.txt
```
**Step 2: Set up the LLM**

Use the following command line to set uo the LLM for generating book.
```
export OPENAI_BASE_URL="https://0x57b00e4f3d040e28dc8aabdbe201212e5fb60ebc.us.gaianet.network/v1"
export OPENAI_MODEL_NAME="gemma-2-9b-it-Q5_K_M"
export OPENAI_API_KEY="NA"
```
**Step 3: Run the application**

```
streamlit run main.py
```
If it runs successfully, you will can see the following output.

```

Collecting usage statistics. To deactivate, set browser.gatherUsageStats to false.


  You can now view your Streamlit app in your browser.

  Local URL: http://localhost:8501
  Network URL: http://10.128.0.8:8501
  External URL: http://35.222.115.181:8501
```

Then, you can open `http://localhost:8501` in your browser to generate a book by entering your prompt.

### Features

- 📖 Support all the open source LLMs
- 🖊️ Uses markdown styling to create an aesthetic book on the streamlit app that includes tables and code 
- 📂 Allows user to download a text or PDF file with the entire book contents

### Example Generated Books:

| Example                                      | Prompt                                                                                                                                |
| -------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| [cookbook]()             |  How to make a chicago style sandwich                                    |

---



## Details


### Technologies

- Streamlit
- OpenAI 
- LlamaEdge

## Contributing

Improvements through PRs are welcome!

## Cedits

Thanks Bkieger for crearting [groqbook](https://github.com/Bklieger/groqbook). 

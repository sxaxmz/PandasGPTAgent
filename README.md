# PandasGPTAgent
Chat with your data utilizing powerful AI capabilities (OpenAI &amp; LangChain).

![PandasGPTAgent Demo](media/PandasGPTAgent.gif)

This tool utilizies powerful GPT model along with utilization of LangChain Agent to create a friendly UI to improve the experience and facilitate the usage of GPT models over various data files such as CSV, XLSX, or XLS.


This tool is the first UI prototype created for any Pandas Agent available for public to demonstrate the capabilities of what can be implemented. The focus here is on defining and extracting data from PandasGPT Agent to be integrated or embedded into existing systems.

Demonstration from [here](https://sxaxmz-pandasgptagent-app-prz2p4.streamlit.app/).
<br>

#### Abilities:
* Query your data in plain language.
* Facilitates and performs many Data Analysis related tasks.
* Create plots/graphs/charts.
* Accepts multiple files.
* Conversations are stored including (Question, Steps to Produce, and Answer)

<br>

| Conversation History      | Handle multiple files | Visualize data through various plots     | Inspect Model's Steps To Answer |
|    :----:   |    :----:   |    :----:   |    :----:   |
| ![Conversation History](media/convo_history.gif)      | ![Upload Multiple Files](media/multiple_files_upload.gif)       | ![Plot Charts](media/view_plot.gif) | ![Read Steps to Produce Answer](media/read_steps.gif)  |


#### Requirements:
* Open AI API Key:  [Obtained Here](https://platform.openai.com/account/api-keys).

You can use the demonstration without any installation by placing your Open AI Key in the sidebar API field (Ref: app.py).

![Open AI Key Placement](media/openai_key.png)


      def setOpenAIKey(key):
         os.environ['OPENAI_API_KEY'] = key

* Installation of the following libraries (requirements.txt):

      streamlit==1.22.0
      streamlit-chat==0.0.2.2
      openai==0.27.6
      streamlit-image-select==0.6.0
      langchain==0.0.181
<br>

#### Access Previous Conversations:

When accessing the convo_history.json file, the conversations shall be stored in the following format:

```json
    "DATE_TIME_STAMP": [
            {
                "Question": "",
                "Answer": "",
                "Steps": ""
            }
        ]
```

All generated Charts/Graphs/Plots are stored in the project base directory (Agent Working Directory).
<br>

#### Usage:
When using or modifying this tool do always give appropriate credit.

<br>

#### References:
* [LangChain Dataframe Agent](https://python.langchain.com/en/latest/modules/agents/toolkits/examples/pandas.html)
* [Open AI Model](https://platform.openai.com/)
* [StreamLit Python](https://docs.streamlit.io/)
* [Pandas AI Library](https://python.langchain.com/en/latest/modules/agents/toolkits/examples/pandas.html)

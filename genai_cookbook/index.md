---
title: Databricks Generative AI Cookbook
---

# Databricks Mosaic AI <br> Generative AI Cookbook

The Generative AI Cookbook is a collection of notebooks demonstrating different use cases for Databricks Mosaic AI tools such as the Foundation Model API and the Model Playground.

## Featured Notebooks

::::{grid} 3
:class-container: text-center

:::{grid-item-card}
:link: nbs/vector_search_fm_api
:link-type: doc
:class-header: bg-light

Embeddings for Vector Search
^^^
Use the Foundation Model API to generate embeddings for Databricks Vector Search.
:::

:::{grid-item-card}
:link: nbs/fm_api_openai_sdk
:link-type: doc
:class-header: bg-light

Use the Foundation Model API with the OpenAI Python SDK
^^^
Convert your OpenAI Python code to use the Foundation Model API with minimal code changes.
:::

:::{grid-item-card}
:link: nbs/streaming_outputs
:link-type: doc
:class-header: bg-light

Generate Streaming Outputs
^^^
Generate streaming outputs with the Python SDK and the REST API.
:::
::::

## How to Run These Notebooks in your Databricks Workspace

### Import individual notebooks

If you want to run one of these notebooks in your Databricks workspace, click the download icon in the upper right corner of the page you would like to run. Then right-click on `.ipynb` and select "Copy link address." In your Databricks workspace, in the workspace view, select "import" (from the three-dots menu or from the right-click menu) and paste in the url you copied. This will import the notebook to your Databricks workspace.

![Image](./images/index/import_notebook.png)

### Clone the repository

You can also clone the whole repository into your workspace. Simply navigate to "Repos" in your Databricks workspace, click "Add Repo", and copy in the URL: [https://github.com/databricks-genai-cookbook/cookbook](https://github.com/databricks-genai-cookbook/cookbook). Then click Create Repo. This will clone the repository to your workspace, giving you access to all of the notebooks right in your Databricks workspace.

## Official Documentation
- [Foundation Model APIs](https://docs.databricks.com/en/machine-learning/foundation-models/index.html)
- [AI Playground](https://docs.databricks.com/en/large-language-models/ai-playground.html)
- [Vector Search](https://docs.databricks.com/en/generative-ai/vector-search.html)
- [AI Functions](https://docs.databricks.com/en/large-language-models/ai-functions.html)


```{tableofcontents}
```




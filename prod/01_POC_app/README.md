# RIGHT NOW - ONLY PDF WORKS!!!!!

# Building the POC application

Before getting started, follow this [guide]() to work with your business stakeholders to determine your application's requirements.

### Step 1: Deploy a POC to collect stakeholder feedback

To get started, deploy a *quality-ready POC* to stakeholders.  A quality-ready POC is a RAG application that:
- Stakeholders can provide 👍 / 👎 feedback and ✏️ correct answers using a chat-based Web UI 
- Attaches a detailed MLflow Trace to every piece of feedback
- Chain & data preparation code are parameterized and ready for fast, iterative dev loops to improve quality

1. Clone this repo into your Databricks workspace
2. Adjust the `00_global_config` to point to your Unity Catalog schema and data sources.
2. Select a folder within `01_POC_app` folder that corresponds to the data you are using

*Each POC app is configured with reccomended default settings*

| File type                        | Source            | POC application folder |
|----------------------------------|-------------------|------------------------|
| PDF (`.pdf`) files                        |   UC Volume                |        [Single-turn chat]()        \|  [Multi-turn chat]()        |
| PowerPoint (`.pptx`) files                 |       UC Volume            |         [Single-turn chat]()        \|  [Multi-turn chat]()        |
| Word (`.docx`) files                       |    UC Volume               |         [Single-turn chat]()        \|  [Multi-turn chat]()        |
| HTML (`.html`)files                     |    UC Volume               |               [Single-turn chat]()        \|  [Multi-turn chat]()        |
<!-- | HTML text                     |    Delta Table               |               [Single-turn chat]()        \|  [Multi-turn chat]()        | -->
<!-- | Markdown or regular text         |        Delta Table           |            [Single-turn chat]()        \|  [Multi-turn chat]()        | -->
<!-- | JSON files        |         UC Volume          |          [Single-turn chat]()        \|  [Multi-turn chat]()        | -->

> *In contrast to the "3 lines of magic code" POC, there is necessarily more complexity in the code base. However, we have organized this complexity to make quality iteration easy.*

3. Review the POC's parameters in the `00_config` Notebook
4. Run `02_validate_config` to ensure that all necessary resources are set up
4. Run `02_poc_data_pipeline` to create a Vector Index from your data using Databricks Vector Search
5. Run `03_deploy_poc_to_review_app` to deploy the app to a [Quality Lab Review App]()
6. Share the app's URL your stakeholders so they can chat with it and provide feedback

**IMAGE OF REVIEW APP**

## Step 2: Evaluate the POC’s quality

Once your stakeholders have used your POC, we will use their feedback to measure the POC’s quality and establish a baseline.

1. Open the `04_evaluate_poc_quality` Notebook.
2. Follow the steps in the Notebook to create an initial Evaluation Set based on the logs from your Review App.
3. Inspect the Evaluation Set to understand the data that is included.  You need to validate that your Evaluation Set contains a representative and challenging set of questions..
4. Save your evaluation set to a Delta Table for later use
5. Evaluate the POC with Agent Evaluation's LLM Judge-based evaluation.  Open MLflow to view the results.
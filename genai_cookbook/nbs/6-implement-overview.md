## **Start here:** Clone code repo & create compute

This implement section is coupled with a repository of sample code designed to work on Databricks.  

**Requirements:**

- A Databricks workspace with [serverless](https://docs.databricks.com/en/admin/workspace-settings/serverless.html) and Unity Catalog enabled
- A [Mosaic AI Vector Search](https://docs.databricks.com/en/generative-ai/vector-search.html) endpoint, either:
    - An existing endpoint
    - Permissions to create a new endpoint - the setup Notebook will do this for you
- Unity Catalog Schema where the output Delta Tables with the parsed/chunked documents and Vector Search indexes are stored, either:
    - Write access to an existing [Unity Catalog](https://docs.databricks.com/en/data-governance/unity-catalog/index.html) and [Schema](https://docs.databricks.com/en/data-governance/unity-catalog/index.html#the-unity-catalog-object-model) 
    - Permissions to create a new Unity Catalog and Schema - the setup Notebook will do this for you
- A [**single-user**](https://docs.databricks.com/en/compute/configure.html#access-modes) cluster running [DBR 14.3+](https://docs.databricks.com/en/release-notes/runtime/index.html) with access to the internet
    - These tutorials have Python package conflicts with Machine Learning Runtime.  
    - Internet access is required to download the necessary Python and system packages 

To get started:

1. Clone this repository into your workspace using [Git Folders](https://docs.databricks.com/en/repos/repos-setup.html)


```{image} ../images/5-hands-on/clone_repo.gif
:align: center
```
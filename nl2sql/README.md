# Build Your Own NL2SQL engine

How?

* We'll try to keep this as simple as possible and not get lost in the weeds
* You will be able to ask a question and the NL2SQL engine will be able to figure out the schema of the db and generate the SQL
* The SQL will be executed by _the agent_.  For that, we'll use LangChain

We'll try to do all of this in Jupyter notebooks.  Hopefully you can follow along:  

We'll load up and use a subset of the titanic dataset from Kaggle.  

You'll need to install:
* vscode
* jupyter notebook extension
* open the [nl2sql jupyter notebook](./nl2sql.ipynb) and follow along
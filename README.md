# PSSUG GenAI sessions - April 2025


dave@davewentzel.com
davew@microsoft.com
linkedin.com/in/dwentzel


## Schedule 

_This schedule is subject to change depending on how much progress we make each week_

* 4/9:  6pm-8  in Malvern.  
  * foundational stuff.  
  * What is an LLM?  How do these things work?  Are they safe?  
  * we'll look at the RAG pattern and agentic AI and what that means
  * we'll briefly touch on "copilot"
* 4/16 630-830  virtual only
  * might be worth talking through how to find good use cases, how to structure a team and project, pick tools, how the real world does Responsible AI etc
  * we'll also take a look at Natural Language to SQL (nl2sql) and the pros and cons of doing this
* 4/23 630-830  virtual only
  * [Here is the general pattern for basic NL2SQL tasks](structured_data_retreival_nltosql.ipynb)
  * Fabric and AI
    * [nl2sql in Fabric](fabric.md)
    * [fabric copilot in spark notebooks](./Copilot.ipynb)
  * advanced topics around "querying databases"
    * we can definitely do nl2sql...that's easy, but there are VERY difficult problems we still need to solve
      * complex schemas  (lots of tables with goofy naming conventions, non-intuitive join keys, complex filter conditions like adding `WHERE status = 1` to all queries)
        * we can handle this with judicious views
      * natural language ambiguity:  example:  "how much" (dollar amounts) vs "how many" (counts) queries
        * we can provide few-shot prompts to describe which columns we should use when the query is asking _how much_ vs _how many_
        * lots of other examples like this
        * aka "understanding _intent_"
      * tribal knowledge:  understanding that certain _phrases_ mean different things in different companies
        * "active customer" could mean "customers who bought something in the last 3 months" at one company, but 6 months at another company
          * we can again solve this with few-shot prompting.  
    * is there a better way to do all of this?  can we use a search index to help us?  YES.  [Using a search index to aid nl2sql](./nlsql-search-index.md)
    * TAG and LOTUS
    * llms over tables of unstructured and structured data

  * What does the "near future" look like?  
    * Advanced use cases
    * GraphRAG (RAG against a Knowledge Graph)
  * bring your use cases and questions and let's discuss them
  * let's get ready for actually building something using an LLM.  Let's get an environment setup and ready.  
* 4/30 630-830 virtual only 
  * let's build something and test the waters.  this might be complicated if folks don't have access to azure subscriptions and whatnot.  I might have a good solution to this problem by then.  Otherwise, another possible topic would be Fabric and the AI skills that exist there (altho they are half-baked).
    * [AI Dev Gallery](https://apps.microsoft.com/detail/9n9pn1mm3bd5?hl=en-US&gl=US)
      * windows app, runs all models locally, good for experimentation and _art of the possible_.  
      * no need for azure access or microsoft account
      * [gh repo to learn more](https://github.com/microsoft/ai-dev-gallery/)
    * [Build Your Own NL2SQL copilot](./nl2sql/README.md)
      * you will need to know some python (not much()), have access to a sql server somewhere, and access to GPT4 (either via Azure, which you can do for free, or OpenAI directly)

[Registration](https://www.eventbrite.com/e/phila-sql-april-2025-user-group-meeting-dave-wentzel-series-part-1-of-4-tickets-1291203216579?aff=oddtdtcreator)



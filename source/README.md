## Data Acquisition and Preprocessing

To perform our analysis, we obtained two PDF documents from the official website of the Power Grid Company of Bangladesh (PGCB), containing detailed data on substations and transmission lines. Each document presents data in a semi-structured, tabular format across multiple pages, with some missing values and inconsistent naming conventions.

The original source of the PDF files is as follows:

- [https://pgcb.gov.bd/site/download/0443b0d5-d49c-46bf-bcbc-980ade10478f/](https://pgcb.gov.bd/site/download/0443b0d5-d49c-46bf-bcbc-980ade10478f/)

- [https://pgcb.gov.bd/site/download/174e55d2-2780-4d33-9d71-057c38647695/](https://pgcb.gov.bd/site/download/174e55d2-2780-4d33-9d71-057c38647695/)

These documents were accessed on Nov 5, 2024

To convert these PDFs into an analyzable format compatible with network science tools, we employed Claude 3.5 Sonnet, a large language model released by Anthropic. This model is capable of interpreting both image and document formats, including PDFs. We attached the PDF files alongside prompts that specified format requirements and included several few-shot examples, which guided the model in outputting data in the required structure.

Upon completion of this process, we obtained two CSV files representing the network data, structured to support further processing and analysis.

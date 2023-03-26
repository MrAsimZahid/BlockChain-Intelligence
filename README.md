# BlockChain-Intelligence
Building few ideas on the intersection of Data Science x AI x Blockchain in public.


This repository is for the purpose of building on ideas, and practice knowledge related to the intersection of Data Science x AI x Blockchain.

- BlockChain Intel 
- BlockChain data
- Fraud detection
- On-Chain Analysis
- Liquidity prediction
- Ransom Tracking


## System Design

BlockChain intelligence Data Platform

<p align="center">
  <img src="media/BlockChian_Intelligence_Data_platform.png" alt="Preview">
</p>


# Architecture

Base architecture design is [Lambda Architecture](https://mrasimzahid.medium.com/lambda-architecture-basics-data-engineering-ea0c05fe1c0f)

Later on, if required, we will migrate to Kappa architecture.

# Sections

## Data Ingesion

### `Sources`
- JSON-RPC API
- Web3.js/web3.py API
- Etherscan API
- Blocknative API
- Infura API
- Blockcahin Nodes

### `Data Modeling`

Will write on this later.

Feel free to contribute.

### `Data Contracts`

Use [Pydantic](https://docs.pydantic.dev/) to perform data validation and ensure data quality of the data model.

## Orchestration Tools

Will go for airflow for now.

- Airflow
- Perfect

The choice between Airflow and a perfect orchestration tool ultimately depends on the specific needs of your organization. Airflow can be a great choice for smaller organizations or teams that want a flexible and extensible platform for managing their workflows, while perfect orchestration tools are better suited for larger enterprises with complex, distributed workflows that require more advanced features and support.

## Data Storage

### `Kafka`

To handle event driven streaming data

### `Elasticsearch`

Why ELK?

Its a search database and efficient to do lookup the data.

How to optimize the elasticsearch (Index Management)?

- Create seperate indexes for each blockchain
- Apply a weekly or daily index rollup policy . This will optimize the search


[Read More on enginnering blogs](https://vinted.engineering/)

### `Postgres`

Use ULIDs rather than UUIDs. This small change will reduce the read and write costs to the DB by 50%

[Read Shopify Engineering Blog](https://shopify.engineering/building-resilient-payment-systems)


### `BigQuery`

Considering the internals of BigQuery. It's good for analytical purposes.

- BigQuery uses columnar database `colossus` which stores the data in B-Tree dataStructure
- It automatically manages re-clustering and partitioning


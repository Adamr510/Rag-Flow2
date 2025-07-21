```mermaid
graph TD
    A([Data Source] SharePoint Online) -->|1. Documents are added/updated| B{Indexer in Azure AI Search};
    B -->|2. Indexer runs on a schedule| C(Skillset Pipeline);
    subgraph C [Skillset Pipeline]
        direction LR
        C1(Text Splitting) --> C2(Vectorization);
    end
    C2 -->|Uses Agent 1| D([Agent 1] Embedding Model);
    D -->|3. Creates embeddings| B;
    B -->|4. Stores text chunks and vectors| E[[Vector Store] Azure AI Search Index];

    style A fill:#2b579a,color:#fff
    style E fill:#0078d4,color:#fff
    style D fill:#4CAF50,color:#fff
```

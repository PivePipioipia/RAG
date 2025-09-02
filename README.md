#  RAG Pipeline

This repository demonstrates a simple Retrieval-Augmented Generation (RAG) pipeline.

##  Pipeline Overview

```mermaid
graph TD
    A[PDF/Txt/Docs] --> B[Extract Data/Context]
    B --> C1[Text Chunk 1]
    B --> C2[Text Chunk 2]
    B --> C3[Text Chunk 3]
    B --> Cn[Text Chunk N]

    C1 --> E1[Embedding 1]
    C2 --> E2[Embedding 2]
    C3 --> E3[Embedding 3]
    Cn --> En[Embedding N]

    E1 --> F[Build Semantic Index]
    E2 --> F
    E3 --> F
    En --> F

    F --> K[Knowledge Base]

    Q[User Question] --> QE[Query Embedding] --> S[Semantic Search] --> K

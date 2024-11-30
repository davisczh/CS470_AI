# About:
 TlDR: This project attempts to implement a geo-spatial aware llm, by equiping llm with a vector database through function calling. Attempts to vectorise addresses with sentence-transformers, assuming that similar address would give similar vector.

# Project Setup Instructions

MAKE SURE THE YELPDATASET IS IN THIS DIRECTORY UNDER: archive/yelp_academic_dataset_business.json

## Step 1: Install Ollama

To install Ollama, refer to the GitHub repository for the latest instructions:

[Ollama GitHub Repository](https://github.com/ollama/ollama)

## Step 2: Pull Ollama Content

After Ollama is installed, you can pull the specific content repository using the following command:

```bash
ollama pull calebfahlgren/natural-functions
```

## Step 3: Set Up Qdrant with Docker

Install and run Qdrant using Docker with the commands below. This will set up the necessary ports and volume for data persistence:

```bash
docker pull qdrant/qdrant
docker run -p 6333:6333 -p 6334:6334 -v $(pwd)/qdrant_storage:/qdrant/storage:z qdrant/qdrant
```

## Step 4: Install Python Dependencies

Install all required Python packages from your requirements.txt file and update the sentence-transformers package using these commands:

```bash
pip install -r requirements.txt
pip install -U sentence-transformers
```


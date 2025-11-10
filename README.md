# Nexora Vibe Matcher

A semantic product recommendation system that matches user "vibe" queries to fashion products using AI embeddings and cosine similarity.

## Overview

The Nexora Vibe Matcher is a prototype recommendation engine that allows users to describe their desired fashion mood or "vibe" (e.g., "cozy festival") and receive personalized product recommendations. The system uses OpenAI embeddings or TF-IDF fallback to convert product descriptions and user queries into semantic vectors, then finds the most relevant matches using cosine similarity.

## Features

- **Semantic Search**: Natural language queries to find matching products
- **Dual Embedding System**: 
  - Primary: OpenAI `text-embedding-ada-002` embeddings
  - Fallback: Local TF-IDF embeddings (works without API key)
- **Top-K Recommendations**: Returns the most relevant products for any vibe query
- **Performance Evaluation**: Includes test queries and evaluation metrics
- **Visualization**: Performance analysis with charts and timings

## Project Structure

```
Nexora/
├── Nexora_Vibe_Matcher.ipynb    # Main notebook with implementation
├── products_with_embeddings.csv  # Product data with embeddings
├── vibe_results.json             # Sample recommendation results
└── README.md                     # This file
```

## Installation

### Requirements
- Python 3.8+
- Jupyter Notebook or Google Colab

### Dependencies
```bash
pip install openai pandas scikit-learn matplotlib numpy
```

## Usage

### Setting Up API Key (Optional)

For OpenAI embeddings, set your API key as an environment variable:

**Windows (cmd):**
```cmd
set OPENAI_API_KEY=your-key-here
```

**Mac/Linux:**
```bash
export OPENAI_API_KEY=your-key-here
```

**Google Colab:**
Go to Runtime → Environment Variables and add `OPENAI_API_KEY`

> **Note**: The system works without an API key using TF-IDF fallback embeddings.

### Running the Notebook

1. Open `Nexora_Vibe_Matcher.ipynb` in Jupyter or Google Colab
2. Run all cells sequentially
3. Try different vibe queries like:
   - "cozy festival vibes"
   - "urban edgy streetwear"
   - "elegant evening wear"

### Sample Products

The prototype includes 10 sample fashion items:
- Boho Dress
- Urban Bomber Jacket
- Cozy Knit Sweater
- Minimal Blazer
- Athleisure Hoodie
- Boho Sandals
- Glam Party Top
- Vintage Denim Jacket
- Elegant Midi Skirt
- Graphic Oversized Tee

## How It Works

1. **Product Embedding**: Convert product descriptions to dense vectors
2. **Query Embedding**: Convert user vibe query to the same vector space
3. **Similarity Matching**: Calculate cosine similarity between query and products
4. **Ranking**: Return top-3 (or top-K) most similar products

## Why AI for Nexora?

Because Nexora is redefining product discovery through **vibe-based AI recommendations**, and that aligns strongly with my interests in **NLP, embeddings, and personalization systems**. Here, AI isn’t just a backend feature — it becomes the **core user experience**, and I want to contribute to building that impact.       
This prototype shows how embeddings + lightweight vector search can reduce discovery friction, power shoppable influencer content, and evolve into a production pipeline with Pinecone or a managed vector DB for scale.

## Author

**Vineet Patel**
- Email: vineetpatel468@gmail.com
- GitHub: [@vineet416](https://github.com/vineet416)
- LinkedIn: [@vineet416](https://www.linkedin.com/in/vineet416/)

Created: November 10, 2025

## Future Enhancements

- Integration with production vector database (Pinecone, Weaviate)
- Expanded product catalog
- Multi-modal embeddings (text + images)
- User feedback and personalization
- Real-time API deployment

## Acknowledgments

This project was developed with reference to the following resources:

- **OpenAI Documentation**: [OpenAI Embeddings API](https://platform.openai.com/docs/guides/embeddings) - For implementing the `text-embedding-ada-002` model
- **ChatGPT**: Used for code assistance, debugging, and implementation guidance
- **Scikit-learn Documentation**: For TF-IDF vectorization and cosine similarity implementations

## License

This is a prototype project for assignment purposes.
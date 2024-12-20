# ModernBERT Knowledge Graph Generator

This project leverages **ModernBERT** and other NLP tools to create a knowledge graph from input text. The pipeline extracts meaningful entities and relationships from text, builds a graph, and visualizes it.

---

## Features
- **Entity Extraction**: Uses ModernBERT's `fill-mask` pipeline to extract entities.
- **Relationship Extraction**: Identifies relationships between entities using masked language modeling.
- **Knowledge Graph Visualization**: Builds and visualizes a directed graph with extracted entities and relationships.

---

## Requirements
To run this project, ensure you have the following installed:
- Python 3.8 or higher
- The dependencies listed in `requirements.txt`

### Dependencies
- [transformers](https://github.com/huggingface/transformers)
- [spacy](https://spacy.io/)
- [networkx](https://networkx.github.io/)
- [matplotlib](https://matplotlib.org/)
- [flash-attn](https://github.com/HazyResearch/flash-attention)

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Install Dependencies
Install the required dependencies using `uv` or `pip`:
```bash
# Using uv (recommended for virtual environments)
pip install uv
uv pip install -r requirements.txt

# Or directly using pip
pip install -r requirements.txt
```

---

## Usage

1. Replace the input text in the code with the text you want to process.
2. Run the preprocessing, entity extraction, relationship extraction, and visualization steps sequentially.
3. View the generated knowledge graph.

---

## Example Outputs

### Extracted Entities
- Examples: `['AI', 'Google', 'Bing', 'Tesla']`

### Extracted Relationships
- Examples: `[('AI', 'powers', 'Google'), ('AI', 'assists', 'doctors')]`

### Knowledge Graph Visualization
- A directed graph with:
  - **Nodes**: Entities extracted from the input text.
  - **Edges**: Relationships identified between entities.

---

## Troubleshooting

### Common Issues
1. **Slow Execution**:
   - Reduce the size of the input text for faster results.
   - Limit the number of relationships processed using predefined thresholds.

2. **Unexpected Predictions Format**:
   - Debug the predictions to inspect the model output.

3. **No Meaningful Relationships**:
   - Ensure the input text contains clear and structured relationships.
   - Adjust the confidence threshold in the relationship extraction function.

---

## Contributing
Contributions are welcome! Feel free to submit issues or pull requests to improve this project.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

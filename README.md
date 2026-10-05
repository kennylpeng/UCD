# Universal Concept Dictionaries

A universal concept dictionary (UCD) is a general-purpose interpretable embedding model that converts natural language inputs into high-dimensional sparse vectors, where each dimension corresponds to a labeled natural language concept.

UCDs enable efficient statistical computation while maintaining interpretability.

Our model is `gemini-ucd-80k`, a UCD that builds on top of gemini-embedding-2. The model is available at https://huggingface.co/klpeng/gemini-ucd-80k.

For example, the string "Djokovic overwhelms Nadal for Wimbledon Title" activates on the following concepts:

| Concept ID | Activation | Label |
|---|---:|---|
| 58492 | 0.185 | Short, standalone article titles |
| 9715 | 0.180 | Tennis-related text |
| 105125 | 0.139 | Novak Djokovic |
| 27796 | 0.122 | Wimbledon Championships |
| 14127 | 0.117 | Mentions of Wimbledon |
| 104228 | 0.072 | Rafael Nadal |
| 22956 | 0.068 | Sports finals and championship matchups |
| 13845 | 0.046 | People, places, and topics associated with the former Yugoslavia |
| 7908 | 0.038 | Winning and victory (including forms of “win” and “winner”) |
| 20603 | 0.035 | UK- and Britain-related content |
| 117500 | 0.032 | Sports results, standings, and rankings pages |
| 73147 | 0.029 | Grass-court tennis tournament names, especially the Queen’s Club Championships |
| 15101 | 0.027 | Sports blowouts and lopsided victories |
| 72276 | 0.025 | Male/men-related content |
| 94790 | 0.025 | Serbia and Serbian-related topics |
| 35618 | 0.025 | Endings and finality |

## Artifacts

- A sparse encoder (mapping gemini embeddings to sparse concept vectors)
- A concept dictionary (mapping dimensions to concept labels)
- Baseline prevalences for each concept (from the entire corpus), which can be used to identify concepts that are uniquely prevalent in a dataset.

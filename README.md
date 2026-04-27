# Project objectives

  We apply the GLiNER2 base model to identify the candidate and his political affiliation based on a transcript of his manifesto in the 1988 parliamentary election in France. We explore several different specifications of this task and compare the recall performance. In particular, we are interested in the structured extraction feature of GLiNER2, in comparison with standard NER or classification tasks. The performance of featured extraction is quite high and only slightly lower than standard NER, suggesting that structured extraction will be useful for future projects at INSEE, such as for mapping free-text passages into official categories.

# Replication

- setup the environment
  - `uv sync`
  - `uv run ipython kernel install --user --env VIRTUAL_ENV $(pwd)/.venv --name=project`
  - then select the `project` kernel in jupyter
- setup data : `archelect_search.csv` and `text_files` in the root directory
- run `Main.ipynb` to create `df_gliner_full.parquet`. This dataframe assembles the outputs from GLiNER2 for each transcript.
- run `Visualization.ipynb` for the Doc2Vec + t-SNE figure
- run `Analysis.ipynb` for the data analysis



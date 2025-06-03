# Harmfulness-of-Ambiguous-Vectors
Distributional vectors summarize word contexts to model meaning, but ambiguous words average distinct senses, potentially distorting results. The extent of this harm is unclear. Using lexicons that flag ambiguity, we can restrict to unambiguous words and measure morphological performance. How crucial is lexical ambiguity?

## Data

https://drive.google.com/file/d/1Dr38AGjigYBIFnbjHcwFI6JQHo4dgBmv/view?usp=drive_link

-including the words and embeddings used in the model as prep_data

prep_data = {
    'lemma_to_supersense': lemma_to_supersense, # dict of lemmas to supersenses
    'lemma_to_hypersense': lemma_to_hypersense, # dict of lemmas to hypersenses
    'supersense_set': supersense_set, # set: all supersenses
    'hypersense_set': hypersense_set, # set: all hypersenses
    'words': words, # list of str: words to embeddings
    'embeddings': embeddings_array, # numpy array of list of list of floats: emdeddings to words
    'words_bow': words_bow, # list of str: words to embeddings
    'embeddings_bow': embeddings_array_bow, # numpy array of list of list of floats: emdeddings to words
    'ambiguous_sslemmas': ambiguous_sslemmas, # list of str
    'ambiguous_hslemmas': ambiguous_hslemmas  # list of str
}


-embeddings taken from Bonami & Naranjo (2021) https://zenodo.org/records/5975226

-ambiguous&unambiguous words based on Supersense and Hypersense labels provided by Angleraud, Barque, and Candito (2025) https://www.ortolang.fr/market/lexicons/superwikt-fr

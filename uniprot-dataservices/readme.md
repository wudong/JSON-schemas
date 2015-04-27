# UniProt Dataservices - JSON Schemas #
## Features ##
A features JSON provides general information about a protein such as accession, identifier, and sequence, as well as an array of sequence features. A sequence feature always has a start and end position within the sequence; some uncertainty regarding those positions is also possible.

Features are grouped in types, and types are grouped in categories. A special category corresponds to Natural Variants. In our JSON schema we have an array for variants and another one for the rest of the features. Mutagenesis is currently part of "the rest of the features" but in the future it could be treated in a similar way as variants, and then moved to a third array "mutagenesis".

All features, variants or not, should have a begin position. An end position is optional, if not present then it is understood that the end is exactly the same as the beginning.

### Non variant features ###
Non variant features, refert to as features in the JSON schema, should be order by category, type, and start position. In this way we aim to save some processing time on the clients.

### Variants ###
A variant is a mutated set of amino acides. Usually it will be only one amino acid but it could be more than one, e.g., insertions and repetitions. The attribute "length" in the JSON schema indicates how many amino acids are mutating, if ommited it is understood that the variant deals with only one amino acid.

### Categories and types ###
The file [categoriesTypes.json](https://github.com/ebi-uniprot/JSON-schemas/blob/master/uniprot-dataservices/categoriesTypes.json) contains the categories and types for UniProt features. Category and type abbreviations **must** be the same as those used in the features JSON. The order for categories and types in the features JSON **must** be alphabetical.

### Visualization ###
Some types usually cover a region within the sequence, those are represented as rectangles. Some other types are known as sites; they usually cover one single amino acid, sometimes two amino acids. For the latter types, some shapes have been predefined. Below there is a summary of shapes and colours used for UniProt protein features.

### Uncertainty ###

### Notes ###
- The types for Natural Variants are not well defined yet. We are testing with users some possibilities.
- The order has not been defined, it could be alphabetical or a predefined one.



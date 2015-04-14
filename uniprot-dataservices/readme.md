# UniProt Dataservices - JSON Schemas #
## Features ##
A features JSON provides general information about a protein such as accession, identifier, and sequence, as well as an array of sequence features. A sequence feature always has a start and end position within the sequence; some uncertainty regarding those positions is also possible.

Features are grouped in types, and types are grouped in categories. A special category corresponds to Natural Variants. All features belonging to this category **must** include a *variantObject*.

Features should be order by category, type, and start position. In this way we aim to save some processing time on the clients.

### Categories and types ###
These are the categories and types for UniProt features. Category and type abbreviations **must** be the same as those used in the features JSON.

    [
    	{
			"categoryAbbrev": "MOL_PROC",
			"category": "MOLECULE PROC.",
			"types": [
				{
					"typeAbbrev": "INIT_MET",
					"type": "INIT. METHIONINE"
				}, {
					"typeAbbrev": "SIGNAL",
					"type": "SIGNAL"
				}, {
					"typeAbbrev": "PROPEP",
					"type": "PROPEPTIDE"
				}, {
					"typeAbbrev": "TRANSIT",
					"type": "TRANSIT"
				}, {
					"typeAbbrev": "CHAIN",
					"type": "MATURE REGION"
				}, {
					"typeAbbrev": "PEPTIDE",
					"type": "PEPTIDE"
				}
			]
		}, {
			"categoryAbbrev": "STR_FT",
			"category": "STRUCTURAL FT.",
			"types": [
				{
					"typeAbbrev": "TURN",
					"type": "TURN"
				}, {
					"typeAbbrev": "HELIX",
					"type": "HELIX"
				}, {
					"typeAbbrev": "STRAND",
					"type": "BETA STRAND"
				}, {
					"typeAbbrev": "CROSSLNK",
					"type": "CROSSLNK"
				}, {
					"typeAbbrev": "DISULFID",
					"type": "DISULFIDE BOND"
				}
			]
		}, {
			"categoryAbbrev": "DOM_SITE",
			"category": "DOMAINS & SITES",
			"types": [
				{
					"typeAbbrev": "REPEAT",
					"type": "REPEAT"
				}, {
					"typeAbbrev": "HELIX",
					"type": "HELIX"
				}, {
					"typeAbbrev": "CA_BIND",
					"type": "CALCIUM BINDING"
				}, {
					"typeAbbrev": "ZN_FING",
					"type": "ZINC FINGER"
				}, {
					"typeAbbrev": "DNA_BIND",
					"type": "DNA BINDING"
				}, {
					"typeAbbrev": "NP_BIND",
					"type": "NUCLEOTIDE BIND"
				}, {
					"typeAbbrev": "REGION",
					"type": "REGION OF INTEREST"
				}, {
					"typeAbbrev": "COILED",
					"type": "COILED COIL"
				}, {
					"typeAbbrev": "MOTIF",
					"type": "SHORT SEQ. MOTIF"
				}, {
					"typeAbbrev": "ACT_SITE",
					"type": "ACTIVE SITE"
				}, {
					"typeAbbrev": "METAL",
					"type": "METAL ION-BINDING"
				}, {
					"typeAbbrev": "BINDING",
					"type": "BINDING"
				}, {
					"typeAbbrev": "SITE",
					"type": "SITE"
				}
			]
		}, {
			"categoryAbbrev": "PTM",
			"category": "POST TRANSLATIONAL MODIFICATIONS",
			"types": [
				{
					"typeAbbrev": "MOD_RES",
					"type": "MODIFIED RESIDUE"
				}, {
					"typeAbbrev": "LIPID",
					"type": "LIPID"
				}, {
					"typeAbbrev": "CARBOHYD",
					"type": "GLYCOSILATION"
				}
			]
		}, {
			"categoryAbbrev": "MUTA",
			"category": "MUTAGENESIS",
			"types": [
				{
					"typeAbbrev": "MUTA",
					"type": "MUTAGENESIS"
				}
			]
		}, {
			"categoryAbbrev": "SEQ_INFO",
			"category": "SEQUENCE INFO.",
			"types": [
				{
					"typeAbbrev": "COMP_BIAS",
					"type": "COMPOSITIONAL BIAS"
				}, {
					"typeAbbrev": "CONFLICT",
					"type": "CONFLICT"
				}, {
					"typeAbbrev": "NON_CONS",
					"type": "NON CONSECUTIVE"
				}, {
					"typeAbbrev": "NON_TER",
					"type": "NON TERMINAL"
				}, {
					"typeAbbrev": "UNSURE",
					"type": "UNSURE SEQ."
				}
			]
		}, {
			"categoryAbbrev": "TOPO",
			"category": "TOPOLOGY",
			"types": [
				{
					"typeAbbrev": "TOPO_DOM",
					"type": "TOPOLOGICAL DOMAIN"
				}, {
					"typeAbbrev": "TRANSMEM",
					"type": "TRANSMEMBRANE"
				}, {
					"typeAbbrev": "INTRAMEM",
					"type": "INTRAMEMBRANE"
				}
			]
		}, {
			"categoryAbbrev": "NAT_VAR",
			"category": "VARIANTS",
			"types": [
				{
					"typeAbbrev": "MISSENSE",
					"type": "MISSENSE"
				}, {
					"typeAbbrev": "INSDEL",
					"type": "INSERT & DELETE"
				}, {
					"typeAbbrev": "STOP_GAINED",
					"type": "STOP GAINED"
				}, {
					"typeAbbrev": "STOP_LOST",
					"type": "STOP LOST"
				}, {
					"typeAbbrev": "INIT_CODON",
					"type": "INITIATOR CODON"
				}
			]
		}
    ]
    

### Visualization ###
Some types usually cover a region within the sequence, those are represented as rectangles. Some other types are known as sites; they usually cover one single amino acid, sometimes two amino acids. For the latter types, some shapes have been predefined. Below there is a summary of shapes and colours used for UniProt protein features.

### Uncertainty ###

### Notes ###
- The types for Natural Variants are not well defined yet. We are testing with users some possibilities.
- The order has not been defined, it could be alphabetical or a predefined one.



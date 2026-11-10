# Claude BioServices Skill

A Python skill for accessing a broad range of bioinformatics services through a unified interface. BioServices can support multi-database workflows across resources such as UniProt, KEGG, ChEMBL, PubChem, Reactome, QuickGO, and other biological services.

## What It Covers

- **Protein data:** Retrieve protein sequences, identifiers, and functional annotations.
- **Pathway analysis:** Search organisms and pathways, retrieve pathway records, and analyze interactions with KEGG and Reactome.
- **Compound research:** Search and cross-reference chemical and bioactive compound records.
- **Sequence analysis:** Run remote sequence similarity searches and alignments.
- **Identifier mapping:** Convert identifiers between supported biological databases.
- **Gene ontology:** Query GO terms and annotations.
- **Data integration:** Combine information from multiple bioinformatics resources in Python workflows.

## Installation

Clone this repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-bioservices-skill.git ~/.claude/skills/bioservices
```

Install BioServices:

```bash
python -m pip install bioservices
```

## Using the Skill

Example request:

```text
Use the bioservices skill to retrieve a UniProt protein sequence,
map its identifier to KEGG, and identify related pathways.
```

The skill provides examples for individual services and cross-database workflows. It also explains when a unified BioServices interface is appropriate and when a database-specific REST API skill may offer more direct control.

## Repository Resources

- [SKILL.md](SKILL.md) contains the overview, service workflows, and operating guidance.
- `references/services_reference.md` provides service-specific API details.
- `references/workflow_patterns.md` describes integrated pathway and data workflows.
- `references/identifier_mapping.md` covers cross-database identifier conversion.

## Good Practices

Handle service errors and missing records explicitly, keep credentials out of source control, respect service usage policies, and validate identifier mappings before combining datasets. Confirm current API behavior with the relevant service documentation when implementing production workflows.

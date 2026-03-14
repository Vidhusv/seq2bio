# Seq2Bio: Protein Sequence to Biological Context

Seq2Bio is a comprehensive Google Colab notebook that transforms a protein sequence into a rich biological report. It integrates multiple public databases (NCBI BLAST, NCBI Taxonomy, iNaturalist, GBIF, PubMed) and tools (Clustal Omega, AlphaFold DB, ColabFold) to provide:

- BLAST homology search (≥70% identity)
- Taxonomic lineage
- Organism images and common names
- Interactive geographic map with hover tooltips (species, common name, image, location)
- Relevant PubMed publications (toxin/venom focused, but customisable)
- Multiple sequence alignment and phylogenetic tree (Newick format)
- Protein structure retrieval from AlphaFold DB or prediction via ColabFold, with confidence plots (pLDDT, PAE) and Ramachandran plots
- Downloadable ZIP archive of all results
- Email notification upon completion

## Quick Start (Google Colab)

1. Open the notebook in Google Colab: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/16XlTDvXRkk1n6FZpICSYdnraF32TejR1?usp=sharing)
2. Run the first two cells to install dependencies.
3. Enter your email and protein sequence in the configuration widget.
4. Run all subsequent cells sequentially – each step will display its results.
5. At the end, click the **Download All Results** button to save a ZIP archive.

## Local Installation (Optional)

If you wish to run the notebook outside Colab, install the required Python packages:

```bash
pip install biopython==1.85 requests folium pandas matplotlib seaborn py3Dmol


## Output Files

When you click Download All Results, a ZIP file named Seq2Bio_results.zip is created containing:

blast_results.csv – BLAST hits (species, accession, identity)

taxonomy.csv – Full taxonomic lineage for each species

images.csv – Image URLs and common names (from GBIF)

occurrences.csv – Geographic coordinates and location names (from GBIF)

publications.csv – PubMed articles related to each species

phylogenetic_tree.nwk – Newick tree file (for iTOL or other viewers)

structures/ – Folder with downloaded AlphaFold structures or ColabFold predictions (CIF/PDB, PAE JSON, pLDDT CSV)

cf_predictions/ – Additional ColabFold predictions (if any)


## Citation

If you use Seq2Bio in your research, please cite it as:

Vidhu Smitha Vijay. (2026). Seq2Bio: A Colab‑based tool for protein‑centric biological context retrieval (Version 1.0.0). Zenodo. [https://doi.org/10.5281/zenodo.19014688](https://doi.org/10.5281/zenodo.19014688)


## Contact

For questions, suggestions, or bug reports, please contact [team.wgs.prad2026@gmail.com].

## License
This project is licensed under the MIT License – see the LICENSE file for details.
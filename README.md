# qDA-seq Data Analysis Pipeline

This pipeline is designed to analyze qDA-seq sequencing data. Below are the steps involved:

1. **Quality Control (QC) for qDA-seq Data:**
   - FASTQ files are checked for quality using FastQC, and a summary report is generated.

2. **Read Alignment for qDA-seq Data:**
   - Reads are aligned to the reference genome using BWA, and sorted and indexed BAM files are generated.

3. **Filtering of Aligned Reads:**
   - PCR duplicates and low-quality reads are removed from the aligned reads.

4. **Peak Calling for qDA-seq Data:**
   - Differentially accessible regions are identified using qDA-seq specific algorithms like qDAPeakFinder.

5. **Annotation of Peaks:**
   - Annotate the identified peaks with genomic features using tools like BEDTools and annotatePeaks.pl.

6. **Visualization and Interpretation:**
   - Visualize and interpret the identified differentially accessible regions to gain insights into chromatin accessibility changes.

## Usage
- Clone this repository.
- Place your qDA-seq FASTQ files, reference genome, and condition information file (e.g., conditions.txt) in the same directory as the pipeline script.
- Modify the script as necessary to specify paths and parameters.
- Run the pipeline using `./pipeline.sh`.

## Requirements
- BWA
- Samtools
- qDA-seq specific algorithms (e.g., qDAPeakFinder)
- FastQC
- BEDTools
- deeptools (for visualization)

## Notes
- Adjust parameters and additional analysis steps based on specific experimental needs.
- Ensure reference genome files are available and properly indexed.

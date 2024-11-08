# RNA-Seq Processing Pipeline

This pipeline performs essential RNA-Seq preprocessing tasks, including compressing FASTQ files, quality control, trimming, genome indexing, alignment,  BAM file indexing and nd read counting.

## Prerequisites

Make sure the following tools are installed:
- **gzip**: For file compression
- **FastQC**: Quality control analysis
- **Trimmomatic**: Read trimming
- **STAR**: Genome indexing and alignment
- **samtools**: BAM file processing
- **featureCounts**: Counting the number of reads assigned to genes

## Workflow

1. **Compress FASTQ Files**: Compresses raw FASTQ files.
2. **Quality Control (FastQC)**: Generates quality control reports.
3. **Trimming (Trimmomatic)**: Removes adapters and low-quality bases from reads.
4. **Genome Indexing (STAR)**: Prepares the genome index for alignment.
5. **Alignment (STAR)**: Aligns reads to the genome, generating sorted BAM files.
6. **Index BAM Files (samtools)**: Creates index files for BAM files.
7. **Count Reads (featureCounts)**: Counts the number of reads assigned to genes

## Usage

1. Place your raw FASTQ files and a text file (`fastqfiles.txt`) containing the base names (without file extensions) in the same directory.
2. Update the paths to Trimmomatic and the genome files in the script if needed.

Run the script:
```bash
bash rna_seq_pipeline.sh

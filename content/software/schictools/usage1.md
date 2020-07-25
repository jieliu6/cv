---
title: Supported Format
linktitle: Format
toc: true
type: docs
date: "2019-05-05T00:00:00+01:00"
draft: false
menu:
  schictools:
    parent: Usage
    weight: 1

# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 4
---

  - Pre-processed Matrices:
  If the data is already processed into matrices for intra-chromosomal contacts,
  the chromosome from the same cell must be stored in the same folder with
  chromosome names as file names (e.g., scHiC/cell_1/chr1.txt).
  You only need to provide the folder name for a cell (e.g., scHiC/cell_1).
    - npy: numpy.array / numpy.matrix
    - npz: scipy.sparse.coo_matrix
    - matrix: matrix stored as pure text
    - matrix_txt: matrix stored as .txt file
    - HiCRep: the format required by HiCRep package

  - Edge List <br />
   For all formats below:<br />
   &nbsp; str - strand (forward / reverse)<br />
   &nbsp; chr - chromosome<br />
   &nbsp; pos - position<br />
   &nbsp; score - contact reads<br />
   &nbsp; frag - fragments (will be ignored)<br />
   &nbsp; mapq - map quality<br />

     - Shortest
     ```
    <chr1> <pos1> <chr2> <pos2>
     ```
    - Shortest_Score
     ```
    <chr1> <pos1> <chr2> <pos2> <score>
     ```
    - Short
     ```
    <str1> <chr1> <pos1> <frag1> <str2> <chr2> <pos2> <frag2>
     ```
    - Short_Score
     ```
    <str1> <chr1> <pos1> <frag1> <str2> <chr2> <pos2> <frag2> <score>
     ```
    - Medium
     ```
    <readname> <str1> <chr1> <pos1> <frag1> <str2> <chr2> <pos2> <frag2> <mapq1> <mapq2>
     ```
    - Long
     ```
    <str1> <chr1> <pos1> <frag1> <str2> <chr2> <pos2> <frag2> <mapq1> <cigar1> <sequence1> <mapq2> <cigar2> <sequence2> <readname1> <readname2>
     ```
    - 4DN
     ```
    ## pairs format v1.0
    #columns: readID chr1 position1 chr2 position2 strand1 strand2
     ```
   - .hic format: we adapted "straw" from JuiceTools.

   - .mcool format: we adapted "dump" from cool.

   - Other formats: simply give the indices (start from 1) in the order of<br />
 "chromosome1 - position1 - chromosome2 - position2 - score" or<br />
 "chromosome1 - position1 - chromosome2 - position2" or<br />
 "chromosome1 - position1 - chromosome2 - position2 - mapq1 - mapq2".<br />
   For example, you can provide "2356" or [2, 3, 5, 6] if the file takes this format:
   ```
   <name> <chromosome1> <position1> <frag1> <chromosome2> <position2> <frag2> <strand1> <strand2>
   contact_1 chr1 3000000 1 chr1 3001000 1 + -
   ```
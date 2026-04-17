NECTIN-4 FISH Calculator Help
============================

Purpose
-------
This calculator is adapted from the HER2 FISH calculator and 
mapped for NECTIN-4 (PVRL4) with CEP1 as the reference probe. 
It helps the user enter per-nucleus counts,calculate averages 
and ratios, review chromosome 1 gain, assess heterogeneity, 
screen for bimodality, and assign a NECTIN-4 group result 
using the supplied study-based thresholds.

General use
-----------
1. Enter Sample Name and Sample ID if desired.
2. For each tumor nucleus, enter the CEP1 centromere count and the 
   NECTIN-4 signal count.
3. Click Add after each pair. Press Enter in the centromere field to move to the 
   NECTIN-4 field, and press Enter in the NECTIN-4 field to add the pair.
4. Continue until the intended nuclei count has been entered.
5. Review the Results panel, histogram, and the definition boxes at the bottom.
6. Use Copy Report to copy a text summary to the clipboard.
7. Use Delete to remove selected rows or Clear to remove all rows.

Important scoring prerequisites
-------------------------------
- Score invasive neoplastic cells only.
- Exclude in situ elements, benign cells, necrotic areas, and overlapping nuclei.
- Score only nuclei that show at least one NECTIN-4 signal and at least one CEP1 signal.
- A specimen is considered evaluable only if the specimen contains at 
  least 100 viable invasive tumor cells.
- The calculator performs the arithmetic on the cells entered; specimen adequacy still 
  requires pathologist review.

Fields and controls
-------------------
Sample Name:
Optional text field for the case name.

Sample ID:
Optional text field for the accession or identifier.

Centromere:
The CEP1 count for a single nucleus.

NECTIN-4 Signal:
The NECTIN-4 count for the same nucleus.

Add:
Adds the entered nucleus pair to the table.

Delete:
Deletes the selected row or rows from the table.

Clear:
Deletes all entered rows.

Entered Nuclei Pairs table:
Shows all nuclei entered. Clicking a row selects it for deletion.

Copy Report:
Copies a plain-text summary of the case and results.

Exit Program:
Attempts to close the browser tab. Some browsers block this.

Results fields
--------------
Cells:
The number of nuclei entered into the calculator.

Avg NECTIN-4:
Average NECTIN-4 copy number per entered nucleus.

Avg Centromere:
Average CEP1 copy number per entered nucleus.

Ratio:
NECTIN-4 divided by CEP1, using the averages derived from the entered nuclei.

SD (NECTIN-4):
Standard deviation of the NECTIN-4 counts. This reflects the spread 
of NECTIN-4 values.

CV:
Coefficient of variation for NECTIN-4, calculated as SD divided by the 
average NECTIN-4 count.

Group:
The NECTIN-4 group assignment based on the supplied mapping.

Interpretation:
A short action or status statement attached to the group.

Heterogeneity:
A CV-based category describing how variable the NECTIN-4 counts are across nuclei.

Bimodality:
A simple screening result indicating whether the NECTIN-4 signal distribution appears 
to contain two separate peaks.

Chromosome Gain:
A CEP1-based category describing the degree of chromosome 1 gain.

Gain Note:
A brief interpretive comment explaining what the chromosome gain category means.

Interpretation categories
-------------------------
Group 1:
NECTIN-4/CEP1 ratio >= 2.0 and average NECTIN-4 copy number >= 6.0.
Interpretation: Positive.
This represents amplification by both ratio and gene copy number.

Group 2:
NECTIN-4/CEP1 ratio >= 2.0 and average NECTIN-4 copy number < 6.0.
Interpretation: Positive.
This reflects an amplified ratio even though the average gene copy number remains below 6.0.

Group 3:
NECTIN-4/CEP1 ratio < 2.0 and average NECTIN-4 copy number >= 6.0.
Interpretation: Positive.
This reflects high-level copy number increase despite a ratio below 2.0.

Group 4:
Borderline range. This is assigned if either of the following is present:
- Ratio 1.8 to 2.2, or
- Average NECTIN-4 copy number 5.4 to 6.6.
Interpretation: Count 20-50 additional cells.
This group is intended to flag borderline cases for additional enumeration.

Group 5:
Ratio < 2.0 and average NECTIN-4 copy number < 6.0, without Group 4 
borderline features. 
Interpretation: Negative.
This usually corresponds to a disomic pattern or absence of 
focal amplification.

How the calculator assigns groups
---------------------------------
The calculator checks for Group 4 borderline conditions first. If the ratio is 
between 1.8 and 2.2 inclusive, or if the average NECTIN-4 copy number is 
between 5.4 and 6.6 inclusive, it reports Group 4 and recommends 
counting 20-50 additional cells.

If the case is not borderline, it then assigns:
- Group 1 if ratio >= 2.0 and average NECTIN-4 >= 6.0
- Group 2 if ratio >= 2.0 and average NECTIN-4 < 6.0
- Group 3 if ratio < 2.0 and average NECTIN-4 >= 6.0
- Group 5 otherwise

Heterogeneity categories
------------------------
The calculator uses coefficient of variation (CV) of NECTIN-4 
counts to describe heterogeneity:
- Below low heterogeneity range: CV < 0.25
- Low heterogeneity: CV 0.25 to 0.40
- Moderate heterogeneity: CV > 0.40 to 0.60
- High heterogeneity: CV > 0.60

These categories describe numeric spread only. They do not by themselves 
define amplification status.

Chromosome gain categories
--------------------------
These categories are based on average CEP1 count:
- No chromosome gain: Avg CEP1 < 2.25
- Low-level chromosome 1 gain: Avg CEP1 2.25 to < 3.0
- Moderate chromosome 1 gain: Avg CEP1 3.0 to < 4.0
- Marked chromosome 1 gain: Avg CEP1 >= 4.0

Chromosome gain versus amplification
------------------------------------
The calculator separates chromosome 1 gain from focal NECTIN-4 amplification. When both 
NECTIN-4 and CEP1 increase together, the ratio may stay near 1.0 even though the absolute 
NECTIN-4 count rises. That pattern supports chromosome gain rather than focal amplification.

Gain note behavior
------------------
The Gain Note field changes automatically to explain the likely meaning of the CEP1 category:
- No chromosome gain: CEP1 not increased enough to support chromosome 1 gain
- Low-level gain: modest CEP1 increase; not equivalent to focal NECTIN-4 amplification
- Moderate gain: interpret NECTIN-4 counts in the context of the ratio
- Marked gain: high CEP1 count may explain increased NECTIN-4 counts without 
  focal amplification

Bimodality
----------
The calculator includes a simple distribution-based screen for bimodality 
using the NECTIN-4 counts:

- It builds a histogram of NECTIN-4 signals per nucleus.
- It looks for at least two meaningful peaks.
- It looks for separation between the peaks and a valley between them.
- If those criteria are met, it reports Bimodal and shows the approximate peak values.

This is a screening feature only. It is not a formal clinical classification by itself. 
A bimodal pattern may suggest two cell populations, clonal divergence, 
mixed amplification states, or sampling heterogeneity, but the pathologist 
must interpret that pattern in morphologic and technical context.

Histogram
---------
The histogram plots the number of nuclei at each NECTIN-4 signal count. 
If bimodality is detected, red dashed vertical markers identify the detected peaks.

Practical notes
---------------
- The calculator follows the arithmetic behavior of the original HER2 tool but 
  substitutes the supplied NECTIN-4 thresholds and terminology.
- Group names are analog mappings for NECTIN-4 and are not formal ASCO/CAP 
  Nectin-4 guideline groups.
- Borderline cases should be reviewed carefully and extended by counting 
  additional cells as directed.

WARNING:  "Software should not be used in life and death situations, such as in medical equipment, nuclear facilities, spacecraft or military combat operations. However, this restriction will not apply in the event of the occurrence certified by the United States Centers for Disease Control or successor body. Widespread viral infection transmitted via bites or contact with bodily fluids that causes human corpses to reanimate and seek to consume living human flesh, blood Brain or nerve tissue, and is likely to result in the fall of organized civilization". 



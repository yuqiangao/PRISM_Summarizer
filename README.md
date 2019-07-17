# PRISM_Summarizer

PRISM_Summarizer is a simple utility capable of parsing multiple Skyline output files 
containing targeted proteomic data of PRISM fractionationed samples and summarize them 
into two tables, one is a list of peak area ratios and the other is a list of fraction locations. The
method first select the fraction which contains the largest peak area of 
internal standard peptide (heavy) and then report the total peak area ratio of the endogenous 
peptide (light) against the internal standard peptide (heavy).

## Getting started
### System requirement
Windows 64-bit
### Installing
Download the PRISM_Summarizer folder into local drive. 

PRISM_Summarizer is a python based executable program in windows. So in order to properly run the software, none of the files in the PRISM_Summarizer folder can be deleted.
### Skyline requirement
First, all the fractions of the same sample need to be saved in the same skyline file.


Second, because we are picking the most intensed internal standard peptide (heavy) across all the
fractions, great care needs to be taken in peak picking. Manual checking of peak picking of each peptide
 in each fraction is recommended.

 Lastly, the Skyline output file needs to include at least the following columns: "Protein Name", "Peptide Sequence", "Replicate Name",
"Total Area Ratio", "Isotope Label Type", "Total Area". An example skyline template is located under folder Skyline Report Template.



### Running
1. Open cmd
2. Change the working directory to the one containing all the required files
3. The files required: all Skyline output files and a text file (.txt) containing the list of file names
4. Run the PRISM_Summarizer:

      __~\PRISM_Summarizer\PRISM_Summarizer.exe samplelist.txt__
5. The program will report two csv file: one is a list of peak area ratios while the other
is a list of fracction locations.

### Example
Example files can be found in Example folder.

## Remarks
Current version only exports the total peak area ratios and the internal stardard type is heavy.

## Version
V 1.0

## Authors
Yuqian Gao
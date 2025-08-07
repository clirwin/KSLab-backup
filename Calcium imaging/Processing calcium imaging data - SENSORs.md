
**Andrew’s analysis pipeline**
Last updated: July 28 2025 (C. Irwin)

Save .lif file to desktop ‘calcium’ folder containing the following:
-              extract_tiffs_from_lif.py
-              preprocess_tiffs.py
-              ops-CI.npy
-              analysis_SNR.ipynb
-              empty folder named ‘preprocessed’


**Extracting tiffs from lif file:**

1.         Save .lif file to desktop ‘calcium’ folder containing script to extract tiffs from lif file (‘extract_tiffs_from_lif.py’) and empty output folder (‘preprocessed’)

2.         In Terminal, run:

                                                i.                  conda activate calcium2+

                                              ii.                  python /Users/courtneyirwin/Desktop/calcium/extract_tiffs_from_lif.py --lif_file **lif_file_path** -o /Users/courtneyirwin/Desktop/calcium/preprocessed

**Pre-processing images:**

1.         In Terminal, run:

                                                i.                  python /Users/courtneyirwin/Desktop/calcium/preprocess_tiffs.py /Users/courtneyirwin/Desktop/calcium/preprocessed

**Create organoid mask in FIJI:**

1.         Open processed .tiff file in FIJI

2.         Using polygon selection tool, draw outline around cells within organoid

3.         Create mask by clicking Edit > Selection > Create Mask

4.         Save mask as .tiff file to same folder by adding “_mask.tiff” to end of file name

5.         Repeat for all files in dataset

**Cell registration using suite2p:**

1.         In Terminal, run:

                                                i.                  conda activate suite2p

                                              ii.                  suite2p

2.         In suite2p GUI:

                                                i.                  File > Run suite2p

                                              ii.                  Click ‘Add directory to data_path’ and open first file in /Users/courtneyirwin/Desktop/calcium/preprocessed/processed

                                           iii.                  Click ‘Load ops file’ and open /Users/courtneyirwin/Desktop/calcium/ops-CI.npy

                                           iv.                  Click ‘RUN SUITE2P’

                                              v.                  Manually confirm automatic registration accuracy

                                           vi.                  Repeat for all recordings in folder

**Add experiment metadata:**

1.         Create csv file with experiment and sample details:

                                                i.                  Sample (i.e., file name)

                                              ii.                  Day

                                           iii.                  Batch

                                           iv.                  Genotype (e.g., WT, FMR1 KO)

                                              v.                  Plate (e.g., 1xmat, 2xmat)

                                           vi.                  Treatment details (if applicable)

**Extract SNR analysis and create figures:**

1.         In Visual Studio Code, open ‘analysis_SNR.ipynb’ file and run code

                                                i.                  Change output folders to applicable paths

Troubleshooting:

-              remove spaces in file names

-              consider whether script needs TIFF vs TIF

-              to install new packages, in general start by trying:

o   conda activate calcium2+

o   conda install **package_name**
**Pre-processing images:**

1.         In Terminal, run:

                                                i.                  python /Users/courtneyirwin/Desktop/calcium/preprocess_tiffs.py /Users/courtneyirwin/Desktop/calcium/preprocessed

**Create organoid mask in FIJI:**

1.         Open processed .tiff file in FIJI

2.         Using polygon selection tool, draw outline around cells within organoid

3.         Create mask by clicking Edit > Selection > Create Mask

4.         Save mask as .tiff file to same folder by adding “_mask.tiff” to end of file name

5.         Repeat for all files in dataset

**Cell registration using suite2p:**

1.         In Terminal, run:

                                                i.                  conda activate suite2p

                                              ii.                  suite2p

2.         In suite2p GUI:

                                                i.                  File > Run suite2p

                                              ii.                  Click ‘Add directory to data_path’ and open first file in /Users/courtneyirwin/Desktop/calcium/preprocessed/processed

                                           iii.                  Click ‘Load ops file’ and open /Users/courtneyirwin/Desktop/calcium/ops-CI.npy

                                           iv.                  Click ‘RUN SUITE2P’

                                              v.                  Manually confirm automatic registration accuracy

                                           vi.                  Repeat for all recordings in folder

**Add experiment metadata:**

1.         Create csv file with experiment and sample details:

                                                i.                  Sample (i.e., file name)

                                              ii.                  Day

                                           iii.                  Batch

                                           iv.                  Genotype (e.g., WT, FMR1 KO)

                                              v.                  Plate (e.g., 1xmat, 2xmat)

                                           vi.                  Treatment details (if applicable)

**Extract SNR analysis and create figures:**

1.         In Visual Studio Code, open ‘analysis_SNR.ipynb’ file and run code

                                                i.                  Change output folders to applicable paths

**Troubleshooting:**

-              remove spaces in file names

-              consider whether script needs TIFF vs TIF

-              to install new packages, in general start by trying:

o   conda activate calcium2+

o   conda install **package_name**
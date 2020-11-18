# I-Frag
Software that can analyze terminal and internal fragments from top-down mass spectrometry data.
Download Instructions:
1.	Download the zip file from github. (This can be found under "Code" on the top right)
2.	Go to your downloads file and extract the files
3.	Place the unzipped file where it will be easy to find.
4.	Download Anaconda.
5.	Open file and begin installation. 
6.	We recommend installing for all users.
7.	Install in the "ProgramData" folder.
8.	If this is is your first time installing python and anaconda click both boxes in the "advanced installation options" dialog box.
9.	Install the software. 
10.	Once installed click next.
13.	Once going through all the other options, click finish. 
14.	Once anaconda is downloaded search for “anaconda prompt” on your computer.
15.	Type “start spyder” to start spyder software
16.	On the top right side of the software, open the folder that contains all the .csv and .py files from the zip file.
17. On the bottom of the top right pannel click "Files." (This should have all the files in the folder.)
18.	Open the setup.py file and run the script. (This will download all the packages need to run the script.)
19.	The program should be ready to run. Open the Test_GUI.py file and run it. 


Program instructions:
1. Run Test_GUI.py. 
2. Insert user parameters into the GUI that appears.
a.	PPM error indicates the maximum PPM error allowed to match a fragment. (We recommended a PPM error of less than 2 to reduce false positives)
b.	Sequence is the protein sequence that you want to compare the observed data against. (Make sure there are no spaces or commas between the letters or at the ends of the sequence and that all characters are standard amino acid codes.)
c.	Insert a number for the smallest internal fragment size. (We recommend 5 AA for the smallest internal fragment length.)
d.	Click "Observed Fragments" and upload a .csv file with the deconvoluted masses ([M+H]+ format) in one column and the intensities in the second column. (If the intensity is not known insert a zero for all masses in the second column)
e.	To insert fixed modifications upload a .csv file by clicking the "Fixed Modifications" tab. In the first column place the name of the modification, in the second collumn put the molecular weight, and the third column insert the number of the amino acid that contains the modification.
f.	To insert variable modification upload a .csv file by clicking the "Variable Modifications" tab. In the first column place the name of the modification, in the second row put the molecular weight, and in the third column place the amino acids the modification is placed on. If the modification does not ascribe to any specific amino acid write "None"
g.	Choose a terminal modification if you expect one on your sequence. If a terminal modification exists on the protein but does not show up in the list treat it as a known modification and place it on the first/last amino acid. 
h.	Select your fragmentation technique. 
i.	If you would like to search for specific fragments they can be checked/unchecked under "Search Fragment Type".
j.	If you are searching for fragments that contain c or z cleavages, you can exclude cleavages that occur at proline residues. By checking the last box. 
3. Click "Run Program".
4. If you are looking for internal and terminal fragments a dialog box will ask if you want to bias for terminal fragments. Click yes if you want to bias for terminal fragments or no if you want to treat terminal fragments and internal fragments as equally likely.
5. Depending on the sequence length, the number of observed fragments, and the types of fragments searched, the program could run from ~5s to ~1hour.
6. Once completed, a "Matched_Fragments_File.csv" file should appear in the folder with all matched fragments.
7. 3 Figures should be output from the program indicating the fragment location, the sequence coverage, and the cleavage sites. (These are located in the folder containing all of the other files)
If you have any questions or concerns email: internalfragments.loolab@gmail.com
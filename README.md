<h1 align="center">Antimicrobial Resistance Detection Workflow</h1>


<h3 align="center">M. Asaduzzaman Prodhan<sup>*</sup></h3>


<div align="center"><b> School of Biological Sciences, The University of Western Australia </b></div>


<div align="center"><b> 35 Stirling Highway, Perth, WA 6009, Australia. <sup>*</sup>Correspondence: prodhan82@gmail.com </b></div>


<br />


<p align="center">
  <a href="https://github.com/asadprodhan/How-to-automatically-download-reads-from-the-NCBI-SRA/tree/main#GPL-3.0-1-ov-file"><img src="https://img.shields.io/badge/License-GPL%203.0-yellow.svg" alt="License GPL 3.0" style="display: inline-block;"></a>
  <a href="https://orcid.org/0000-0002-1320-3486"><img src="https://img.shields.io/badge/ORCID-green?style=flat-square&logo=ORCID&logoColor=white" alt="ORCID" style="display: inline-block;"></a>
</p>


<br />


<br />


## **FastQC Analysis**

### **Step 1: Bring the raw data in the Terminal**


- Open the Termnal

- write cd and then drag the directory containg the fastq.gz files. It will show as follows:

```
cd "path-of-the-directory"
```

- Hit enter

- Check the fastq.gz files by running 


```
ls
```
 
### **Step 2: Set a conda environment**

Run the follwoing commands one by one

```
conda
```

> If it shows the usage options, then you have conda installed.
If it show "command not found", then you don't have conda installed.
To install conda follow: https://github.com/asadprodhan/A-beginner-s-guide-to-Bioinformatics#how-to-install-conda-in-my-computer

Now, run

```
conda create -n amr
```

```
conda activate amr
```

```
conda install -c bioconda fastqc
```

### **Step 4: Create a directory to collect the fastqc results**

- Create a directory to collect the fastqc results

```
mkdir fastqc_results
```

### **Step 5: Run FastQC**

```
for file in *.fastq.gz; do fastqc $file -o ./fastqc_results/ -t 16 -Xmx20g; done 
```

Then

```
cd fastqc_results
```

```
ls
```

You will see the fastqc reports here.




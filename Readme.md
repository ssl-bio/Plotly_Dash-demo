# Plotly Dash Demo

A Plotly Dash app that summarizes the analysis of mRNA degradation fragments using a third party script (`PyDegradome`, (<a href="#citeproc_bib_item_1">Gaglia, Rycroft, and Glaunsinger 2015</a>) followed by a custom classification. The analysis uses the data from the work of <a href="#citeproc_bib_item_3">Zhang et al. 2021</a> and <a href="#citeproc_bib_item_2">Oliver et al. 2022</a>.

The app is divided in two pages, one where the analysis of mRNA degradation fragments is described along with some characteristics of the app itself and another where the results of the analysis are presented.

Regarding the second page organization:

-   The first section allows to select which dataset is shown.
-   Next, the user should select one of three settings (`PyDegradome`) used for the analysis.
-   The selection would update a barplot that summarizes the number of results (genome regions with significant accumulation of mRNA degradation fragments, *i.e.* ***peaks***). Two dropdown menus allow to display the counts according to different criteria and two additional menus allow to filter out some classification criteria or groups.
-   The next section displays a table with the transcripts associated with each peak along with data about the classification. Next to the table three different plots are available on tabs. The first plot shows all the degradation fragments found along the transcript; next to it is another plot showing the degradation fragments around the peak region; and the third one shows a cartoon with the potential alignment of a sequence around the peak region with a known miRNA species, the latter only when the alignment value was above a certain threshold.
-   The next section allows the user to search on pubmed (PMC, database) for literature mentioning one or more of the transcripts. These are selected using a checkbox on the table above. Additional search terms could be included in a search field. Note that for the search to be conducted an e-mail address [registered on NCBI](https://account.ncbi.nlm.nih.gov) is needed. The results of the search are displayed on a table with links to the publication website and, below it, the article's abstract. Each row has a checkbox to select and download the bibliographic information (`medline` format).
-   A floating icon allows the user to open a panel for taking notes in plain format which can also be downloaded.


# Running the app


## Virtual environment setup

```bash
# Create a new environment on the same folder
# where the app is
python3 -m venv venv

# Activate the environment
source venv/bin/activate

# Install the requirements
pip install -r min_requirements.txt
```


## Run the app

```bash
# On the activated environment
python app.py
```


# Further details

Details and code for the analysis of degradation fragments are provided on another [repository](https://github.com/ssl-bio/Degradome-analysis)


# References
<div class="csl-bib-body">
  <div class="csl-entry"><a id="citeproc_bib_item_1"></a>Gaglia, Marta Maria, Chris H. Rycroft, and Britt A. Glaunsinger. 2015. “Transcriptome-Wide Cleavage Site Mapping on Cellular mRNAs Reveals Features Underlying Sequence-Specific Cleavage by the Viral Ribonuclease SOX.” Edited by Pinghui Feng. <i>Plos Pathogens</i> 11 (12): e1005305. doi:<a href="https://doi.org/10.1371/journal.ppat.1005305">10.1371/journal.ppat.1005305</a>.</div>
  <div class="csl-entry"><a id="citeproc_bib_item_2"></a>Oliver, Cecilia, Maria Luz Annacondia, Zhenxing Wang, Pauline E. Jullien, R. Keith Slotkin, Claudia Köhler, and German Martinez. 2022. “The miRNome Function Transitions from Regulating Developmental Genes to Transposable Elements during Pollen Maturation.” <i>The Plant Cell</i> 34 (2): 784–801. doi:<a href="https://doi.org/10.1093/plcell/koab280">10.1093/plcell/koab280</a>.</div>
  <div class="csl-entry"><a id="citeproc_bib_item_3"></a>Zhang, He, Zhonglong Guo, Yan Zhuang, Yuanzhen Suo, Jianmei Du, Zhaoxu Gao, Jiawei Pan, et al. 2021. “MicroRNA775 Regulates Intrinsic Leaf Size and Reduces Cell Wall Pectin Levels by Targeting a Galactosyltransferase Gene in Arabidopsis.” <i>The Plant Cell</i> 33 (3): 581–602. doi:<a href="https://doi.org/10.1093/plcell/koaa049">10.1093/plcell/koaa049</a>.</div>
</div>

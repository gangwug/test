### Well hello there!

This repository is meant to provide an example for *forking* a repository on GitHub.

Creating a *fork* is producing a personal copy of someone else's project. Forks act as a sort of bridge between the original repository and your personal copy. You can submit *Pull Requests* to help make other people's projects better by offering your changes up to the original project. Forking is at the core of social coding at GitHub.

After forking this repository, you can make some changes to the project, and submit [a Pull Request](https://github.com/octocat/Spoon-Knife/pulls) as practice.

For some more information on how to fork a repository, [check out our guide, "Forking Projects""](http://guides.github.com/overviews/forking/). Thanks! :sparkling_heart:

## tricky errors that experienced

## how to generate the token

https://stackoverflow.com/questions/68775869/support-for-password-authentication-was-removed-please-use-a-personal-access-to

Create Personal Access Token on GitHub
From your GitHub account, go to Settings => Developer Settings => Personal Access Token => Generate New Token (Give your password) => Fillup the form => click Generate token => Copy the generated Token, it will be something like ghp_sFhFsSHhTzMDreGRLjmks4Tzuzgthdvfsrta

## how to use the token

For Linux, you need to configure the local GIT client with a username and email address,

$ git config --global user.name "your_github_username"
$ git config --global user.email "your_github_email"
$ git config -l
Once GIT is configured, we can begin using it to access GitHub. Example:

$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
> Cloning into `Spoon-Knife`...
$ Username for 'https://github.com' : username
$ Password for 'https://github.com' : give your personal access token here
Now cache the given record in your computer to remembers the token:

$ git config --global credential.helper cache
If needed, anytime you can delete the cache record by:

$ git config --global --unset credential.helper
$ git config --system --unset credential.helper


## case 1:

RCPPARMADILLO AND OS X MAVERICKS "-LGFORTRAN" AND "-LQUADMATH" ERROR 

(https://thecoatlessprofessor.com/programming/cpp/rcpp-rcpparmadillo-and-os-x-mavericks-lgfortran-and-lquadmath-error/)

MACOS SIERRA (10.12) OR GFORTRAN 6.3.0
The following provides a procedure to use the macOS Sierra gfortran routine with R for those on macOS Sierra. Please note, if you installed the gfortran 6.1.0 binary, then do NOT use the directions below for installing gfortran 6.3.0.

First, download the official gfortran 6.3.0 binary for macOS Sierra (10.12) from http://gcc.gnu.org/wiki/GFortranBinaries#MacOS and then install it.

Next, we need to set a path in a file called ~/.R/Makevars, which handles compilation, so that it recognize the gfortran 6.3.0 binary. So, we’ll create a ~/.R/Makevars file – if one does not exist – and then add a special implicit variable called FLIBS that controls which Fortran library is used. This is detailed in Section 6.3.2: macOS of the R Installation and Administration

Open Terminal and type:

mkdir ~/.R
cat << EOF >> ~/.R/Makevars
FLIBS=-L/usr/local/gfortran/lib/gcc/x86_64-apple-darwin16/6.3.0 -L/usr/local/gfortran/lib -lgfortran -lquadmath -lm
EOF
LATER
Check back when new versions of R are released.

## case 2:

Error: package or namespace load failed for ‘gdtools’ in dyn.load(file, DLLpath = DLLpath, ...):
 unable to load shared object '/Library/Frameworks/R.framework/Versions/3.5/Resources/library/gdtools/libs/gdtools.so':
  dlopen(/Library/Frameworks/R.framework/Versions/3.5/Resources/library/gdtools/libs/gdtools.so, 6): Library not loaded: /opt/X11/lib/libcairo.2.dylib
  Referenced from: /Library/Frameworks/R.framework/Versions/3.5/Resources/library/gdtools/libs/gdtools.so
  Reason: image not found
  
Does all your packages complain about this? Library not loaded: /opt/X11/lib/libcairo.2.dylib Do you have package Cairo installed? Also, on which operating system are you? If you are on MAC OS try installing xquartz https://www.xquartz.org/


# Machine learning

## Unsupervised machine learning/clusering

NMF, k-means, DBSCAN

https://www.datanovia.com/en/blog/types-of-clustering-methods-overview-and-quick-start-r-code/

##CNN vs. RNN vs. ANN – Analyzing 3 Types of Neural Networks in Deep Learning

https://www.analyticsvidhya.com/blog/2020/02/cnn-vs-rnn-vs-mlp-analyzing-3-types-of-neural-networks-in-deep-learning/

##Deep Learning Project in Python with Keras Step-by-Step

https://machinelearningmastery.com/tutorial-first-neural-network-python-keras/

## Semantic segmentation introduction

https://www.superannotate.com/blog/guide-to-semantic-segmentation


# Reference links

## The-world-of-faculty

https://github.com/crazyhottommy/The-world-of-faculty


### graph gallery

https://www.r-graph-gallery.com/

http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html

Chart Combinations: Proportional Area Charts: https://datavizcatalogue.com/blog/chart-combinations-proportional-area-charts/

### ggplot2 tips

venn-diagram: https://scriptsandstatistics.wordpress.com/2018/04/26/how-to-plot-venn-diagrams-using-r-ggplot2-and-ggforce/

half-circle: https://stackoverflow.com/questions/28185743/draw-a-half-circle-with-ggplot2

position two legends independently in ggplot: https://stackoverflow.com/questions/13143894/how-do-i-position-two-legends-independently-in-ggplot

introduction about color blind friendly: http://jfly.uni-koeln.de/color/

distint colors: https://stackoverflow.com/questions/9563711/r-color-palettes-for-many-data-classes/41230685#41230685

c25 <- c(
  "dodgerblue2", "#E31A1C",
  "green4",
  "#6A3D9A", 
  "#FF7F00", 
  "gold1",
  "skyblue2", "#FB9A99",
  "palegreen2",
  "#CAB2D6", 
  "#FDBF6F",
  "gray70", "khaki2",
  "maroon", "orchid1", "deeppink1", "blue1", "steelblue4",
  "darkturquoise", "green1", "yellow4", "yellow3",
  "darkorange4", "brown", "black")

pie(rep(1, 25), col = c25)

install.packages("rcartocolor")
library(rcartocolor)
nColor <- 12
scales::show_col(carto_pal(nColor, "Safe"))

examples of color bind friendly: 

##blue panel

a = c("#00AFBB", "#0072B2", "#56B4E9", "#33BBEE")

##red panel

b = c("#FC4E07", "#D55E00", "#EE3377", "#E7298A")

##orange panel

c = c("#E7B800", "#E69F00", "#D95F02")

##yellow panel

d = c("#DDCC77", "#E6AB02", "#A6761D")

##green panel

e = c("#1B9E77", "#009E73", "#66A61E")

##purple panel

f = c("#CC79A7", "#7570B3")

##other panel: "#7E6148B2"(grey)

ca = c(a,b,c,d,e,f)

caD = data.frame(ca = ca, xp = 1:length(ca), yp = 1:length(ca)) %>% dplyr::mutate(ca = factor(ca, levels = ca))

ggplot(data = caD, aes(x = xp, y = yp, color = ca)) + geom_point(size = 6) + scale_color_manual(values = ca)


###use RColorBrewer

library(RColorBrewer)

n <- 60

qual_col_pals = brewer.pal.info[brewer.pal.info$category == 'qual',]

col_vector = unlist(mapply(brewer.pal, qual_col_pals$maxcolors, rownames(qual_col_pals)))



##creating a Timeline graphic using R and ggplot2: http://benalexkeen.com/creating-a-timeline-graphic-using-r-and-ggplot2/

##annotate outside the plot: https://stackoverflow.com/questions/12409960/ggplot2-annotate-outside-of-plot

### draw figures with multiple panels

#arrange the figures with 'gridExtra' package

https://cran.r-project.org/web/packages/gridExtra/vignettes/arrangeGrob.html

http://www.sthda.com/english/articles/24-ggpubr-publication-ready-plots/81-ggplot2-easy-way-to-mix-multiple-graphs-on-the-same-page/

http://rstudio-pubs-static.s3.amazonaws.com/2852_379274d7c5734f979e106dcf019ec46c.html

#using cowplot

https://beep-boopr.github.io/ubcBIOL548L/articles/group-03_Using-cowplot-multi-panel.html

#align plot panels

https://cran.r-project.org/web/packages/egg/vignettes/Ecosystem.html

#specify a second axis

https://ggplot2.tidyverse.org/reference/sec_axis.html

#Modifying facet scales in ggplot2

https://fishandwhistle.net/post/2018/modifying-facet-scales-in-ggplot2/

#discussion about 'plotting multiple panels of UpSetR'

https://github.com/hms-dbmi/UpSetR/issues/105

##free software

https://enviragallery.com/5-free-alternatives-to-photoshop/


#UMAP and t-SNE

https://cran.r-project.org/web/packages/umap/vignettes/umap.html

https://www.r-bloggers.com/playing-with-dimensions-from-clustering-pca-t-sne-to-carl-sagan/

https://www.r-bloggers.com/quick-and-easy-t-sne-analysis-in-r/

#multiple density plot (geom_density_ridges)

http://www.sthda.com/english/articles/32-r-graphics-essentials/133-plot-one-variable-frequency-graph-density-distribution-and-more/


### data tidy

#general:

http://garrettgman.github.io/tidying/

#replace multiple values:

plyr::mapvalues(wtime, from = c(6, 18, 12, 0), to = c("6am", "6pm", "12pm", "12am"))

#easy way of generate combinations of two vectors

expand.grid(height = seq(60, 80, 5), weight = seq(100, 300, 50), sex = c("Male","Female"))

#the introduction about map, pmap, imap

http://zevross.com/blog/2019/06/11/the-power-of-three-purrr-poseful-iteration-in-r-with-map-pmap-and-imap/

#the introduction about time formatting and convertions

https://www.flutterbys.com.au/stats/tut/tut3.4.html


#mine the Pubmed text 

https://rstudio-pubs-static.s3.amazonaws.com/235239_f75d5005bc0f4015bd97fb4be182144a.html


#dimension reduction

https://rpubs.com/Saskia/520216


#DBSCAN: density-based clustering for discovering clusters

http://www.sthda.com/english/wiki/wiki.php?id_contents=7940

### statistical soup

##solve the issue of getting different results with set.seed() from different R versions:

https://community.rstudio.com/t/getting-different-results-with-set-seed/31624

##about ANOVA, ANCOVA, MANOVA, & MANCOVA

http://www.statsmakemecry.com/smmctheblog/stats-soup-anova-ancova-manova-mancova

https://cran.r-project.org/web/packages/MANOVA.RM/vignettes/Introduction_to_MANOVA.RM.html

http://www.sthda.com/english/wiki/manova-test-in-r-multivariate-analysis-of-variance

###the demo of one way anova plus posthoc analysis

https://www.statology.org/one-way-anova-r/

https://www.scribbr.com/statistics/anova-in-r/


##posthoc analysis after ANOVA analysis

https://statisticsbyjim.com/anova/post-hoc-tests-anova/

https://www.statology.org/anova-post-hoc-tests/


##example of fisher exact test

https://www.biostars.org/p/252937/

##hazard ratio calculation

http://www.sthda.com/english/wiki/cox-proportional-hazards-model

##Regularized Regression

https://bradleyboehmke.github.io/HOML/regularized-regression.html

##Cox Proportional-Hazards Model

http://www.sthda.com/english/wiki/cox-proportional-hazards-model


### shinyapps

#general:

http://shiny.rstudio.com/articles/shinyapps.html

https://github.com/trestletech/dallas-police/

#adding hyperlinks to Shiny plots

https://stackoverflow.com/questions/32057164/adding-hyperlinks-to-shiny-plots

### interactive plots

The Wilke Lab: https://wilkelab.org/SDS375/slides/interactive-plots.html#1

### R Shiny app tutorial # 10 - download plot in shiny- PDF, PNG

https://www.youtube.com/watch?v=LSnWGmVkB6A&ab_channel=AbhinavAgrawal

### useful packages

#anatogram of human and mouse

https://github.com/jespermaag/gganatogram

#lubridate package

https://cran.r-project.org/web/packages/lubridate/vignettes/lubridate.html

https://data.library.virginia.edu/working-with-dates-and-time-in-r-using-the-lubridate-package/

https://bookdown.org/hneth/ds4psy/10-3-time-lubridate.html


### Chinese introduction about S4 class

https://my.oschina.net/bgbfbsdchenzheng/blog/540968

### develop R package

https://tinyheero.github.io/jekyll/update/2015/07/26/making-your-first-R-package.html


### split-spot in SRA toolkit introduction

https://www.biostars.org/p/12047/

This is the description I received the following description from the SRA staff (Adam Stine).

The spot model is Illumina GA centric.  The flowcells have the locations where the adapters have stuck them to the glass of the lane.  There are X and Y coordinates that identify these 'spots'.   As the camera reads the fluorescent flashes during sequencing, the coordinates indicate which spot the new base is added to. 

### how do gene annotation to the array probe

http://biolearnr.blogspot.com/2017/05/bfx-clinic-getting-up-to-date.html

https://support.bioconductor.org/p/85002/

### The UCSC genome brower coordinate (0-start vs 1-start)

https://genome-blog.soe.ucsc.edu/blog/2016/12/12/the-ucsc-genome-browser-coordinate-counting-systems/

### introduction about RNA-seq

https://www.labome.com/method/RNA-seq.html

### trim the adaptor sequence

https://dnatech.genomecenter.ucdavis.edu/faqs/when-should-i-trim-my-illumina-reads-and-how-should-i-do-it/

### how to skip the cache files during sra downloading

https://standage.github.io/that-darn-cache-configuring-the-sra-toolkit.html

mkdir -p ~/.ncbi
echo '/repository/user/main/public/root = "/scratch/standage/sra-cache"' > ~/.ncbi/user-settings.mkfg
#### #Uncomment the next command if you want to disable network access altogether
#### #echo '/repository/user/cache-disabled = "true"' > ~/.ncbi/user-settings.mkfg


### Julia-figures

https://gist.github.com/gizmaa/7214002

### good eBook links

R for Data Science: https://r4ds.had.co.nz/

Text Mining with R: https://www.tidytextmining.com/index.html

        a. Text Mining and Sentiment Analysis: Analysis with R: https://www.red-gate.com/simple-talk/sql/bi/text-mining-and-sentiment-analysis-with-r/

### good video links

how crispr works: https://www.youtube.com/watch?v=MnYppmstxIs


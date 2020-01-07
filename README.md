### Well hello there!

This repository is meant to provide an example for *forking* a repository on GitHub.

Creating a *fork* is producing a personal copy of someone else's project. Forks act as a sort of bridge between the original repository and your personal copy. You can submit *Pull Requests* to help make other people's projects better by offering your changes up to the original project. Forking is at the core of social coding at GitHub.

After forking this repository, you can make some changes to the project, and submit [a Pull Request](https://github.com/octocat/Spoon-Knife/pulls) as practice.

For some more information on how to fork a repository, [check out our guide, "Forking Projects""](http://guides.github.com/overviews/forking/). Thanks! :sparkling_heart:


## Reference links

### graph gallery

https://www.r-graph-gallery.com/

http://r-statistics.co/Top50-Ggplot2-Visualizations-MasterList-R-Code.html


### ggplot2 tips

venn-diagram: https://scriptsandstatistics.wordpress.com/2018/04/26/how-to-plot-venn-diagrams-using-r-ggplot2-and-ggforce/

half-circle: https://stackoverflow.com/questions/28185743/draw-a-half-circle-with-ggplot2

position two legends independently in ggplot: https://stackoverflow.com/questions/13143894/how-do-i-position-two-legends-independently-in-ggplot

introduction about color blind friendly: http://jfly.uni-koeln.de/color/

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


##creating a Timeline graphic using R and ggplot2: http://benalexkeen.com/creating-a-timeline-graphic-using-r-and-ggplot2/

### draw figures with multiple panels

#arrange the figures with 'gridExtra' package

https://cran.r-project.org/web/packages/gridExtra/vignettes/arrangeGrob.html

http://www.sthda.com/english/articles/24-ggpubr-publication-ready-plots/81-ggplot2-easy-way-to-mix-multiple-graphs-on-the-same-page/

http://rstudio-pubs-static.s3.amazonaws.com/2852_379274d7c5734f979e106dcf019ec46c.html

#align plot panels

https://cran.r-project.org/web/packages/egg/vignettes/Ecosystem.html

#discussion about 'plotting multiple panels of UpSetR'

https://github.com/hms-dbmi/UpSetR/issues/105

##free software

https://enviragallery.com/5-free-alternatives-to-photoshop/


#UMAP and t-SNE

https://cran.r-project.org/web/packages/umap/vignettes/umap.html

https://www.r-bloggers.com/playing-with-dimensions-from-clustering-pca-t-sne-to-carl-sagan/

https://www.r-bloggers.com/quick-and-easy-t-sne-analysis-in-r/


### data tidy

#general:

http://garrettgman.github.io/tidying/

#replace multiple values:

plyr::mapvalues(wtime, from = c(6, 18, 12, 0), to = c("6am", "6pm", "12pm", "12am"))


### statistical soup

##solve the issue of getting different results with set.seed() from different R versions:

https://community.rstudio.com/t/getting-different-results-with-set-seed/31624

##about ANOVA, ANCOVA, MANOVA, & MANCOVA

http://www.statsmakemecry.com/smmctheblog/stats-soup-anova-ancova-manova-mancova

https://cran.r-project.org/web/packages/MANOVA.RM/vignettes/Introduction_to_MANOVA.RM.html

http://www.sthda.com/english/wiki/manova-test-in-r-multivariate-analysis-of-variance


### shinyapps

#general:

http://shiny.rstudio.com/articles/shinyapps.html

https://github.com/trestletech/dallas-police/

#adding hyperlinks to Shiny plots

https://stackoverflow.com/questions/32057164/adding-hyperlinks-to-shiny-plots


### Julia-figures

https://gist.github.com/gizmaa/7214002

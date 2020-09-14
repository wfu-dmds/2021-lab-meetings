# Agenda

## 2020-09-14

### General

### Iris Liu

### Hannah Luebbering

### Hannah Mendoza

* Accomplished 
  * Added bio via Jonathan's guide (thank you!)
  * Began working through happygitwithr tutorial
    - made sure I had Git installed, created and threw away a test repo to make sure things were working properly
    - connected RStudio to Git + GitHub
  
* Next steps

### Nuri Park

1. What I accomplished this week
 - I was able to go through little bit of learnR modules. I kept losing connection during the weekends. 
 - have few commens/questions regarding learnR modules. 
2. What I expect to accomplish next week
 - Finish learn R modules. 
3. Any questions that I have 
 - What kind of resources did you use to develop learnR modules? 
  * [Learnr help files](https://rstudio.github.io/learnr/#Exercises)
  * [Learnr GitHub for examples](https://github.com/rstudio/learnr/tree/master/inst/tutorials/)

### Jonathan Trattner

* Accomplished
  * Added [first draft of demographic sample code](https://github.com/LucyMcGowan/teaching-r-study/pull/3).

* Next Steps
  * Automating the demographic code. 
    * I would appreciate your help with rlang evaluation (looking at the `getUICode` from the PR).
    * I want to turn it into a Shiny module that takes in a csv file and returns the UI/server for capturing demographic info.
 
* General Questions
  * On [shinyapps.io](https://www.shinyapps.io) can we test whether `session$clientData$url_port` will provide a unique ID? That should be able to interface with Shiny/learnr documents.
  * R packages for fMRI analysis

## 2020-09-07

### General

* Introductions
* Website updates (https://dmds.lucymcgowan.com)

### Nuri Park

* What I accomplished this week
* What I expect to accomplish next week
* Any questions that I have 

### Jonathan Trattner

* Senior thesis:
  * Discussing features of `taskdesignr` and next steps.
* General R questions
  * Neuroimaging R packages
    * Do you (or any colleagues) have any recommendations?
  * Code optimization
    * Faster alternatives to `transmute()` with user-supplied column names:
    ```r
    # the following is inside a function
    # id, S1, and S2, are strings
    # diff and mean are numeric vectors
    output <- data %>%
      dplyr::transmute(id = .data[[id]],
             "{{variable}}_1" := data[[S1]],
             "{{variable}}_2" := data[[S2]],
             "{{variable}}_diff" := diff,
             "{{variable}}_mean" := mean)
   ```

### Hannah Luebbering

* Projects/ research tasks:
  * Shiny/ Learnr study
    * [link](https://github.com/hluebbering/shiny-learnr-study) to documentation
  * Tutorials for R `tidyverse` package
    * [explaining tidy data](https://github.com/hluebbering/explaining-tidy-data)
    * [base list data frame](https://github.com/hluebbering/base-list-data-frame)
    * [using tidyvsere package to manipulate data](https://github.com/hluebbering/tidyverse-manipulating-data)
 
* Goals:
  * Continue Shiny/ Learnr study
  * Format documents based on [Wiley Online Library](https://onlinelibrary.wiley.com/page/journal/20491573/homepage/forauthors.html) submission guidelines 
  * Tidycode
  * Help develop shiny applications in the classroom
  

* Questions 
  * As Jonathan mentioned, is it possible to conduct studies for Neuroimaging/ Neuroscience based R packages?
  * How do you develop an R package?
  * Is the tidycode package fully developed? If not, is there ongoing work for the package that I could help with?
  

  

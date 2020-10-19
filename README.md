# Agenda

## 2020-10-19

### General

* Adding a 30 minute meeting on Wed/Thurs?

### Hannah Luebbering
 * What I accomplished this week
   * Added studies teaching how to program in R to the lit review
   * Wrote an introductory draft for study on teaching R 
 
 * Next steps
   * Continue finding studies/ research
   * Revise introductory draft
   
 * Questions
   * What other sections of paper could I help with?
   
### Jonathan Trattner

* Accomplished
  * Finished first draft of survey vignette.
  * Created displayDocument code for informed consent or other documents.
* Next Steps
  * Create screen functions to display graphics, questions, choice buttons, sliders, etc.
    * Do you think the general structure of the defineRun/defineTrial would work?
* General Questions
  * Would anyone be willing to go through my vignette and give me feedback?
  * Should I attempt to integrate the survey code with the teaching_r_study? If so, what do I need to know?
  
### Hannah Mendoza 

* Accomplished 
  * Completed CITI training
  * IRB submitted (?)
  * Looked into SurveyMonkey + Prolific
* Next steps 
  * Check that survey is set up 
  * Check on IRB approval 
  * figure out revised time line for the rest of the semester
* Questions
  * How do submissions/presentations work for December grads? If you're not sure, whom should I ask? I realized I'm not entirely sure what my final deadline is
  
### Presentation: Jonathan
  
## 2020-10-12

### General

### Sophia Fang
 * What I accomplished this week
   * Went through Chapter 1-4 and came up with course objectives for each chapter
 
 * Next steps
   * Continue on course materials from Chapter 5
   * Revise previous course objectives
   
 * Questions
   * Some of the objectives might be too detailed. I would like them to be more concise.

### Jonathan Trattner

* Accomplished
  * Finalized the first draft of the survey code. UI function is named `surveyUI()` and `surveyServer()`.
  * Added URL-based user tracking to the survey code.
  * Began writing survey code vignette.
* Next Steps
  * Finish writing the survey code vignette.
  * Develop a function to add an informed consent document to the Shiny app.
* General Questions
  * MongoDB help!
  * AWS?
  
### Nuri Park
 * What I accomplished this week
   * Instead of adding exercise, I added a code in the 'Subsetting tibbles' section where the "df" was not clear before showing example.
   * Reviewed assessment questions
     * I think they do adequately map module lessons; however, I am still confused about the last question on the assessment.
     * It'd be good to have one question on using logical vector (something like "save a new column that has (blah) over 100")
 
 * Next steps
   * Finalize modules, I will go over module one more time and hope to fix all the errors with the help of Dr. McGowan (by October 19th) 
   
 * Questions
   * Do you think we need to introduce rbind function with cbind? 
   * Who are the initial groups that need to be enrolled by November 2nd? Do we collect data from them, and How? 
   
### Hannah Mendoza 

  * Accomplished 
    * 1 (out of 11) module left in CITI training 
    * updated [IRB document](https://docs.google.com/document/d/1XtIwPoIvB-qvfL7Ei9gXVYNDMF1VcG6SlvRDpLDnDhY/edit?usp=sharing) with background, methods, purpose
    * read through write up on Likert analyses 
    
  * Next steps
    * plan analyses 
    * submit IRB 
    * complete final module of CITI training
    * look into setting up survey?
    
  * Questions
    * What else can I be working on? 
  
## 2020-10-05

### General 

* Iris practice talk on 10/19 at 10am

### Nuri Park
 * What I accomplished this week
   * Attempted to fix errors but not successful
   * Added one exercise to "vector, lists, and data frames"
 
 * Next steps
   * Hope to add more exercises to the LearnR modules
   
 * Questions
   * Can you help me fixing errors? 
   * Can you review exercise that I added? 
   
   
### Jonathan Trattner

* Accomplished
  * Added UI and server code for required questions for taskdesignr.
  * Improved dependence functionality.

* Next Steps
  * Setting question defaults.
    * Need help with this please. Errors are the same as when we looked at it last week. 
  * Fixing required server code for dependency questions.
    * I also need help with this please. I have a draft but cannot figure out why it doesn't work.
  * Figure out how to track participants across sessions.
    * Perhaps we can tackle the teaching_r_study problem by using the taskdesignr package. I'm thinking we could use an internal enviornment if we have the demographics form contain a username entry? 
* General Questions
  * Best way to modularize code with conditions?
    * I have two variables passed into a function, sex and race. The function needs to do different things depending on if one is NULL and the other isn't, they are both NULL, or they both have values. There are four conditions. How would you best handle it? As an example, one operation the function does is assign names to a dataframe:
    
    ```r 
    if (is.null(sex) & is.null(race) {
    names(output) <- c("id",
                     paste0(variable, "_1"),
                     paste0(variable, "_2"),
                     paste0(variable, "_diff"),
                     paste0(variable, "_mean"))
    } else if (is.null(sex) & !is.null(race)) {
      names(output) <- c("id",
                     paste0(variable, "_1"),
                     paste0(variable, "_2"),
                     paste0(variable, "_diff"),
                     paste0(variable, "_mean").
                     paste0(race, "_1"),
                     paste0(race, "_2"))
    } else if (!is.null(sex) & is.null(race)) {
      names(output) <- c("id",
                     paste0(variable, "_1"),
                     paste0(variable, "_2"),
                     paste0(variable, "_diff"),
                     paste0(variable, "_mean").
                     paste0(sex, "_1"),
                     paste0(sex, "_2"))
    } else if (!is.null(sex) & !is.null(race)) {
  
     names(output) <- c("id",
                     paste0(variable, "_1"),
                     paste0(variable, "_2"),
                     paste0(variable, "_diff"),
                     paste0(variable, "_mean").
                     paste0(sex, "_1"),
                     paste0(race, "_2"),
                     paste0(race, "_1"),
                     paste0(race, "_2"))
  
    }
    ```
    
### Hannah Mendoza 

* Accomplished this week 
  * Finalized topic + questions for survey 
  * Began CITI training (about halfway through) 

* Next steps 
  * Finish CITI training 
  * Read [write up](https://bookdown.org/Rmadillo/likert/always-visualize.html) on Likert analyses
  * Update IRB document with Background, Purpose, Methods
  
* Questions 
  * For CITI training, want to verify the course should be Human Subjects Research > Social-Behavioral 

## 2020-09-28

### General

### Nuri Park

* What I accomplished this week
  * Uploaded the timeline for thesis
  * look through the module and came up with few more example ideas

* Next steps
  * Attemp to fix errors

### Hannah Luebbering

* What I accomplished this week
  * Added a bio to our website
  * Feedback for [shinyapps-tutorial](https://lucy.shinyapps.io/tutorial-a/)
    * On assessment tabs, an Error message occurred stating to check logs
  * Looked over the teaching-r-study GitHub repo
    
* Next Steps
  * Continue to look over teaching-r-study GitHub repo
* General Questions
  * Is there any code I can help with in the teaching-r-study GitHub repo?

### Hannah Mendoza

* What I accomplished this week
  * Thought more deeply about survey questions, potential questions and topics [here](https://docs.google.com/document/d/1-wDLorEabuuIfkZjo0fOG53aLlsBDB2E31fZ4RoYNYM/edit?usp=sharing).
  * Read article shared last week for ideas about conveying uncertainty for action-threshold decisions
 
* Next steps 
  * Select + revise questions for IRB
  * think about and sketch out analyses to perform on data after we close survey

* Questions 
  * Do you have a bit of time this week to work 1:1 on these questions? Maybe Wednesday when we talk about Twitter, or we can find more time if we need? 

* Look into prolific: https://www.prolific.co
## Sophia Fang

* What I accomplished this week 
  * Accept the invitation

* Next steps

* Questions

## 2020-09-21

### General

* Website
* ASA Women in Statistics Twitter volunteer
* Moving learnr modules to this GitHub Org

### Nuri Park

* What I accomplished this week
  * Added bio 
  * LearnR modules
    * errors 
      * reading data - connection error
      * second Assessment "read.csv" incorrect
      * last question on the second assessment is confusing. (I wasn't sure which function the question wants me to use)
      * Reading data section for tidy - exercise gave me an error 'data/airquality.csv' does not exist. 
      * manipulating data - object 'flights' not found
      
    * Suggestions:
      * Subsetting tibbles - it'd be better to have a whole "df" shown once again before examples. I was confused what is referring to. 
      * have more exercises (easy, intermediate, hard) 

### Jonathan Trattner

* Accomplished
  * Added [updated draft of demographic survey code](https://github.com/LucyMcGowan/teaching-r-study/pull/3).
  * Added [a tentative schedule for completing my thesis](https://github.com/wfu-dmds/lab-meeting/blob/master/trattner_thesis_schedule.pdf).

* Next Steps
  * Dealing with dependence questions (need help).
  * Conversion into Shiny Module (need guidance).
     * Potentially collaborate with Dean Attali? He has the package [shinyforms](https://github.com/daattali/shinyforms) which is not being actively developed.
 
* General Questions
  * R Packages for fMRI Analysis
  

### Hannah Mendoza

* Accomplished
  * Finalized thesis topic
  * Found 2014 [article](https://www.pnas.org/content/pnas/111/Supplement_4/13664.full.pdf) on communicating scientific uncertainty with types of decision making involving science communication, and some broad guidelines for conveying uncertainty
  * Made broad list of possible topics for survey questions with types of decisions (noted in the article above) in mind

* Next Steps
  * Finalizing topic(s) -- need help (see below)
  * Writing survey questions for topic with and without communication of uncertainty
 
* General Questions
  * Finalizing topic
    * What type of decision? 
    * Use historical/relevant issues or something more abstract/theoretical? I'm not sure if using real topics would be unhelpful if these examples of changing advice have already been put out into the world, or on the other hand, if using made up scenarios would be bad communication if they're plausible enough, or perhaps be so obviously wrong that the survey is moot

### Hannah Luebbering

* Accomplished 
* Next Steps
* General Questions

## 2020-09-14

### General

### Iris Liu

### Hannah Luebbering

- [x] add a bio to our website

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
  

  

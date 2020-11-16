# Agenda

## 2020-11-16 

### Sophia Fang
* Accomplished
  * Finished Chapter 7 and posted objectives

* Next Steps
  * Continue from Chapter 8
  
* Questions
  * Feedback if any

### Nuri Park
* Accomplished
  * Completed outline for introduction and methods section of the paper
  * Introduction - literature review, overview of LearnR, Shiny, Tidyverse, and Base R, shiny tools
  * Methods - recruitment, two-period cross-over study, controlled, randomized trial, measurements, demographics, statistical analysis, hypothesis

* Next Steps
  * Collect comments from professors/experts and make changes accordingly
  * Work on filling in more details for the paper
  
* Questions
  * What kind of demographics are we collecting?
  * Research goal: are we revising? 
  * Hypothesis 
  
  Minor Comments Along the Way
* Typo in "Vectors, Lists, Data Frames" I think you mean multiply not multiple, but technically you haven't introduced the multiply " * " operator yet (or subtraction, division, etc.)
* A common issue is that a student wants to check if x is less than or equal to -3, and writes "x<-3" and accidentally reassigns x.  Worth mentioning?
* The verbal explanations of && and || were not clear to me, but the student didn't need to use either.
* Your tasks ask to create objects, but the student can do it correctly and not have it display if they assign the object...
>data.frame(x,y) vs. >z <- data.frame(x,y) is what I have in mind.  This could cause confusion.  At first I thought my code wasn't running but then I realized I was only assigning and not displaying.
* For you exercise on adding a column to an object df, I think the computer scientists would bristle at using the same name "df" for the new object.  But I break this rule all the time.  What it means is that if a student runs their code more than once they could accidentally keep adding columns.  Not an issue for chunks in RMarkdown but an issue for R scripts or working in the console.
* Any reason you spell is "summarise"?  Seems British to me.
* I am in the Assessment, did you introduce a command to check the dimension of a data frame?  I don't recall.  A student can click the buttons at the bottom of the window displaying the data to see the answers, but they couldn't do that in an actual R analysis.
* The word "filter" is unfamiliar to me.  I have only ever heard subset.  I keep thinking you must mean something more specific.  You've used this term a few times by now.

Larger Overall Comments
* The number of activities throughout seems low relative to the number of concepts/commands you are teaching.  I am inclined to think students need to use most if not all of the commands you introduce in exercises.  By the time I got to "Indexing Vectors" I thought this may be moving too fast for some.  To a student who still doesn't immediately know what c() and brackets mean, the expression "y[c(TRUE, FALSE)]" is not likely to be clear.

* For what it's worth, I have never used nor heard of the R commands >aggregate() or >subset().  They are probably more efficient than what I do.  For subset I just treat a data frame as a matrix and write stuff like mtcars[(mpg>20),].  Maybe I am just outdated in this regard.  I mention this only because you wanted to know what this looks like to a base R user.

* Finally I'll level with you, I just completed it and the syntax for >subset() has already left my short-term memory.  I am not sure how long you intend students to work on this, but if these are the topics you want to cover I might suggest a few more exercises along the way, add a few that take 2-4 lines of code to complete "(first make ..., and then merge it with ..."), and I would revisit all of this a few days later with a guided lab or more open-ended task to make sure things stick. 
  
### Jonathan Trattner
* Accomplished
  * Not related to this lab, but I published my first package to CRAN!
  * Made some progress with task designer UI but wasn’t able to figure it out — would appreciate some more hands-on help.
* Next Steps
  * Launching Teaching R Study?
    * Creating two documents for each group.
    * Transferring documents to Dr. McGowan's shinyapps.io.
  * Finishing GUI and screen functions for taskdesignr.
* General Questions
  * Username functions
    * Did you have a chance to look at my tests for the username functions?
    * Could we talk about SQL integration?
  * CRAN reference manual — how could I delete internal functions?
  * Could you explain `UseMethod`? 
  * Can I automate scripts in R without using my personal laptop?
    * For example, how could I re-execute a script every 24 hours or every time a database changes?
  * Does the university have a shinyapps.io plan I could utilize? I ran out of space on my free plan...
  
### Hannah Mendoza 
* Accomplished 
  * Got together most of intro+methods
  * Visualizations for responses to Q1 and Q2 by treatment
  * Table with baseline variables - looks pretty balanced; will definitely fit models for male/female separately in addition to the full one
  * started analysis with orm in rms package
* Next steps 
  * work on finishing fitting the models and interpreting them
  * incorporate better descriptions of the visualizations
* Questions 
  * visualizing the probabilities for scoring 1-5 based on treatment: I think I've figured out how to pull these pretty easily, but for visualizing these results, should I use a line graph like they do [here](https://bookdown.org/Rmadillo/likert/is-there-a-significant-difference.html#proportional-odds-regression)? That seems like a slightly confusing visualization to me but I'm not sure
  
## 2020-11-09

### Jonathan Trattner
* Accomplished
  * Updated the [welcome page](https://jdtrat-apps.shinyapps.io/teaching_r_study_welcome/) and integrated it with the survey and learnr modules. 
    * Everything opens in the same window.
    * Usernames are assigned upon consent
  * Created functions to add and remove usernames.
    * These should be more generalized and flushed out if we wish to include them other places. Right now they're very specific to the Teaching R Study.
  * Worked on GUI for creating Shiny UI (taskdesignr).
    * Need help saving images for dynamic uploading
* Next Steps
  * Launching Teaching R Study?
    * Creating two documents for each group.
    * Transferring documents to Dr. McGowan's shinyapps.io.
  * Finishing GUI and screen functions for taskdesignr.
    * Begin working on trial structure.
    * Colin Fay is working on [multipage Shiny apps](https://twitter.com/_ColinFay/status/1324799785661091842), but it may not be ready for a little bit. Could we reach out to him and talk about incorporating it?
  * Generalizing the usernames functionality. 
    * Perhaps translating to SQL databases instead of Dropbox? Or adding functionality for it in addition?
    * Adding a check for when the username groups are not equal (when get_username was unequally run for different groups) as below, there may be a problem with adding or removing usernames.
    
```r
purrr::walk(.x = c(rep("A", 4), rep("B", 5)),
            ~ get_username(.x,
                           'teaching-r-study/'))       
```
* General Questions
  * Can you help me improve the tests in the file testing_add_usernames.R (i.e. help converting into formal unit tests with testthat)?
  
### Hannah Mendoza 

* Accomplished this week 
  * Got more familiar with data and visualizations and functions with first 150 observations 
  * Worked on draft of intro + methods sections 
  * began cleaning data set with all 600 observations (WIP) 
* Next steps 
  * finish cleaning
  * create table with baseline demographic variables by treatment
  * fit proportional odds models predicting Q2 from treatment
* Questions 
  * subsetting 
  

## 2020-11-02 WOW It's already November!! 

### Sophia Fang
* What I accomplished this week
  * Finished Chapter 6

* Next Steps 
  * Continue finishing Chapter 7
  * Revise if any feedbacks
  
* Questions
  * About next week

### Nuri Park
* What I accomplished this week
  * Dr. McGowan sent out modules to professors/experts
  * Fixed typo on the module (Thanks to Dr. Dalzell)
  
* Next Steps 
  * Wait for their comments/feedback and make adjustments accordingly.
  
* Questions
  * Is there anything that I need to do for my thesis paper while waiting for feedback?
   - [Plos Medicine most recent issue](https://journals.plos.org/plosmedicine/issue)
  
### Jonathan Trattner

* Accomplished
  * Posted draft of [survey](https://jdtrat-apps.shinyapps.io/teaching_r_study_demographics/?user_id=dmds_lab/) and [learnr modules](https://jdtrat-apps.shinyapps.io/teaching_r_study/?user_id=dmds_lab/)
* Next Steps
  * Debug deployed apps (check logs).
  * Add informed consent information that redirects to survey and then learnr modules.
    * Specific language for informed consent?
* General Questions
  * Using [sass](https://rstudio.github.io/sass/articles/sass.html) for allowing user-defined areas for Shiny UI elements
  * Unit testing
  
### Hannah Mendoza 
* Accomplished
  * Got IRB approval (Yay! Thank you Dr. D'Agostino McGowan for dealing with all of the back and forth!)
* Next steps 
  * Open survey
  * Use background + methods from IRB application as starting point for paper
* Questions
  * Anything big I should be doing in the meantime?
  
## 2020-10-26

### Nuri Park
* What I accomplished this week
  * I finished reviewing LearnR modules

* Next Steps
  * Send out modules to 4 professors/experts and collect initial data
  * Ask them for any suggestions
  
### Hannah Mendoza

* Accomplished 
  * Dr. D'Agostino McGowan created survey, I went through it several times to make sure everything looks good 
  * Responded to availability when2meet for presentations during the last week of classes
  * Revised timeline for the rest of the semester
* Next steps 
  * Open survey to start collecting data 
  
### Jonathan Trattner

* Accomplished
  * Confusing myself with CSS - Please help!
  * Not integrating survey questions with teaching_r_study
     * How is teaching_r_study going to be disseminated? I have some ideas and can walk through what I did.
* Next Steps
  * Finish creating screen functions to display graphics, questions, choice buttons, sliders, etc.
* General Questions
  * I had one but can't remember it right now, so hopefully I will think of it as we go!

## 2020-10-19

### General

* Adding a 30 minute meeting on Wed/Thurs?
  @LucyMcGowan send out when2meet for this!
  
 ### Sophia Fang
 * What I accomplished this week
   * Went through chapter 5 and summarized two course objectives
   * Sent course objectives for chapter 1 to 4
 
 * Next steps
   * Revise objectives if feedback received
   * Continue working on chapter 6 and beyond
   

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
  

  

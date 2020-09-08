# Agenda

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

* Projects/ research tasks
 * [explaining tidy data](https://github.com/hluebbering/explaining-tidy-data)
 * [base list data frame](https://github.com/hluebbering/base-list-data-frame)
 * [Using Tidyvsere to Manipulate Data](https://github.com/hluebbering/tidyverse-manipulating-data)
 
* Goals

* Questions 

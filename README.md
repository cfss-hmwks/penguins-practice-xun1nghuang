## R Markdown

Here we are going to learn a bit about penguins!

## Penguins

See below for averages on penguins.

    ## # A tibble: 3 × 3
    ##   sex    avg_bill avg_mass
    ##   <fct>     <dbl>    <dbl>
    ## 1 female     37.3    3369.
    ## 2 male       40.4    4043.
    ## 3 <NA>       37.8    3540

## Your work

Summarize the dataset in a meaningful way (use AT LEAST two of the key
functions from slide \#12)

    penguins %>% filter(sex == "male") %>% 
      group_by(island) %>%
      summarize(avg_bill = mean(bill_length_mm, na.rm = TRUE))

    ## # A tibble: 3 × 2
    ##   island    avg_bill
    ##   <fct>        <dbl>
    ## 1 Biscoe        47.1
    ## 2 Dream         46.1
    ## 3 Torgersen     40.6

# Final task

You need to make a README.md doc – practice by outputting a .md file
here and renaming it to README.md before pushing to github

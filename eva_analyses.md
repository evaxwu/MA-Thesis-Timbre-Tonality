Eva Analyses
================
Eva Wu
2022-05-19

## Explore correlation between music background & categorization / explicit rating

TBC

## Statistical Analyses

Descriptives, exploratory plot

``` r
# save data to be used
#attach(all)

# descriptives
#summary(cat_rtg)
#plot(instrument, pct_maj)
```

Correlations b/w 1) instrument’s presumed valence, 2) mean explicit
rating, and 3) tuning step & percent of major categorization, and
4)instrument’s presumed valence & mean explicit rating

``` r
#cor(cat_rtg$inst_id, cat_rtg$pct_maj)
#cor(cat_rtg$mean_rtg, cat_rtg$pct_maj)
#cor(cat_rtg$tuning_step, cat$pct_maj)
#cor(cat_rtg$inst_id, cat_rtg$mean_rtg)
```

Logistic regression

1)  Percent major \~ instrument & tuning step

``` r
#glm.fit <- glm(pct_maj ~ instrument + tuning_step, family = binomial) 
# family= binomial tells r to run logistic regression
#summary(glm.fit)
```

2)  Percent major \~ mean explicit rating of each instrument & tuning
    step

``` r
#glm.fit2 <- glm(pct_maj ~ mean_rtg + tuning_step, family = binomial) 
# family= binomial tells r to run logistic regression
#summary(glm.fit2)
```

Linear regression

``` r
#lm.fit2 <- lm(pct_maj ~ tuning_step, data = cat)
#lm.fit <- lm(pct_maj ~ instrument + tuning_step, data = cat) 
#summary(lm.fit)
```

ANOVA exploring 1) whether adding instrument as a predictor
significantly improves model, and 2) whether adding both predictors is
significantly better than null model

``` r
#anova(lm.fit, lm.fit2) # adding instrument significantly improves model
#anova(lm.fit) # adding both predictors significantly better than null model
```
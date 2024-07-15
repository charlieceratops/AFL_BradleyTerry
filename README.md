# The Footy Forte

This  repository contains the code and data to replicate the experiments in the thesis The Footy Forte: Factors impacting team strengths in the Australian Football League. The thesis focuses on estimating team strengths and predicting game results in advance in the Australian Football League.

This code was made by Carlos Rafael González Soffner. Anyone is welcome to
use these files or any part of them for their projects as long as they reference
this thesis, code or author/supervisor.

Bests,

Carlos.

## Abstract

Australian Rules Football is a field invasion game where two teams attempt to score the
highest points to win. There is extensive research on the use of complex Machine Learning
algorithms to predict match outcomes post-game, but their lack of interpretability hampers an
understanding of the factors that affect a team’s performance. Using data from the male
competition of the Australian Football League, seasons 2015 to 2023, this thesis estimates
team strengths and the factors impacting them by fitting three expansions of the
Bradley-Terry model. It finds that the model successfully identifies teams significantly
stronger or weaker than the average, with stronger teams placing higher in the previous
seasons’ ladder and leading the activity in the Forward 50 zone, goal shots and scoring over
their opponents. Moreover, playing at home is confirmed to create an advantage regardless of
team strengths. The ability of the model to predict game results in advance is tested, with the
expansions accounting for team-specific, time-variant features predicting up to 71.5% of
outcomes. The findings of this thesis imply that the Bradley-Terry model can provide an
interpretable understanding of team strengths and competitive game predictions, making it
optimal for data-driven strategies and training.

## Usage

### Fetching Data
Download *FETCHING_RESULTS_AND_LADDER.Rmd* and run the chunks in R Studio to retrieve the data used in this thesis. The data is also available in the folder *FETCHED DATA*.
  
  - LADDER_15TO23.csv: Ladder results, seasons 2015-23
  - PIS_15TO23.csv: Performance Indicator data, seasons 2015-23
  - last_ladder_position.xlsx: Final ladder position from the previous season, for seasons 2012-23
  - results_afl_tables_12TO23.csv: Game results, seasons 2012-23

Download *DATA PROCESSING.ipynb* and run the cells to perform the data processing for the different Bradley-Terry models. The processed data can also be found in the following folders.

  - *ST_DATA*: Datasets to fit the standard and contest-specific expansions of the Bradley-Terry model. One for each season and all the available data (2015-23, labelled as 2024)
  - *ST_DATA_TEST*: Test datasets for the standard and contest-specific expansions of the Bradley-Terry model. One for each season and all the available data (2015-23, labelled as 2024).
  - *TS_TV_DATA*: Datasets to fit the team-specific, time-variant expansion of the Bradley-Terry model. One for each season, separated by Home and Away teams and for both encodings of cumulatives (L4, ALL). There is also one dataset with all the available data (2015-23, labelled as FULL).

Download *BT_BASELINE_23_TRIAL.Rmd* and run the chunks in R Studio to replicate the results of the standard and contest-specific expansions of the Bradley-Terry model.

Download *TS_TV_BT.Rmd* and run the chunks in R Studio to replicate the results of the steam-specific, time-variant expansion of the Bradley-Terry model, and the results of the round-by-round predictions.


## The Impact of Winning Faceoffs on Expected Goals (xG) in Powerplays: An Analysis of 2020-2021 SHL Season Data

### Introduction
Over the last decade, the overall efficiency of powerplays in ice hockey has been
on the rise, suggesting an increasing importance placed on this aspect of the
game. Every powerplay starts with a faceoff, making it a crucial play as it pro-
vides a chance to gain possesion of the puck. Teams that can effectively take
advantage of their powerplay opportunities are more likely to score goals and
ultimately win games. As a result, teams are constantly seeking ways to improve
their powerplay.

In this context, analyzing the impact of winning faceoffs during powerplay
situations can provide valuable insights for teams seeking to enhance their pow-
erplay performance. By understanding the effect that winning faceoffs has on a
team’s expected goals (xG) during powerplays, teams can make more informed
decisions about their approach to powerplay situations, potentially leading to
improved overall performance.

### Research question
The aim of this study is to provide valuable insights for teams seeking to enhance
their powerplay performance by answering the following research question:

– How does winning a faceoff impact the expected goals during powerplays in
ice hockey?

### Background:
A previous study on faceoffs in the NHL has shown that faceoffs can have a
significant impact on a teams success over a full season (Schuckers, Tom Pasquali
and Jim Curro 2012). They found that it takes 40.9 faceoff wins in the powerplay
to gain a goal differential and 76.5 faceoff wins during even strength, suggesting
it is more important to win a faceoff during powerplay.

To analyze the effect of the faceoff result, it must be defined what events
should be attributed as a result of the faceoff. Compared to the previous study
by Schuckers, Tom Pasquali and Jim Curro, this study do not limit the impact
of the faceoff to 20 seconds as puck possesion is switching far less often during
powerplays. In this report, a simplistic approach has been chosen where a game
sequence has been defined as all powerplay events that happen between the
current faceoff and the next powerplay faceoff. If it is the last faceoff during the
powerplay, all events until the teams play with equal strength are included in
the game sequence.

The event data used in this research was acquired from Sportlogiq, as pro-
vided by LINHAC. The dataset covers 20 games from the 2020-2021 SHL sea-
son and contains over 76,000 rows, each representing a distinct game event. To
ensure anonymity, player and team names were substituted with numeric iden-
tifiers, and certain attributes were removed. Although the dataset captured 22
attributes for each event, only a subset of these attributes were deemed relevant
to the research question and were therefore analyzed.

### Method

The provided dataset was loaded into Python using the Pandas library. The
dataset was then divided into powerplay game seqeunces according to the def-
inition in section 3.2 of the report. All game sequences were then filtered so
that only the expected goals of the powerplay team were included in the game
sequences. The game sequences were then divided into two groups based on the
result of the faceoff.

Data from these two groups were then collected which included sum of all
goals, expected goals and total time. This allowed for calculation of the expected
goals per 60 minutes (xG/60).

### Results

A total of 244 faceoffs were analyzed during 135 penalties. Of these, 148 faceoffs
were won and 96 were lost by the powerplay team. When the powerplay team
won the faceoff, 24 goals were scored with an expected goals (xG) of 16.44,
resulting in an xG/60 of 8.17. In contrast, when the powerplay team lost the
faceoff, 8 goals were scored with an xG of 8.31, resulting in an xG/60 of 5.90.

<img src="./images/table.png"  width="500" >

The results indicate a significant difference in the xG per 60 minutes when
comparing faceoff wins and losses. Winning a faceoff during a powerplay situation
led to an increase in xG per 60 minutes by 38% (8.17 xG/60 min vs. 5.90 xG/60
min).

<img src="./images/xg.png"  width="500" >


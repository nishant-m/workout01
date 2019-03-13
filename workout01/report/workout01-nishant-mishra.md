workout01-nishant-mishra
================
Nishant Mishra
12/03/2019

##### Effective Shooting % By Player (2PT %)

| Name           | Total | Made | % Made |
|----------------|-------|------|--------|
| Andre Iguodala | 210   | 134  | 63.81  |
| Kevin Durant   | 643   | 390  | 60.65  |
| Stephen Curry  | 563   | 304  | 54.00  |
| Klay Thompson  | 640   | 329  | 51.41  |
| Draymond Green | 346   | 171  | 49.42  |

##### Effective Shooting % By Player (3PT %)

| Name           | Total | Made | % Made |
|----------------|-------|------|--------|
| Klay Thompson  | 580   | 246  | 42.41  |
| Stephen Curry  | 687   | 280  | 40.76  |
| Kevin Durant   | 272   | 105  | 38.60  |
| Andre Iguodala | 161   | 58   | 36.02  |
| Draymond Green | 232   | 74   | 32.00  |

##### Effective Shooting % By Player (Total)

| Name           | Total | Made | % Made |
|----------------|-------|------|--------|
| Draymond Green | 578   | 333  | 57.61  |
| Kevin Durant   | 915   | 495  | 54.10  |
| Andre Iguodala | 371   | 192  | 51.75  |
| Klay Thompson  | 1220  | 575  | 47.13  |
| Stephen Curry  | 1250  | 584  | 46.72  |

The Tendencies of the All-Time-Great Golden State Warriors of 2016
==================================================================

It is easy to look at the numbers behind the five starters of the Golden State Warriors and arrive at a simplistic conclusion regarding their greatness on offense. With two (if we are being conservative and not including Durant) of the best three-point shooters of all time on the team, their shooting, undoubtedly, plays a key role in their success. But what about everything else? What are the other tendencies of the players on the Warriors on offense? What do they do tend to do? If we were to gameplan to play against the Warriors, what should we look out for? The purpsoe of this article is exactly that - to look at the tendencies of each of the players on the starting five of the Golden State Warriors, and ultimately, to gameplan for how a team of pickup players could possibly stop this offensive juggernaut the likes of which we have never seen and will likely never see again.

### Draymond Green

![](http://a.espncdn.com/combiner/i?img=/i/headshots/nba/players/full/6589.png&w=350&h=254)

A veteran of 6 years, Green is without a doubt the heart and soul of this Warriors team. He consistently plays at a Defensive Player of the Year level, and the team undoubtedbly runs through him. But how good is he on offense? Below, we can take a look at his shot chart.

![](https://github.com/nishant-m/workout01/blob/master/workout01/images/draymond-green-shot-chart.png?raw=true)

##### Green Shot Tendencies

``` r
summarise(green, 
          Jump_Shots = nrow(filter(green, action_type == "Jump Shot")),
          Layup_Shots = nrow(filter(green, action_type == "Layup Shot")),
          Pullup_Jump_Shots = nrow(filter(green, action_type == "Pullup Jump shot")),
          Tip_Layup_Shots = nrow(filter(green, action_type == "Tip Layup Shot")),
          Cutting_Dunk_Shot = nrow(filter(green, action_type == "Cutting Dunk Shot")))
```

    ##   Jump_Shots Layup_Shots Pullup_Jump_Shots Tip_Layup_Shots
    ## 1        240          59                44              26
    ##   Cutting_Dunk_Shot
    ## 1                22

Here, analysis of our data shows the five most common tendencies of Green on offense. He takes a significant amount of jump shots. His low number of layup shots, pullup jump shots, and other shot attempts near the basket suggest that his role on offense is that of a fourth or fifth man. This makes sense with offensive powerhouses on the team like Durant, Curry, and Thompson. While we cannot ascertain this from the data, it is likely that, due to the gravity of these other players on the Warriors, Green often finds himself open on the floor with a clear jump shot, suggesting a possible reason for his very high number of attempted jumpshots.

### Kevin Durant

![](http://a.espncdn.com/combiner/i?img=/i/headshots/nba/players/full/3202.png&w=350&h=254)

In his 11th year in the League, Kevin Durant is one of the best offensive players of all time. The skills he posses are unprecedented - basketball has never seen a 7 footer that can dribble and move like a guard in the way that Durant can. To add to that, his shooting is not only servicable, it is absolutely **elite**. While the numbers at first glance may not seem otherworldly, his being the focal point on offense a lot of time makes every shot he takes tough. Below, we can look at his shot chart and his top shot tendencies.

![](https://github.com/nishant-m/workout01/blob/master/workout01/images/kevin-durant-shot-chart.png?raw=true)

##### Durant Shot Tendencies

``` r
summarise(durant, 
          Jump_Shots = nrow(filter(durant, action_type == "Jump Shot")),
          Pullup_Jump_Shots = nrow(filter(durant, action_type == "Pullup Jump shot")),
          Fadeaway_Jump_Shot = nrow(filter(durant, action_type == "Fadeaway Jump Shot")),
          Layup_Shots = nrow(filter(durant, action_type == "Layup Shot")),
          Driving_Layup_Shot = nrow(filter(durant, action_type == "Driving Layup Shot")),
          Running_Layup_Shot = nrow(filter(durant, action_type == "Running Layup Shot")))
```

    ##   Jump_Shots Pullup_Jump_Shots Fadeaway_Jump_Shot Layup_Shots
    ## 1        348               114                 48          35
    ##   Driving_Layup_Shot Running_Layup_Shot
    ## 1                 34                 30

Here, analysis of Durant's tendencies only continues to support our ideas that he is an all-time-great. Like Draymond, he takes a very large amount of jump shots, which we can most likely attribute to being the way the offense of Golden State runs as well as a benefit of having so many offensive superstars on one team. The rest of his tendencies, however, are where we can recognize his greatness. With a very large number of pull up jump shots, Durant still manages to shoot 60.65% from 2 pointers and 38.60% from 3 - both incredible numbers for the volume and difficulty of the shots he takes. Considering the numbers of his fadeaway jump shots, driving layup shots, and running layup shots, his tendencies can be observed to be similar to that of a guard, and something that defenders must remain wary of.

### Sources

<http://www.espn.com/nba/player/_/id/6589/draymond-green> <http://www.espn.com/nba/player/_/id/3202/kevin-durant>

# Unified Music Dataset

A curated dataset combining Billboard chart performance, Spotify audio
features, and Genius metadata for 1,792 songs. Song lyrics are not
included because they are copyrighted works. Used throughout "From Vibes
to Variables" for teaching data analysis and research methods.

## Usage

``` r
unified_music
```

## Format

A data frame with 1,792 rows and 35 variables:

- Song:

  Song title

- Artist:

  Artist name

- Average_Rank:

  Average Billboard chart position

- Max_Rank:

  Highest Billboard chart position achieved (1 = top)

- First_Week_on_Board:

  Date of first chart appearance

- First_Rank_on_Board:

  Chart position on first appearance

- Last_Week_on_Board:

  Date of last chart appearance

- Last_Rank_on_Board:

  Chart position on last appearance

- Weeks_on_Board:

  Number of weeks on the Billboard chart

- track_id:

  Spotify track identifier

- track_popularity:

  Spotify popularity score (0-100)

- track_album_id:

  Spotify album identifier

- track_album_name:

  Album title

- track_album_release_date:

  Album release date

- playlist_name:

  Source Spotify playlist

- playlist_id:

  Spotify playlist identifier

- playlist_genre:

  Genre category

- playlist_subgenre:

  Subgenre category

- danceability:

  Spotify danceability score (0-1)

- energy:

  Spotify energy score (0-1)

- key:

  Musical key (0-11, where 0 = C)

- loudness:

  Overall loudness in decibels

- mode:

  Modality (0 = minor, 1 = major)

- speechiness:

  Spotify speechiness score (0-1)

- acousticness:

  Spotify acousticness score (0-1)

- instrumentalness:

  Spotify instrumentalness score (0-1)

- liveness:

  Spotify liveness score (0-1)

- valence:

  Spotify positivity/happiness score (0-1)

- tempo:

  Tempo in beats per minute

- duration_ms:

  Track duration in milliseconds

- tag:

  Content tag or label

- year:

  Release year

- views:

  Genius page view count

- features:

  Featured artists

- id:

  Genius song identifier

## Source

Compiled from Billboard Hot 100 chart data, the Spotify Web API, and the
Genius API. Each source's values remain subject to that source's own
terms (the Billboard terms of use, the Spotify Developer Terms, and the
Genius API terms); the package's MIT license covers the code, not the
third-party data. Song lyrics are not distributed. See the textbook for
full methodology.

## Examples

``` r
data(unified_music)
head(unified_music)
#>                    Song         Artist Average_Rank Max_Rank
#> 1 ...Baby One More Time Britney Spears     37.07767        1
#> 2                  1999         Prince     71.15951        7
#> 3             24K Magic     Bruno Mars     88.48731        2
#> 4           400 Degreez       Juvenile     62.02000        9
#> 5             8 Letters   Why Don't We    103.75000        9
#> 6        99 Luftballons           Nena     73.14286       27
#>   First_Week_on_Board First_Rank_on_Board Last_Week_on_Board Last_Rank_on_Board
#> 1          1999-01-27                   1         2001-01-10                143
#> 2          1982-11-17                  56         2019-12-11                 45
#> 3          2016-12-07                   2         2025-01-29                198
#> 4          1998-11-18                  36         2000-10-11                198
#> 5          2018-09-12                   9         2018-10-03                197
#> 6          1984-03-21                  58         1984-06-20                199
#>   Weeks_on_Board               track_id track_popularity         track_album_id
#> 1            103 3MjUtNVVq3C8Fn0MP3zhXa               75 3WNxdumkSMGMJRhEgK80qx
#> 2            163 2H7PHVdQ3mXqEHXcvclTB0               68 3U1ht9EdWEI9nMvaqdQI67
#> 3            197 6b8Be6ljOzmkOmFslEb23P               78 4PgleR09JVnm3zY1fW3XBA
#> 4            100 5nXQHx4yYKsZqrm7y4bj03               45 6wpqS71CJr3I0dLguYiZdJ
#> 5              4 4zRZAmBQP8vhNPf9i9opXt               77 2qIbHfs93z6eDwGoAdCkXA
#> 6             14 4ZhPLoMzZwewHLLjV1J15c               73 78hVLZZJhaXgrnfXKc6yxF
#>                                 track_album_name track_album_release_date
#> 1 ...Baby One More Time (Digital Deluxe Version)               1999-01-12
#> 2                                           1999               1982-10-27
#> 3                                      24K Magic               2016-11-17
#> 4                                    400 Degreez               1998-01-01
#> 5                                      8 Letters               2018-08-31
#> 6                                           Nena               1983-09-23
#>                                        playlist_name            playlist_id
#> 1                                     90s Dance Hits 50cXvxgMGrvoUeLhkzCyIO
#> 2 80s-90s R&B / New Jack Swing / Funk / Dance / Soul 3X4HmijjKdwwLonCrOOEAZ
#> 3                                      10er Playlist 1kEczIkZH8IgaWT2BiApxZ
#> 4            Dirty South Rap Classics by DJ HOTSAUCE 0tLHH1C4HkWEUCXXSSjbOe
#> 5                                       Hip Pop 2019 3tmx4p5RGlOV1AapXOt1Ze
#> 6                                Permanent Wave CHDB 2foj4ZYVHRGqSd1aMqNPBj
#>   playlist_genre playlist_subgenre danceability energy key loudness mode
#> 1            pop         dance pop        0.759  0.699   0   -5.745    0
#> 2            r&b    new jack swing        0.866  0.730   5   -8.201    1
#> 3            pop        electropop        0.818  0.803   1   -4.282    1
#> 4            rap  southern hip hop        0.856  0.472   3   -9.452    1
#> 5            r&b           hip pop        0.607  0.478   1   -5.702    0
#> 6           rock    permanent wave        0.575  0.555   4   -7.495    1
#>   speechiness acousticness instrumentalness liveness valence   tempo
#> 1      0.0307        0.202         1.31e-04   0.4430   0.907  92.960
#> 2      0.0767        0.137         0.00e+00   0.0843   0.625 118.523
#> 3      0.0797        0.034         0.00e+00   0.1530   0.632 106.970
#> 4      0.0641        0.140         0.00e+00   0.1230   0.642  96.957
#> 5      0.0310        0.649         0.00e+00   0.0928   0.255  88.979
#> 6      0.0453        0.103         1.30e-06   0.1110   0.504  95.361
#>   duration_ms  tag year   views             features      id
#> 1      211067  pop 1998  967940                   {}   78169
#> 2      379267 rock 1982  254603                   {}    2770
#> 3      225983  pop 2016 1573750                   {} 2872960
#> 4      249133  rap 1998   52269                   {}   24993
#> 5      190027  pop 2018  520383 {"Why Don\\\\'t We"} 3888124
#> 6      232467  pop 1983  624448                   {} 1145735
summary(unified_music$Max_Rank)
#>    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
#>    1.00    4.00   15.00   28.94   48.00  180.00 
```

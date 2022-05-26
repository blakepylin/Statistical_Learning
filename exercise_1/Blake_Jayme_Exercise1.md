## Problem 1: Data visualization: flights at ABIA

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/Q1-1.png)

It appears that the best time to fly would be an early morning flight on
Jet Blue, however Jet Blue has the worst arrival delay among evening
flights. In fact, it appears that almost all evening flights have some
sort of delay and that early flights overall are the best choice to
minimize delays.

## Problem 2: Wrangling the Billboard Top 100

### Part A:The Top 10 Most Popular Songs Since 1958

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Performers</th>
<th style="text-align: left;">Songs</th>
<th style="text-align: right;">Total # of Weeks on Billboard</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Imagine Dragons</td>
<td style="text-align: left;">Radioactive</td>
<td style="text-align: right;">87</td>
</tr>
<tr class="even">
<td style="text-align: left;">AWOLNATION</td>
<td style="text-align: left;">Sail</td>
<td style="text-align: right;">79</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Jason Mraz</td>
<td style="text-align: left;">I’m Yours</td>
<td style="text-align: right;">76</td>
</tr>
<tr class="even">
<td style="text-align: left;">The Weeknd</td>
<td style="text-align: left;">Blinding Lights</td>
<td style="text-align: right;">76</td>
</tr>
<tr class="odd">
<td style="text-align: left;">LeAnn Rimes</td>
<td style="text-align: left;">How Do I Live</td>
<td style="text-align: right;">69</td>
</tr>
<tr class="even">
<td style="text-align: left;">LMFAO Featuring Lauren Bennett &amp; GoonRock</td>
<td style="text-align: left;">Party Rock Anthem</td>
<td style="text-align: right;">68</td>
</tr>
<tr class="odd">
<td style="text-align: left;">OneRepublic</td>
<td style="text-align: left;">Counting Stars</td>
<td style="text-align: right;">68</td>
</tr>
<tr class="even">
<td style="text-align: left;">Adele</td>
<td style="text-align: left;">Rolling In The Deep</td>
<td style="text-align: right;">65</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Jewel</td>
<td style="text-align: left;">Foolish Games/You Were Meant For Me</td>
<td style="text-align: right;">65</td>
</tr>
<tr class="even">
<td style="text-align: left;">Carrie Underwood</td>
<td style="text-align: left;">Before He Cheats</td>
<td style="text-align: right;">64</td>
</tr>
</tbody>
</table>

### Part B: Musical Diversity

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/2B-1.png)

This graph shows the number of Hot 100 Entries from years 1958 to 2021.
The slow decline of song diversity from ~1970 to an all time low in the
early aughts is interesting, and you can clearly see the impact of
iTunes and streaming starting around 2005. Maybe the decline in musical
diversity in the 20th century could be attributed to a consolidation of
genres in the zeitgeist.

### Part C: Ten-Week Hit

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/2C-1.png)

## Problem 3: Wrangling the Olympics

### Part A

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Event</th>
<th style="text-align: right;">95th percentile of heights</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Athletics Women’s 1,500 metres</td>
<td style="text-align: right;">172.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Athletics Women’s 10 kilometres Walk</td>
<td style="text-align: right;">170.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Athletics Women’s 10,000 metres</td>
<td style="text-align: right;">167.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">Athletics Women’s 100 metres</td>
<td style="text-align: right;">179.6</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Athletics Women’s 100 metres Hurdles</td>
<td style="text-align: right;">176.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Athletics Women’s 20 kilometres Walk</td>
<td style="text-align: right;">173.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Athletics Women’s 200 metres</td>
<td style="text-align: right;">180.0</td>
</tr>
<tr class="even">
<td style="text-align: left;">Athletics Women’s 3,000 metres</td>
<td style="text-align: right;">170.0</td>
</tr>
<tr class="odd">
<td style="text-align: left;">Athletics Women’s 3,000 metres Steeplechase</td>
<td style="text-align: right;">176.8</td>
</tr>
<tr class="even">
<td style="text-align: left;">Athletics Women’s 4 x 100 metres Relay</td>
<td style="text-align: right;">176.0</td>
</tr>
</tbody>
</table>

The list is showing the 10 rows of the 95th percentile of heights for
female competitors

### Part B

<table>
<thead>
<tr class="header">
<th style="text-align: left;">Event</th>
<th style="text-align: right;">Variability in Height</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;">Rowing Women’s Coxed Fours</td>
<td style="text-align: right;">10.86549</td>
</tr>
</tbody>
</table>

The women’s event with the greatest variability in height was the Rowing
Coxed Fours.

### Part C

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/3C-1.png)

With a strange uptick in age in the men’s event in the 1920’s. It
appears that the average age for men has trended upwards throughout the
years, with the late teen/early twenties being the norm for most of the
20th century and mid-twenties being the norm in the 21st century. A
similar pattern emerges in the women’s event as well, with the mid-late
teens being the norm for most of the 20th century, with a steep uptick
in the late 20th century that put the average female age into the early
20’s. An explanation for these upward trends could be that as healthcare
and training methods improve, people are able to compete at the Olympic
level for longer. Comparatively, it appears that the average age for men
has trended very steadily while the average age for women has a steeper
upward trend.

## Problem 4: K-nearest neighbors

#### For Trim 350

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/unnamed-chunk-1-1.png)

Aftering balacning the biases, we dedcided to use 30 as the optimal k
for trim 350
![](Blake_Jayme_Exercise1_files/figure-markdown_strict/prediction%20plot-1.png)

#### For Trim 65 AMG

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/unnamed-chunk-2-1.png)

Aftering balacning the biases, we dedcided to use 15 as the optimal k
for trim 65 AMG

![](Blake_Jayme_Exercise1_files/figure-markdown_strict/plot%20trim%2065AMG-1.png)

#### Which trim yields a larger optimal value of K?

    ## [1] 416

    ## [1] 292

Trim 350 has 416 observations and Trim 65 AMG has 292, Trim 350 has a
larger data size so it can accommodate a larger K to get a smoother line
without having too much bias in our prediction.

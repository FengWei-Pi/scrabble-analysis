# scrabble-analysis

A small project examining the difference in win percentages between the player who goes first and second in Scrabble.

Data was scraped from [annotated Scrabble games on cross-tables.com](https://www.cross-tables.com/annolistself.php) using Python in a Jupyter Notebook environment hosted on Google Colab. The code is available in full at [scrabble_analysis.ipynb](https://github.com/FengWei-Pi/scrabble-analysis/blob/main/scrabble_analysis.ipynb).

## Results
In 998 randomly selected games, 548 were won by the player going first, 450 by the player going second, and 0 were drawn. This corresponds to win percentages of 55% (95% CI: 52%, 58%) and 45% (95% CI: 42%, 48%). McNemar's test revealed this difference to be statistically significant $(\chi^2(1)=9.43, p<.005)$.

The player going first, then, holds a sizeable advantage.

<img src="https://github.com/user-attachments/assets/4bcddd45-2307-4e38-8b3d-277bcd372b2a" width="380" height="240">

## Considerations
- Players who win their games may be more likely to upload their games, exaggerating the difference in win percent if there is one. The majority of uploads are also tournament games with higher skilled players and may not be representative of the general population.
- Games that could not be parsed by the code were skipped. These games may have had shared characteristics, though only two were excluded in this way and are unlikely to affect the results.

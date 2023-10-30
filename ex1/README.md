test

```
install.packages("dplyr")
install.packages("ggplot2")
library(dplyr)
library(ggplot2)
install.packages("tidyverse")
library(tidyverse)

ggplot(data = fawar, aes(x = Year, y = DollarWAR, color = Pos)) +
  geom_point() +
  scale_x_continuous(breaks = seq(2010,2023,by = 1)) +
  scale_y_continuous(breaks = seq(5.5,14,by = .5)) +
  labs(x = 'Year', y = 'FA Spending on WAR (in millions of $)',
        title = 'Separated Free Agent Value of Batters and Pitchers, 2010-2023',
        color = 'Position') +
  geom_smooth(method = 'lm', se = FALSE)
```

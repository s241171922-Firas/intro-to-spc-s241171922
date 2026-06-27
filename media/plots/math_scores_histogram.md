
# Histogram of Math Scores
library(tidyverse)
library(plotly)
library(htmlwidgets)

p <- bigclass %>%
  ggplot(aes(x = Math)) +
  geom_histogram(binwidth = 50, fill = "#0072B2", color = "black") +
  labs(
    title = "Distribution of Math Scores",
    x = "Math Scores",
    y = "Frequency"
  ) +
  theme_minimal() +
  theme(
    axis.title = element_text(size = 18),
    axis.text = element_text(size = 14),
    plot.background = element_rect(fill = "white", colour = "white"),
    panel.background = element_rect(fill = "white", colour = "white")
  )

html_path <- "media/plots/math_scores_histogram.html"
saveWidget(ggplotly(p), file = html_path, selfcontained = TRUE)


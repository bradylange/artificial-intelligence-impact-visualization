# Developer: Brady Lange
# Date: 04/21/2019
# Description: Visual of the 2017 impacts of artificial intelligence on 
# the economy. Survey data obtained from business executives in 2017.
# Source: www.bcg.com/Images/Reshaping%20Business%20with%20Artificial
# %20Intelligence_tcm9-177882.pdf

# Set-up workspace
graphics.off()
rm(list = ls())

# Load libraries 
library(tidyverse)

# Create tibble of proportion of economic benefits to businesses 
# 16 = 16% had no benefits, 84 = 84% had benefits
ai <- tibble(economic_benefit = c(16, 84))

# Visualize artificial intelligence impacts on the economy in 2017
ggplot(ai, aes(x = "", y = economic_benefit, fill = factor(economic_benefit))) +
  geom_bar(stat = "identity") + 
  coord_polar(theta = "y") + 
  scale_x_discrete("") + 
  scale_y_continuous("") + 
  scale_fill_brewer("Economic Benefit", labels = c("No Benefit", "Benefit"),
                    palette = "Paired") + 
  ggtitle("How Artificial Intelligence Benefits Economics") +
  geom_text(aes(label = str_c(factor(economic_benefit), "%")), vjust = c(-4, 7),
            hjust = c(3.25, -1.5), size = 6, color = "black") +
  geom_text(x = 0, y = 0, label = "Source: Ransbotham et al.", 
            vjust = 11.85, size = 3, inherit.aes = F) +
  theme(plot.title = element_text(face = "bold", size = 15, vjust = -5,
                                  hjust = 0.25),
        legend.position = c(1.1, 0.1), 
        panel.background = element_blank(),
        axis.ticks.y = element_blank(),
        axis.text = element_blank())

# Save the pie chart to folder
ggsave("./plots/ai_economic_benefits.png", scale = 1, plot = last_plot())

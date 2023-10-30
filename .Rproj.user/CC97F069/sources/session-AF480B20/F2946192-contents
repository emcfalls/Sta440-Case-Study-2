# Load required libraries
library(dplyr)
library(tidyr)

# Read the data from the original CSV
data <- read.csv("data/data_2022_2023.csv")

data_final <- data %>%
  mutate(Date = sapply(strsplit(as.character(Date), "-"), tail, 1),
         Date = trimws(Date),                 # Trim leading and trailing spaces
         Date = sub(" *$", "", Date),         # Remove spaces at the end
         Date = gsub(" ", "-", Date))         # Replace remaining spaces with "-"

# Write the final data back to a new CSV file
write.csv(data_final, "cleaned data/data_2022_2023_cleaned.csv", row.names = FALSE)

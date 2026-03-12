# 📊 Step-by-Step Guide: Visualizing the GDELT Representation Gap

This guide breaks down the visualization module of the **GDELT Bias Investigator**. The goal of this script is to expose geographic "Data Deserts" by comparing physical population reality against digital news narrative.

## Step 1: Defining the Data Arrays
First, we import our libraries and define the core disparity. Instead of raw counts, we use **global percentages** to create a direct 1:1 comparison.

```python
import matplotlib.pyplot as plt
import numpy as np

# Physical Reality: % of World Population
# Digital Narrative: % of Global News Volume in GDELT
labels = ['India', 'Israel']
population_share = [17.5, 0.1]  
news_visibility = [1.5, 20.0]

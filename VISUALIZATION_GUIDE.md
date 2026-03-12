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

## Step 2: Setting up the Side-by-Side Plot
To visually prove algorithmic bias, a single bar isn't enough. We must map the expected baseline (population) directly next to the actual output (news volume). We use `numpy` to offset the bars side-by-side.

```python
x = np.arange(len(labels))
width = 0.35

fig, ax = plt.subplots(figsize=(10, 6))

# Mapping the variables to the plot
rects1 = ax.bar(x - width/2, population_share, width, 
                label='Physical Reality (% of World Population)', color='#3498db', alpha=0.8)
rects2 = ax.bar(x + width/2, news_visibility, width, 
                label='Digital Narrative (% of News Volume)', color='#e67e22', alpha=0.8)
ax.set_title('The Representation Gap: Physical World vs. Digital News', fontsize=14, fontweight='bold', pad=20)
ax.set_ylabel('Global Percentage (%)', fontsize=12)
ax.set_xticks(x)
ax.set_xticklabels(labels, fontsize=12, fontweight='bold')
ax.legend()

# Formatting labels to one decimal place
ax.bar_label(rects1, padding=3, fmt='%.1f%%')
ax.bar_label(rects2, padding=3, fmt='%.1f%%')
plt.grid(axis='y', linestyle='--', alpha=0.4)
plt.tight_layout()
plt.savefig('global_representation_gap.png')
plt.show()
```

![Representation Gap Chart](representation_gap.png)

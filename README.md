## 🔍 Data Bias Investigator: GDELT Geographic Skew Analysis
* Author: Sultana | BCA Researcher
* Status: Active Research Project (Mar 2026)
* Focus: Algorithmic Fairness & Data Integrity
# 👤 About the Author
I am Zinath Sultana, a 4th-semester Bachelor of Computer Applications (BCA) student and an aspiring AI/ML researcher. My work focuses on bridging the gap between social media analytics and ethical AI research.
* Research Interests: Algorithmic Fairness, Natural Language Processing (NLP), and Data Integrity.
* Certifications: IBM AI Fundamentals & Generalist Certified.
# Mission:
To develop reproducible and scalable research methodologies that identify and mitigate bias in global datasets.
# 📖 Project Overview
This investigator analyzes the GDELT (Global Database of Events, Language, and Tone) to identify geographic representation skews. By examining millions of broadcast, print, and web news entries, this project quantifies how specific regions are over-represented while others remain "data deserts."
# 🔬 Research Methodology
* Data Ingestion: Streaming GDELT 2.0 event logs.
* Memory Optimization: Implementation of Pandas chunking to process high-volume datasets (GBs) on resource-constrained hardware.
* Statistical Analysis: Calculating representation ratios to detect an identified 0.09% skew in specific global news categories.
* Quantification: Tracking data density across 200+ countries to map "News Bias" hotspots.
# 💻 Technical Highlights
* Vectorized Processing: Utilizing NumPy for fast numerical operations on event coordinates.
* Scalable Architecture: Script-based approach designed for easy integration into larger ML pipelines.
* Memory Efficiency: Reduced RAM overhead by 60% using categorical data types and chunk-based loading.
# 🛠️ Reproducibility (Step-by-Step)
Follow these commands in your terminal to set up the environment and run the analysis:
# 1. Clone the repository
git clone [https://github.com/ZinathBCAResearch078/Google-Internship-Research-Project.git](https://github.com/ZinathBCAResearch078/Google-Internship-Research-Project.git)

# 2. Navigate to directory
cd Google-Internship-Research-Project

# 3. Install dependencies
pip install -r requirements.txt

# 4. Execute the Investigator
python bias_detection.py

# 📋 Tech Stack
* Language: Python 3.10+
* Libraries: Pandas (Data Wrangling), NumPy (Numerical Analysis)
* Dataset: GDELT Project (Global Event Database)

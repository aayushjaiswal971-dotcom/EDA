# EDA
Method 1: Open and Run in Google Colab (Recommended)
This is the easiest method.
Step 1: Open Google Colab
Go to
https://colab.research.google.com
Step 2: Upload the Notebook
Click File → Upload Notebook
Upload EDA.ipynb
OR
Click Upload
Drag and drop the file.
Step 3: Mount Google Drive
One of the cells in your notebook contains:
from google.colab import drive
drive.mount('/content/gdrive')
Run this cell by clicking ▶ Run.
It will show a Google authentication link.
Click the link
Sign in
Copy the code
Paste it in Colab
Step 4: Upload Dataset to Google Drive
Your code uses this path:
'/content/gdrive/My Drive/CVENG_8160/data/delay_bottleneck.csv'
So you must create this folder in your Google Drive:
My Drive
 └── CVENG_8160
      └── data
           └── delay_bottleneck.csv
Upload the delay_bottleneck.csv dataset there.
Step 5: Run All Cells
Click:
Runtime → Run All
or run cells one by one using ▶ button.
Method 2: Run on Your Computer (Jupyter Notebook)
Step 1: Install Python
Install Anaconda (recommended):
https://www.anaconda.com/download
Step 2: Install Required Libraries
Open Anaconda Prompt / Terminal and run:
pip install pandas numpy matplotlib jupyter
Step 3: Start Jupyter Notebook
Run:
jupyter notebook
Your browser will open automatically.
Step 4: Open the File
Navigate to the folder where EDA.ipynb is saved
Click EDA.ipynb
Step 5: Run the Notebook
Click:
Cell → Run All
or press
Shift + Enter
to run each cell.
Important Fix (If Running Locally)
Remove this part because it only works in Colab:
from google.colab import drive
drive.mount('/content/gdrive')
Replace the dataset path with a local path like:
path = "delay_bottleneck.csv"
Example Code Structure in Your Notebook
Your notebook contains code like:
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
Then it creates a class:
class dataproc:
Then loads dataset:
path = '/content/gdrive/My Drive/CVENG_8160/data/delay_bottleneck.csv'
dp = dataproc(path)


# Floor Plan Segmentation and Analysis model


This code snippet exemplifies a comprehensive floor plan segmentation process. The code initializes the model, processes a test image from the dataset and showcases the original image alongside the accurately segmented rooms and icons present in the input floor plan image. 

# Prerequisites
 
lmdb: Efficient key-value database management system.

matplotlib: Popular plotting library for visualizations.

torch: Core library for deep learning.

floortrans: Floor plan analysis and segmentation.

mpl_toolkits: Additional tools for Matplotlib plots.

scikit-image: Image processing and manipulation library.

numpy: Fundamental library for numerical computing.

torchvision: Computer vision utilities for PyTorch.

EasyOCR: Optical character recognition (OCR) library.

# Installation

1. Clone the repository:
```
git clone https://github.com/sayantanmaji10/FloorPlanSolutions.git
```

2. Mount Google Drive in Google Colab:
```
from google.colab import drive
drive.mount('/content/drive')
```

3. Navigate to the project directory where the dataset is present 

4. List the contents of the directory:
```
ls

```

5. Extract the data from the zip file:
```
from zipfile import ZipFile

file = "/content/drive/MyDrive/dt.zip"
with ZipFile(file, 'r') as zip:
    zip.printdir()
    print('Extracting all the files now...')
    zip.extractall()

``` 
Replace dt with the actual dataset 

# Usage

1. Import all the necessary libraries(As already mentioned)

2. Load and preprocess the data
```
data_folder = '/content/path/'
data_file = 'test.txt'
normal_set = FloorplanSVG(data_folder, data_file, format='txt', original_size=True)
data_loader = DataLoader(normal_set, batch_size=1, num_workers=0)
data_iter = iter(data_loader)

```
Replace "/content/path/" with the actual path 

3. Set up and load the model

4. Make predictions

5. Visualize the results 

# Results

It calculates and visualizes the precise percentage distribution of each room class within the segmentation map, offering valuable insights. Also the code leverages the EasyOCR library to perform accurate optical character recognition on an image file, enabling the extraction of textual information for further analysis. Overall, this code demonstrates a professional approach to floor plan segmentation, visualization, and information extraction, contributing to improved understanding and interpretation of floor plan data.






# Plant-Seedling-Classification
In recent times, the field of agriculture has been in urgent need of modernizing, since the amount of manual work people need to put in to check if plants are growing correctly is still highly extensive. Despite several advances in agricultural technology, people working in the agricultural industry still need to have the ability to sort and recognize different plants and weeds, which takes a lot of time and effort in the long term. The potential is ripe for this trillion-dollar industry to be greatly impacted by technological innovations that cut down on the requirement for manual labor, and this is where Artificial Intelligence can actually benefit the workers in this field, as the time and energy required to identify plant seedlings will be greatly shortened by the use of AI and Deep Learning. The ability to do so far more efficiently and even more effectively than experienced manual labor, could lead to better crop yields, the freeing up of human inolvement for higher-order agricultural decision making, and in the long term will result in more sustainable environmental practices in agriculture as well.

## Objective
The aim of this project is to Build a Convolutional Neural Netowrk to classify plant seedlings into their respective categories.

## Data Dictionary
The Aarhus University Signal Processing group, in collaboration with the University of Southern Denmark, has recently released a dataset containing images of unique plants belonging to 12 different species.

The dataset can be download from Olympus.

The data file names are:

images.npy
Labels.csv
Due to the large volume of data, the images were converted to the images.npy file and the labels are also put into Labels.csv, so that you can work on the data/project seamlessly without having to worry about the high data volume.

The goal of the project is to create a classifier capable of determining a plant's species from an image.

### List of Species
* Black-grass
* Charlock
* Cleavers
* Common Chickweed
* Common Wheat
* Fat Hen
* Loose Silky-bent
* Maize
* Scentless Mayweed
* Shepherds Purse
* Small-flowered Cranesbill
* Sugar beet

## Results
Three different models were trained and evaluated to classify plant species from image
| Model                   | Training Accuracy | Validation Accuracy |
| ----------------------- | ----------------- | ------------------- |
| Base Model              | 79.71%            | 59.90%              |
| ReduceLRonPlateau Model | 86.65%            | 74.75%              |
| Data Augmentation Model | 89.89%        | 87.46%          |

The Data Augmentation model showed the best performance, significantly improving generalization and reducing overfitting.

However, the model frequently misclassified Black-grass as Loose Silky-bent, indicating that these two classes are visually similar and difficult to distinguish with the current dataset size and quality.

To further improve accuracy, particularly for confusing classes, a partnership with companies in the agricultural or botanical sector is recommended. Such collaborations could facilitate access to a larger and more diverse labeled dataset, enabling more robust model training and better classification performance.

## 📦 Key Libraries Used

* **TensorFlow / Keras** – Model building, training, and data augmentation
* **OpenCV (`cv2`)** – Image processing and visualization
* **NumPy & Pandas** – Numerical operations and data handling
* **Matplotlib & Seaborn** – Data visualization and plotting
* **Scikit-learn (`sklearn`)** – Data splitting and evaluation metrics

Here's a complete **"Installation & Environment Setup"** section you can add to your **README**, covering both **Google Colab** and **Visual Studio Code (VS Code)**:

---

### ⚙️ Installation & Environment Setup

#### 🟢 Option 1: Using Google Colab (Recommended for Beginners)

No installation required. All key libraries (TensorFlow, OpenCV, NumPy, etc.) come pre-installed.

To run the notebook:

1. Upload your notebook to [Google Colab](https://colab.research.google.com/)
2. Make sure your runtime is set to **GPU**:

   * Go to `Runtime` > `Change runtime type` > Select **GPU**
3. Run all cells sequentially

---

#### 💻 Option 2: Using Visual Studio Code (Local Setup)

1. **Install Python** (preferably Python 3.8 or later) from [python.org](https://www.python.org/)

2. **Create a virtual environment** (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required libraries**:

   ```bash
   pip install tensorflow opencv-python numpy pandas matplotlib seaborn scikit-learn
   ```

4. **Install Jupyter Notebook extension for VS Code**:

   * Go to Extensions in VS Code (`Ctrl+Shift+X`)
   * Search for and install **"Jupyter"**

5. **Launch and run the notebook**:

   * Open `.ipynb` file in VS Code and run cells

Great! Based on your provided pip install command, here’s the content for a **`requirements.txt`** file you can include in your GitHub repo:

---

### 📄 `requirements.txt`

```
tensorflow==2.15.0
scikit-learn==1.2.2
seaborn==0.13.1
matplotlib==3.7.1
numpy==1.25.2
pandas==1.5.3
opencv-python==4.8.0.76
```

---

### ✅ How to Use:

To install the dependencies locally using `requirements.txt`, run:

```bash
pip install -r requirements.txt
```

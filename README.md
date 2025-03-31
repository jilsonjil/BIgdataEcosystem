# Population Prediction using Hadoop and Spark

## Overview
This project aims to predict population growth using two different big data frameworks:
- **Hadoop**: Uses MapReduce and Pandas for data processing.
- **Spark**: Uses PySpark for distributed data processing and machine learning.

The dataset used contains population data from different years for various countries.

## Project Structure
```
/Population_Prediction
├── Population_Prediction_hadoop.ipynb   # Hadoop-based approach
├── Population_prediction_spark.ipynb   # Spark-based approach
├── README.md                            # Project documentation
└── data/world_population.csv           # Dataset (ensure to add it)
```

## Prerequisites
Ensure you have the following installed:
- Google Colab (No local installation needed)
- A Google Drive account to store data

### Hadoop Notebook Requirements
Run the following in Colab:
```
!pip install mrjob scikit-learn matplotlib pandas
!apt-get install openjdk-8-jdk -qq > /dev/null
```

### Spark Notebook Requirements
Run the following in Colab:
```
!pip install pyspark numpy pandas matplotlib
```

## Usage in Google Colab
### Running the Hadoop-based Notebook
1. Open `Population_Prediction_hadoop.ipynb` in **Google Colab**.
2. Mount Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Ensure the dataset (`world_population.csv`) is stored in Drive and update the file path.
4. Run the notebook to process data and analyze population trends.

### Running the Spark-based Notebook
1. Open `Population_prediction_spark.ipynb` in **Google Colab**.
2. Mount Google Drive:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Ensure the dataset (`world_population.csv`) is stored in Drive and update the file path.
4. Run the notebook to perform distributed data processing and machine learning.

## Key Differences
| Feature      | Hadoop Approach | Spark Approach |
|-------------|----------------|---------------|
| **Data Handling** | Pandas (`pd.read_csv`) | Spark DataFrame (`spark.read.csv`) |
| **Processing** | MapReduce & Pandas | PySpark transformations |
| **ML Model** | Polynomial Regression | Polynomial Regression |
| **Storage** | Google Drive | Google Drive & SQLite |
| **Speed** | Slower due to batch processing | Faster due to in-memory computing |
| **Scalability** | Limited | Highly Scalable |
| **Ease of Use** | Requires MapReduce knowledge | Easier with PySpark APIs |

### Summary
- **Hadoop** is suitable for traditional batch processing but can be slower.
- **Spark** provides faster, in-memory data processing and is more scalable.
- If machine learning is required, **Spark** is the better choice due to its built-in ML capabilities.


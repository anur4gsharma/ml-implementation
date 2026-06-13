# California Housing Prices Implementation

This project implements a data processing pipeline for the California Housing dataset, following typical machine learning practices.

## Process Overview

1.  **Data Acquisition**:
    *   The project uses `urllib.request` to download the `housing.tgz` tarball from a remote repository.
    *   The `tarfile` library is used to extract the `housing.csv` file into a local `datasets` directory.
    *   `pandas` is used to load the CSV data into a DataFrame for manipulation.

2.  **Data Exploration**:
    *   The dataset contains geographical information (longitude/latitude), housing characteristics (age, rooms, bedrooms), and economic indicators (median income, house value).
    *   Histograms are generated using `matplotlib` to visualize the distribution of each numerical attribute, helping identify data quirks like capped values or skewed distributions.

3.  **Data Splitting**:
    *   A manual implementation of data splitting is used to create a test set.
    *   `numpy.random.default_rng()` is utilized to ensure reproducible shuffling of indices before partitioning the data into training (80%) and testing (20%) sets.

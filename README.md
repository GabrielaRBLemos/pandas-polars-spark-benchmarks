# Performance Benchmarking: Pandas vs Polars vs PySpark

This repository contains a Jupyter notebook that benchmarks the performance of three popular Python data-processing libraries:

- **Pandas**
- **Polars**
- **PySpark**

The comparison focuses on **data loading speed**, **memory usage**, and **group-by aggregation performance** across different data sizes and file formats.
The Iris dataset used in this benchmark was sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/53/iris) in CSV format, with the Parquet version obtained from [Agents For Data](https://www.agentsfordata.com/parquet/sample).

---

## 📌 Objectives

The notebook aims to answer the following questions:

- How fast do Pandas, Polars, and PySpark load small datasets?
- Does file format (**CSV vs Parquet**) significantly impact load time and memory usage?
- How do these libraries scale when performing `groupby` aggregations on increasingly large datasets?

> ⚠️ **Notes:** Due to environment constraints, PySpark CSV and Parquet reads are performed via intermediate Pandas DataFrames instead of native Spark readers.
> PySpark memory usage is **not included**, as Spark manages memory across JVM executors, making per-DataFrame measurements unreliable without cluster-level metrics.
> Results are hardware- and environment-dependent and should be interpreted comparatively rather than absolutely.

---
name: spark-optimize
description: Optimize Apache Spark and PySpark jobs, queries, joins, partitioning, and Delta Lake writes.
---

# Spark Optimization Rules
When writing, reviewing, or refactoring Spark/PySpark code, apply these rules:
1. **Eliminate Python UDFs:** Replace `@udf` with native `pyspark.sql.functions` or Pandas vectorized UDFs.
2. **Prevent Shuffle Skew:** Use `broadcast()` for dimension tables under ~100 MB, or enable Adaptive Query Execution (`spark.sql.adaptive.enabled=true`).
3. **Prune Early:** Filter rows and select required columns before joins and aggregations.
4. **Safe Driver Memory:** Never call `.collect()` or `.toPandas()` on unaggregated DataFrames.
5. **Delta Writes:** Include explicit partition predicates in `MERGE INTO` statements to avoid full-table scans.

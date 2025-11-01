# Learn Polars - Complete Tutorial Collection

A comprehensive, hands-on collection of Jupyter notebooks to master Polars, the blazingly fast DataFrame library for Python.

---

## 🚀 Quick Start

**New to Polars?** Start here:

1. Read **[QUICK_START.md](QUICK_START.md)** for a fast-track guide
2. Follow **[LEARNING_PATH.md](LEARNING_PATH.md)** for the complete structured curriculum
3. Open `polars-complete-guide.ipynb` and start learning!

---

## 📚 What's Inside

This repository contains **23 comprehensive Jupyter notebooks** covering everything from basics to advanced performance optimization.

### 🎯 Core Curriculum (Start Here)

| # | Notebook | Focus | Time | Priority |
|---|----------|-------|------|----------|
| 0 | `polars-complete-guide.ipynb` | Complete overview | 2h | ⭐⭐⭐ |
| 1 | `02_lazy_evaluation_optimization.ipynb` | Lazy evaluation & optimization | 2h | ⭐⭐⭐ |
| 2 | `03_expressions_selectors.ipynb` | Expression system | 2h | ⭐⭐⭐ |

### 📊 Data Operations

| # | Notebook | What You'll Learn | Time |
|---|----------|-------------------|------|
| 3 | `13_data_types_schemas.ipynb` | Type system, schemas | 1h |
| 4 | `14_missing_duplicate_handling.ipynb` | Handling nulls & duplicates | 1.5h |
| 5 | `06_string_operations.ipynb` | String manipulation | 1.5h |
| 6 | `07_datetime_operations.ipynb` | Date/time handling | 1.5h |

### 🔄 Transformations

| # | Notebook | What You'll Learn | Time |
|---|----------|-------------------|------|
| 7 | `01_joins_comprehensive.ipynb` | All 7 join types | 2h |
| 8 | `04_groupby_aggregations.ipynb` | GroupBy & aggregations | 1.5h |
| 9 | `05_window_functions.ipynb` | Window functions & ranking | 2h |
| 10 | `08_pivoting_reshaping.ipynb` | Pivot, melt, reshape | 1.5h |
| 11 | `12_nested_data_structures.ipynb` | Lists, structs, nested data | 2h |

### 📈 Time Series & Applications

| # | Notebook | What You'll Learn | Time |
|---|----------|-------------------|------|
| 12 | `09_timeseries_groupby_dynamic.ipynb` | Time-based grouping | 2h |
| 13 | `09_yfinance_stock_analysis.ipynb` | Stock analysis example | 1.5h |
| 14 | `10_financial_timeseries_yfinance.ipynb` | Financial time series | 2h |

### 🚀 Advanced Topics

| # | Notebook | What You'll Learn | Time |
|---|----------|-------------------|------|
| 15 | `11_advanced_io_cloud_storage.ipynb` | Cloud I/O, partitioning | 2h |
| 16 | `16_interoperability.ipynb` | Pandas, NumPy, DuckDB integration | 2h |
| 17 | `18_data_quality_validation.ipynb` | Data validation & quality | 1.5h |
| 18 | `05_large_dataset_comparison.ipynb` | Performance benchmarks | 1.5h |
| 19 | `19_performance_debugging.ipynb` | Profiling & optimization | 2h |

### 🎨 Optional Workshops

| # | Notebook | What You'll Learn | Time |
|---|----------|-------------------|------|
| 20 | `20_udfs_custom_functions.ipynb` | UDFs, map_elements, performance | 2h |
| 21 | `21_sql_interface.ipynb` | SQL syntax with Polars | 1.5h |
| 22 | `22_visualization.ipynb` | Matplotlib & Plotly charts | 1.5h |

**Total: ~40 hours** of comprehensive training material (35h core + 5h workshops)

---

## 🎓 Learning Paths

### Path 1: "I'm New to Polars" (4 weeks)
Follow **[LEARNING_PATH.md](LEARNING_PATH.md)** exactly - all 5 phases sequentially.

### Path 2: "I Know Pandas" (2 weeks)
1. `polars-complete-guide.ipynb` - See differences
2. `02_lazy_evaluation_optimization.ipynb` - Learn lazy execution
3. `03_expressions_selectors.ipynb` - Master expressions
4. `16_interoperability.ipynb` - Pandas ↔ Polars conversion
5. `19_performance_debugging.ipynb` - Optimize queries
6. Pick notebooks for your specific needs

### Path 3: "Quick Crash Course" (3 hours)
See **[QUICK_START.md](QUICK_START.md)** → 3-Hour Crash Course section

### Path 4: "Performance Focus" (1 week)
1. `02_lazy_evaluation_optimization.ipynb`
2. `19_performance_debugging.ipynb`
3. `11_advanced_io_cloud_storage.ipynb`
4. `05_large_dataset_comparison.ipynb`

### Path 5: "Time Series Analysis" (1 week)
1. `polars-complete-guide.ipynb`
2. `07_datetime_operations.ipynb`
3. `09_timeseries_groupby_dynamic.ipynb`
4. `05_window_functions.ipynb`
5. `09_yfinance_stock_analysis.ipynb`

---

## 🎯 By Use Case

### Data Analysis
→ Start: `polars-complete-guide.ipynb`
→ Then: `01_joins`, `04_groupby`, `05_window_functions`

### ETL Pipelines
→ Start: `02_lazy_evaluation`
→ Then: `14_missing_duplicate`, `18_data_quality`, `11_advanced_io`

### Time Series
→ Start: `07_datetime_operations`
→ Then: `09_timeseries_groupby_dynamic`, `05_window_functions`

### Performance Optimization
→ Start: `02_lazy_evaluation`
→ Then: `19_performance_debugging`, `05_large_dataset_comparison`

### Data Cleaning
→ Start: `14_missing_duplicate_handling`
→ Then: `06_string_operations`, `18_data_quality_validation`

---

## 🚦 Getting Started

### Prerequisites
```bash
# Install Polars
pip install polars

# For specific notebooks, install optional dependencies:
pip install 'polars[pandas,numpy,pyarrow]'  # Interoperability
pip install yfinance                         # Financial examples
pip install jupyterlab                       # Notebook environment
```

### Choose Your Starting Point

**Complete Beginner?**
```bash
jupyter notebook polars-complete-guide.ipynb
```

**Want Structured Learning?**
```bash
# Read the guides first
cat LEARNING_PATH.md
cat QUICK_START.md

# Then start Phase 1
```

**Need Something Specific?**
Use the "By Use Case" section above to find the right notebook.

---

## 📊 Progress Tracker

Track your progress:

```
Foundations
[ ] polars-complete-guide.ipynb
[ ] 02_lazy_evaluation_optimization.ipynb
[ ] 03_expressions_selectors.ipynb

Core Operations
[ ] 13_data_types_schemas.ipynb
[ ] 14_missing_duplicate_handling.ipynb
[ ] 06_string_operations.ipynb
[ ] 07_datetime_operations.ipynb

Transformations
[ ] 01_joins_comprehensive.ipynb
[ ] 04_groupby_aggregations.ipynb
[ ] 05_window_functions.ipynb
[ ] 08_pivoting_reshaping.ipynb
[ ] 12_nested_data_structures.ipynb

Time Series
[ ] 09_timeseries_groupby_dynamic.ipynb
[ ] 09_yfinance_stock_analysis.ipynb
[ ] 10_financial_timeseries_yfinance.ipynb

Advanced
[ ] 11_advanced_io_cloud_storage.ipynb
[ ] 16_interoperability.ipynb
[ ] 18_data_quality_validation.ipynb
[ ] 05_large_dataset_comparison.ipynb
[ ] 19_performance_debugging.ipynb

Optional Workshops (Learn as needed)
[ ] 20_udfs_custom_functions.ipynb
[ ] 21_sql_interface.ipynb
[ ] 22_visualization.ipynb
```

---

**Happy Learning! 🎉**

*Master the fastest DataFrame library for Python*

---

*Last Updated: 2025 | Polars Learning Collection*

# Polars Learning - Quick Start Guide

## 🎯 Start Here

If you're new to Polars, follow this exact order:

### Week 1: Foundations (Critical - Don't Skip!)

```
Day 1-2: polars-complete-guide.ipynb
         └─ Get familiar with basic Polars concepts

Day 3-4: 02_lazy_evaluation_optimization.ipynb ⭐
         └─ Understand lazy vs eager (CRITICAL!)

Day 5-6: 03_expressions_selectors.ipynb ⭐
         └─ Master the expression system (CRITICAL!)
```

### Week 2: Data Operations

```
Day 1: 13_data_types_schemas.ipynb
       └─ Learn data types

Day 2: 14_missing_duplicate_handling.ipynb
       └─ Clean messy data

Day 3: 06_string_operations.ipynb
       └─ Work with text

Day 4: 07_datetime_operations.ipynb
       └─ Handle dates/times

Day 5-7: Practice and review
```

### Week 3: Transformations

```
Day 1-2: 01_joins_comprehensive.ipynb
         └─ Combine datasets

Day 3: 04_groupby_aggregations.ipynb
       └─ Summarize data

Day 4: 05_window_functions.ipynb
       └─ Advanced analytics

Day 5: 08_pivoting_reshaping.ipynb
       └─ Reshape data

Day 6-7: Practice and review
```

### Week 4: Advanced Topics

```
Day 1-2: 09_timeseries_groupby_dynamic.ipynb
         └─ Time series analysis

Day 3: 16_interoperability.ipynb
       └─ Integration with other tools

Day 4: 18_data_quality_validation.ipynb
       └─ Data quality checks

Day 5: 19_performance_debugging.ipynb ⭐
       └─ Optimize performance

Day 6-7: Build a project!
```

---

## 📚 Learning by Use Case

### "I need to analyze sales data"
1. `polars-complete-guide.ipynb` - Learn basics
2. `01_joins_comprehensive.ipynb` - Join sales with customer data
3. `04_groupby_aggregations.ipynb` - Calculate metrics by region/product
4. `07_datetime_operations.ipynb` - Analyze trends over time
5. `09_timeseries_groupby_dynamic.ipynb` - Time-based grouping

### "I'm coming from Pandas"
1. `polars-complete-guide.ipynb` - See syntax differences
2. `02_lazy_evaluation_optimization.ipynb` - Learn lazy evaluation (NEW!)
3. `03_expressions_selectors.ipynb` - Different from Pandas!
4. `16_interoperability.ipynb` - Convert between Pandas/Polars
5. `05_large_dataset_comparison.ipynb` - See performance gains

### "My queries are too slow"
1. `02_lazy_evaluation_optimization.ipynb` - Use lazy evaluation
2. `19_performance_debugging.ipynb` - Profile and optimize
3. `11_advanced_io_cloud_storage.ipynb` - Efficient I/O

### "I'm working with time series"
1. `07_datetime_operations.ipynb` - Date/time basics
2. `09_timeseries_groupby_dynamic.ipynb` - Time-based grouping
3. `09_yfinance_stock_analysis.ipynb` - Real example
4. `05_window_functions.ipynb` - Rolling calculations

### "I need to clean messy data"
1. `14_missing_duplicate_handling.ipynb` - Handle nulls/duplicates
2. `18_data_quality_validation.ipynb` - Validation checks
3. `06_string_operations.ipynb` - Clean text data

---

## 🎓 3-Hour Crash Course

**Goal:** Get productive with Polars quickly

**Hour 1: Basics (30 min each)**
- `polars-complete-guide.ipynb` - Sections: DataFrame creation, basic operations
- `03_expressions_selectors.ipynb` - Focus on: `pl.col()`, basic expressions

**Hour 2: Essential Operations**
- `01_joins_comprehensive.ipynb` - Focus on: inner, left, semi, anti joins
- `04_groupby_aggregations.ipynb` - Focus on: basic groupby and agg

**Hour 3: Performance**
- `02_lazy_evaluation_optimization.ipynb` - Focus on: `.lazy()`, `.collect()`, query plans
- Start using lazy mode in your own code!

**Bonus (Optional - based on your needs):**
- `21_sql_interface.ipynb` - If you prefer SQL syntax
- `22_visualization.ipynb` - To visualize your results
- `20_udfs_custom_functions.ipynb` - For custom logic (use sparingly!)

**Result:** You can now:
- Create and manipulate DataFrames
- Join and aggregate data
- Write efficient lazy queries
- (Optional) Use SQL syntax or create visualizations

---

## 🚀 One Notebook Per Concept

| Need to... | Notebook | Time |
|-----------|----------|------|
| **Get started** | polars-complete-guide.ipynb | 2h |
| **Understand lazy evaluation** ⭐ | 02_lazy_evaluation_optimization.ipynb | 2h |
| **Write expressions** ⭐ | 03_expressions_selectors.ipynb | 2h |
| **Join tables** | 01_joins_comprehensive.ipynb | 2h |
| **Aggregate data** | 04_groupby_aggregations.ipynb | 1.5h |
| **Use window functions** | 05_window_functions.ipynb | 2h |
| **Work with strings** | 06_string_operations.ipynb | 1.5h |
| **Handle dates** | 07_datetime_operations.ipynb | 1.5h |
| **Reshape data** | 08_pivoting_reshaping.ipynb | 1.5h |
| **Analyze time series** | 09_timeseries_groupby_dynamic.ipynb | 2h |
| **Read/write cloud data** | 11_advanced_io_cloud_storage.ipynb | 2h |
| **Work with nested data** | 12_nested_data_structures.ipynb | 2h |
| **Understand types** | 13_data_types_schemas.ipynb | 1h |
| **Clean messy data** | 14_missing_duplicate_handling.ipynb | 1.5h |
| **Use with Pandas/DuckDB** | 16_interoperability.ipynb | 2h |
| **Validate data quality** | 18_data_quality_validation.ipynb | 1.5h |
| **Optimize performance** | 19_performance_debugging.ipynb | 2h |
| **Use custom functions** | 20_udfs_custom_functions.ipynb | 2h |
| **Query with SQL** | 21_sql_interface.ipynb | 1.5h |
| **Visualize data** | 22_visualization.ipynb | 1.5h |

---

## 💡 Top 3 Must-Know Concepts

### 1. Lazy Evaluation ⭐⭐⭐
```python
# Instead of this (eager):
df = pl.read_csv("data.csv")
result = df.filter(pl.col("age") > 30).select(["name", "age"])

# Do this (lazy - much faster!):
result = (
    pl.scan_csv("data.csv")
    .filter(pl.col("age") > 30)
    .select(["name", "age"])
    .collect()  # Only executes here!
)
```
📖 **Learn in:** 02_lazy_evaluation_optimization.ipynb

### 2. Expressions ⭐⭐⭐
```python
# Expressions are composable and powerful
df.select([
    pl.col("price"),
    (pl.col("price") * 1.1).alias("price_with_tax"),
    pl.when(pl.col("quantity") > 10)
      .then(pl.col("price") * 0.9)
      .otherwise(pl.col("price"))
      .alias("discounted_price")
])
```
📖 **Learn in:** 03_expressions_selectors.ipynb

### 3. Selectors ⭐⭐
```python
import polars.selectors as cs

# Apply operations to all numeric columns at once!
df.select(cs.numeric() * 2)

# Or all string columns
df.select(cs.string().str.to_uppercase())
```
📖 **Learn in:** 03_expressions_selectors.ipynb

---

## 🎯 Success Checkpoints

### ✅ After Week 1 - You should be able to:
- [ ] Create DataFrames from various sources
- [ ] Understand the difference between eager and lazy
- [ ] Write basic expressions with `pl.col()`
- [ ] Use `when/then/otherwise` for conditional logic

### ✅ After Week 2 - You should be able to:
- [ ] Handle missing data and duplicates
- [ ] Work with strings and dates
- [ ] Choose appropriate data types
- [ ] Clean and prepare real-world data

### ✅ After Week 3 - You should be able to:
- [ ] Perform all 7 types of joins
- [ ] Use group_by with complex aggregations
- [ ] Apply window functions
- [ ] Reshape data between wide and long formats

### ✅ After Week 4 - You should be able to:
- [ ] Analyze time series data
- [ ] Integrate with Pandas, NumPy, DuckDB
- [ ] Optimize slow queries
- [ ] Build production-ready pipelines

---

## 🔥 Common Mistakes to Avoid

### ❌ Forgetting to `.collect()` on lazy queries
```python
# This does nothing!
result = df.lazy().filter(pl.col("age") > 30)  # No execution

# Do this:
result = df.lazy().filter(pl.col("age") > 30).collect()  # ✅
```

### ❌ Using `.apply()` when expressions work
```python
# Slow!
df.select(pl.col("value").map_elements(lambda x: x * 2))

# Fast! (100x faster)
df.select(pl.col("value") * 2)  # ✅
```

### ❌ Reading entire file when you need filtered data
```python
# Reads entire file:
df = pl.read_csv("huge.csv").filter(pl.col("category") == "A")

# Only reads needed data:
df = pl.scan_csv("huge.csv").filter(pl.col("category") == "A").collect()  # ✅
```

### ❌ Multiple passes over data
```python
# Multiple passes (slower):
df = df.with_columns((pl.col("a") * 2).alias("a2"))
df = df.with_columns((pl.col("b") * 2).alias("b2"))

# Single pass (faster):
df = df.with_columns([
    (pl.col("a") * 2).alias("a2"),
    (pl.col("b") * 2).alias("b2")
])  # ✅
```

---

## 🎬 Get Started Now!

```bash
# 1. Open first notebook
jupyter notebook polars-complete-guide.ipynb

# 2. Run all cells and follow along

# 3. Try modifying examples

# 4. Complete the exercises

# 5. Move to next notebook!
```

---

## 📞 Need Help?

1. **Check the full guide:** `LEARNING_PATH.md`
2. **Search docs:** https://docs.pola.rs/
3. **Ask community:** Discord - https://discord.gg/4UfP5cfBE7
4. **Read source:** Each notebook has detailed explanations

---

**Ready to start? Open `polars-complete-guide.ipynb` now! 🚀**

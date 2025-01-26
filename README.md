# Fractal Analysis and Outlier Detection

Advanced pattern analysis using fractal mathematics for time series data and anomaly detection.

## Overview

This project implements fractal-based analysis techniques for:
- Pattern recognition in time series data
- Outlier and anomaly detection
- Complex system analysis

## Understanding Fractals

Fractals are geometric patterns exhibiting self-similarity at different scales. Examples:
- Tree branching structures
- Coastline patterns
- Snowflake geometries

### Real-World Applications

1. **Natural Systems**
   - Biological structures (lungs, blood vessels)
   - Geological formations
   - River networks

2. **Technology**
   - Computer graphics terrain generation
   - Network traffic analysis
   - Financial market modeling

3. **Medical Analysis**
   - Brain structure analysis
   - Heart rate variability
   - DNA pattern recognition

## Implementation Details

### Core Components

1. **Fractal Generation**
   - Julia sets implementation
   - AntiFractal algorithms
   - Parameter control (α, scaling factors)

2. **Time Series Analysis**
   - 1D series extraction
   - Pattern recognition
   - Self-similarity measurement

3. **Outlier Detection System**
   ```python
   def analyze_timeseries(x: np.ndarray) -> Tuple[float, float]:
       # Compute fractal metrics
       D = compute_fractal_dimension(x)
       H = compute_hurst_exponent(x)
       return D, H
   ```

### Key Metrics

1. **Hurst Exponent (H)**
   - Measures time series persistence
   - Range: 0-1
   - H > 0.5: Trending behavior
   - H < 0.5: Mean-reverting behavior

2. **Fractal Dimension (D)**
   - Quantifies pattern complexity
   - Relationship: D = 2 - H
   - Higher D indicates more complexity

## Detection Methodology

### Process Flow
1. Window Segmentation
2. Metric Computation
3. Anomaly Detection
4. Result Aggregation

### Detection Algorithm
```python
def detect_outliers(time_series, window_size=100):
    segments = segment_timeseries(time_series)
    metrics = compute_segment_metrics(segments)
    return identify_anomalies(metrics)
```

## References

- Paper Link: [Fractal Analysis for Pattern Recognition](https://www.tandfonline.com/doi/full/10.1080/27684830.2024.2401324)

## License

MIT License

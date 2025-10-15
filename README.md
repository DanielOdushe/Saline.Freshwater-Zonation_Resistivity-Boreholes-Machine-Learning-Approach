# Integrated Geophysical Investigation with Machine Learning for Seawater Intrusion Delineation in Igbo Efon, Southwestern Nigeria

##  Project Overview

This comprehensive hydrogeophysical study integrates **Electrical Resistivity Tomography (ERT)**, **Vertical Electrical Sounding (VES)**, and **Machine Learning (ML)** techniques to delineate seawater intrusion in coastal aquifers of Igbo Efon, Southwestern Nigeria. The project successfully maps subsurface resistivity variations, identifies saline-freshwater interfaces, and develops predictive models with **92.4% accuracy**.

##  Research Objectives

1. **Conduct geophysical surveys** (VES and ERT) to delineate subsurface resistivity variations and saltwater interface
2. **Assess vertical and lateral aquifer continuity** using 2D resistivity imaging
3. **Construct integrated earth models** revealing subsurface lithology
4. **Validate subsurface models** with borehole data for accurate lithological representation
5. **Identify saline water invasion zones** and their occurrence depths
6. **Implement machine learning** for validation and predictive modeling of saline-freshwater boundaries

##  Project Structure

### Data Collection Components
- **Vertical Electrical Sounding (VES)**: 20 stations across 5 traverses
- **Constant Separation Traversing (CST)**: 5 ERT profiles (TR1-TR5) covering 160-200m each
- **Borehole Data**: 2 wells (BH_1 and BH_2) with comprehensive geophysical logging
- **Field Instrumentation**: OHMEGA Resistivity Meter with full accessory suite

### Data Processing Workflow
- **VES Processing**: 1D inversion and modeling using PyGIMLi 
- **ERT Processing**: 2D inversion and modeling using PyGIMLi 
- **Data Integration**: Spatial correlation of VES, ERT, and borehole data
- **Machine Learning**: Random Forest classification and regression models

### Key Deliverables
1. **2D Resistivity Models**: ERT inversion results for all 5 traverses
2. **Integrated Lithological Sections**: Geo-sections combining VES and borehole data
3. **ML Prediction Models**: Automated saline/freshwater classification system
4. **Comprehensive Technical Report**: Methodology, results, and recommendations

##  Methodology

### Geophysical Surveys
- **VES Technique**: Schlumberger array configuration with depth penetration >100m
- **ERT Technique**: Wenner array with 2D inversion using PyGIMLi
- **Survey Parameters**: 
  - Electrode spacing: 5m
  - Profile lengths: 160-200m
  - Depth investigation: 40m+

### Machine Learning Framework
- **Algorithm**: Random Forest Classifier & Regressor
- **Feature Set**: Resistivity, Gamma Ray, Depth parameters, derived ratios
- **Validation**: Group K-Fold Cross-Validation by borehole
- **Performance Metrics**: Accuracy, ROC AUC, Precision, Recall, F1-Score

### Python Libraries Used

#### Core Data Processing
```python
import pandas as pd          # Data manipulation and analysis
import numpy as np           # Numerical computing
import pygimli as pg         # Geophysical inversion and modeling
import matplotlib.pyplot as plt  # 2D plotting and visualization
import seaborn as sns           # Statistical data visualization
import plotly.graph_objects as go # Interactive plots


### Data Integration Approach
- **Spatial Alignment**: VES stations located along ERT traverses
- **Depth Correlation**: Borehole lithology used to validate geophysical interpretations
- **Quality Control**: RMS error assessment for all inversion models

##  Key Findings

### Hydrogeological Framework

- **Resistivity Range: 0.4 - 1776 Ωm across study area
- **Saline Intrusion: Identified in shallow to medium depths (20-80m)
- **Shallow Aquifers** (60-120m): Vulnerable to saline intrusion with thin protective layers
- **Deep Aquifers** (>140m): Protected by thick clay-peat seals (10-30m thickness)
- **Transition Zone**: 70-90m depth with variable salinity conditions
- **Protective Layers**: Identified clay-peat seals at 125-135m (BH_1) and 120-130m (BH_2)

### Saline Intrusion Patterns
- **Spatial Distribution**: Complex lateral variations across traverses
- **Depth Progression**: Increasing salinity with depth in southern sections
- **Vulnerability**: Higher intrusion risk in TR1 and TR2 areas
- **Protected Zones**: TR3 and deep aquifers show minimal saline influence

### Machine Learning Results
- **Classification Accuracy**: 92.4%
- **ROC AUC**: 0.927
- **Precision (Saline)**: 95.0%
- **Recall (Saline)**: 82.6%
- **Top Predictive Features**: Depth_Normalized (34.5%), Log_Resistivity (24.8%)

##  Technical Implementation

### Software Tools
- **PyGIMLi**: Core 2D inversion modeling for  2D ERT data and VES data inversion
- **Python ML Stack**: scikit-learn, pandas, numpy, matplotlib, seaborn
- **Data Processing**: Custom Python scripts for integration and visualization

### Data Quality Assessment
- **Total Samples Analyzed**: 439
- **Borehole Coverage**: BH_1 (221 samples), BH_2 (218 samples)
- **VES Data Coverage**: 11-20% across boreholes
- **ERT Data Quality**: RMS errors 5.50-16.01% across traverses

### Model Performance
- **Overall Accuracy**: 92.4%
- **Feature Importance**: Depth and resistivity parameters most significant
- **Validation**: Robust group-based cross-validation
- **Uncertainty Quantification**: Comprehensive error analysis

##  Implementation Value

### Water Resource Management
- **Sustainable Extraction**: Identification of protected deep aquifers for long-term use
- **Risk Assessment**: Spatial mapping of vulnerable zones requiring monitoring
- **Protection Strategies**: Utilization of natural clay seals for aquifer protection
- **Planning Tool**: Data-driven approach for groundwater management decisions

### Scientific Contribution
- **Methodology Integration**: Successful fusion of traditional geophysics with modern ML
- **Validation Framework**: Multi-method cross-verification enhances reliability
- **Scalable Approach**: Transferable methodology for similar coastal regions
- **Technical Innovation**: PyGIMLi implementation for robust inversion

##  Usage Instructions

### Model Application
1. Use trained ML models for new data classification
2. Apply ERT inversion workflows to new survey data
3. Utilize integration scripts for multi-data correlation

### Visualization
1. Refer to ERT inversion images for 2D resistivity distribution
2. Study integrated sections for VES-ERT-borehole correlation
3. Analyze ML performance metrics for model reliability

##  Future Enhancements

### Immediate Priorities (0-6 months)
- Real-time monitoring system implementation
- Expanded spatial coverage surveys
- Community engagement and awareness programs

### Medium-term Development (6-24 months)
- Climate change impact modeling
- Advanced deep learning approaches
- Multi-method geophysical integration

### Long-term Vision (2-5 years)
- Automated alert systems for intrusion detection
- Policy framework development
- Regional scaling of methodology

##  Project Metrics

### Data Coverage
| Parameter | BH_1 | BH_2 | Overall |
|-----------|------|------|---------|
| Samples | 221 | 218 | 439 |
| Depth Range | 12-232m | 18-235m | 12-235m |
| VES Coverage | 19.9% | 11.0% | 15.5% |
| CST Coverage | 12.7% | 10.1% | 11.4% |

### ERT Survey Quality
| Traverse | Length | RMS Error | Quality |
|----------|--------|-----------|---------|
| TR1 | 200m | 10.27% | Good |
| TR2 | 200m | 15.63% | Fair |
| TR3 | 200m | 6.23% | Excellent |
| TR4 | 200m | 16.01% | Fair |
| TR5 | 175m | 5.50% | Excellent |

### ML Performance
| Metric | Value | Interpretation |
|--------|-------|---------------|
| Accuracy | 92.4% | Excellent |
| ROC AUC | 0.927 | Strong discrimination |
| Precision | 95.0% | Minimal false positives |
| Recall | 82.6% | Good detection rate |

*This project represents a significant advancement in coastal groundwater management through innovative integration of geophysical methods and machine learning, providing a sustainable framework for addressing saltwater intrusion challenges in coastal Nigeria and similar regions worldwide.*

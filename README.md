# BIPV-Climate-Energy
This repository contains the publicly available components of the implementation for the paper "Mitigating Urban Climate-Energy Feedback with Citywide Building-Integrated Photovoltaics Implementation". 

# Author
Liutao Chen (chenlt@ust.hk, chenlt@uw.edu)


# Note on Code Availability:
This repository contains selected modules from our complete urban climate and energy modelling framework. These are self-contained tools that can be used independently for specific analysis tasks.


# Available Modules
## 1. Input parameters
  The `Input_Parameters.xlsx` file contains all essential input parameters required to run the simulations of BEM-SLUCM and GeoBEM. 

## 2. Create_uTMY/ - Urban Weather Generator
 	    Purpose: Generates urbanized Typical Meteorological Year (uTMY) EPW files
    
   	  Technology: MATLAB + Urban Canopy Model outputs
  
 	    Core Function: Integrates UCM outputs with standard meteorological data to create urbanized EPW files
  
     	Compatibility: Full compatibility with EnergyPlus building simulation software
  
 	    Input: Base TMY files + UCM simulation data (.mat files)
  
 	    Output: Urbanized TMY EPW files
  

## 3. Power_GeoBEM/ - Building Facade BIPV Power Calculator
 	    Purpose: Calculates Building-Integrated Photovoltaic (BIPV) facade power output from EnergyPlus outputs
  
 	    Technology: Python + EnergyPlus result processing
  
 	    Core Function: Processes hourly energy simulation data to calculate power generation for each building facade
    
 	    Input: EnergyPlus simulation results (CSV files) + building information
  
 	    Output: Annual power output (JSON) + hourly generation data (8760 hours)


## 4. Power_GlobalCities/ - Global Cities BIPV Power Estimator
 	    Purpose: Estimates hourly BIPV power output for different facade orientations across multiple cities
  
 	    Technology: MATLAB + TMY weather data processing
  
 	    Core Function: Calculates BIPV power output using Typical Meteorological Year data for global cities
  
 	    Input: EPW weather files (samples of global cities)
  
 	    Output: Hourly power data (CSV) + monthly heatmap visualizations


# Quick Start
Each module operates independently - Navigate to the specific tool you need:

Choose the tool for your specific application:
  
 	    cd Create_uTMY/          # For generating urbanized Typical Meteorological Year (uTMY) EPW files
  
 	    cd Power_GeoBEM/         # For calculating building facade power generation
  
 	    cd Power_GlobalCities/   # For multi-city BIPV potential analysis


# Each folder contains:
 	    Complete executable code

 	    Detailed documentation (sub-README)

 	    Sample data

 	    Environment dependencies


# Support
For questions regarding these specific modules, please check the individual README files in each folder first.
Each module contains detailed setup and execution instructions.
 

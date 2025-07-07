# Capstone_Project
Project Overview

This project focuses on creating a simulation-based system that adjusts parking prices dynamically for urban parking spaces. It uses historical data to replicate real-time conditions and applies pricing logic based on parking occupancy. The objective is to enhance parking efficiency by using a data-driven, adaptive pricing strategy.

Technologies Used

Python

Pandas, NumPy for data handling

Bokeh for real-time visualization

Pathway (used for streaming logic)

Visual Studio Code (development)

Git and GitHub for version control

System Architecture

graph TD
    Input[CSV Input Data] --> Streamer[Background Data Thread]
    Streamer --> Model[Pricing Logic]
    Model --> Source[ColumnDataSource]
    Source --> Plot[Bokeh Visualization]
    Server[Bokeh Server] --> Plot
    Plot --> Browser[Live Browser Chart]

Workflow Summary

Data Source: A CSV file with parking attributes like Occupancy and Capacity serves as the data input.

Streaming Setup: A separate thread mimics real-time data streaming by reading one record at a time from the dataset with a delay.

Live Plotting: Bokeh is used to display the price evolution in a browser-based chart that updates each second.

Interaction: The visualization is accessible through the local Bokeh server (localhost:5006)


Main Features

Real-time simulation of price updates
Threaded data streaming with safe Bokeh integration
Visual feedback via interactive browser plot
Step-by-step logs of streaming and computation


![Untitled diagram _ Mermaid Chart-2025-07-07-153411](https://github.com/user-attachments/assets/24821e54-7597-4b4a-9561-1995f444af19)

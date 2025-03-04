# Visualizing Data with Plotly

## Overview

In the previous lesson, you explored basic charts like scatter plots, bar charts, and histograms using `matplotlib`. In this lesson, you'll learn how to create interactive visualizations using a tool called Plotly.

## Learning Objective

By the end of this lesson you will be able to:

- Present data in more engaging and user-friendly formats.
- Create common chart types (histograms, scatter plots) with Plotly.
- Customize plots with titles, labels, and legends.

## Key terms

**Plotly:** an interactive, open-source, and browser-based graphing library for Python.

## Starter Code

This lesson encourages experimentation. Use the included [Collaboratory notebook]() to run the code as you learn, or read the lesson and then freely experiment with the notebook's code.

## Introduction

Plotly is a tool that helps you create **interactive** charts and graphs easily. Unlike regular charts, Plotly charts let you **zoom in, hover over points to see details, and even turn data on or off** by clicking the legend. Plotly allows data scientists to explore and present data in a visually engaging and interactive way. Think of it as a **"smart" graph maker** that lets you play with your data instead of just looking at it!

The following video presents

## Installing and importing Plotly



## Creating Basic Charts

### Scatter plot

Recall that a scatter plot is used to display the relationship between two numerical variables, where each data point is represented by its coordinates on the x and y axes. This allows you to quickly identify trends, clusters, or outliers in your data.

In Plotly, creating a scatter plot is straightforward: you simply provide your DataFrame, the columns for the x and y axes, and optionally use additional parameters such as `color` or `symbol` to highlight different categories. For example, you can run `fig = px.scatter(df, x='columnX', y='columnY', color='category')` and then call `fig.show()` to generate an interactive scatter plot that displays tooltips, supports zooming, and allows you to toggle data series on or off.

Let's create a sample dataset and plot it with Plotly.

```python
# Create a new dataset for demonstration
df_scatter = pd.DataFrame({
    'X': np.random.rand(30),
    'Y': np.random.rand(30),
    'Label': np.random.choice(['Type A', 'Type B', 'Type C'], 30)
})
```

```python
fig = px.scatter(
    df_scatter,
    x='X',
    y='Y',
    color='Label',      # Points will have different colors based on Label
    title="Scatter Plot Example"
)
fig.show()
```

The code above takes data from the table (df_scatter), puts values from column "X" on the x-axis and values from column "Y" on the y-axis. The dots are colored differently based on the "Label" column (like grouping them into categories), and then it shows the chart so you can interact with it! The resulting graph looks like this:

![A scatter plot](scatterplot.png)


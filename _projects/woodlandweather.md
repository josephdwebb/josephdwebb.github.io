---
layout: project
title: 'WoodlandWeather'
caption: An open source geospatial tool matching field research sites to NCEI weather reports.
description: >
  My goals, progress, and results while constructing an intuitive and accessible software to complement biological field research.
date: '01-10-2023'
image: 
  path: assets/img/projects/WoodlandWeather.png
  srcset: 
    1920w: /assets/img/projects/WoodlandWeather.png
    960w:  /assets/img/projects/WoodlandWeather_960.png
    480w:  /assets/img/projects/WoodlandWeather_480.png
links:
  - title: GitHub
    url: https://github.com/josephdwebb/woodlandweather 
sitemap: false
---

Introducing **WoodlandWeather**, an open-source software tailored to support field biologists and ecologists in their research endeavors. This tool is crafted with the goal of fostering a deeper understanding of the intricate connections between ecosystems and the dynamic atmospheric conditions that surround them. Users can easily input the geographic coordinates of their research sites, allowing WoodlandWeather to seamlessly access and retrieve the most recent and comprehensive climate data from the National Center of Environmental Information (NCEI), facilitating an in-depth exploration of the climate and weather conditions within their targetted site.

WoodlandWeather simplifies the process of ecological research, enabling researchers to effortlessly examine, compare, and visualize long-term weather and climate patterns. This resource proves invaluable for a wide range of research areas, from the study of plant phenology and wildlife behavior to the assessment of forest resilience. Join a growing community of dedicated scientists and environmental enthusiasts as we embark on a collective journey to merge the beauty of the natural world with cutting-edge technology. 

## Installation
If you would like to use `woodlandweather()` yourself, please refer to the following steps regarding installation and use.

### Step 1: Making a Pull Request

1. Visit [WoodlandWeather](https://github.com/josephdwebb/woodlandweather). If you don't have the repository, you can clone it to your local machine.
2. To make a Pull Request, fork the repository to your own GitHub account.
3. Clone your forked repository to your local machine using Git or GitHub Desktop.

### Step 2: Opening the Program

1. Open your preferred R environment, such as RStudio or VisualStudioCode.
2. In your R environment, navigate to the `WoodlandWeather.R` file within your local clone of the repository.
3. Open the `WoodlandWeather.R` file.

### Step 3: Running the Program

1. Select the entire code in the `WoodlandWeather.R` file by pressing `Ctrl + A` (Windows/Linux) or `Cmd + A` (Mac) to highlight everything.
2. Run the selected code by pressing `Ctrl + Enter` (Windows/Linux) or `Cmd + Enter` (Mac). This will run the program and log the variables and functions.

### Step 4: Running `install()`

1. After the `WoodlandWeather` program completes, you will be ready to use it. However, you need to download station data first. To do this, execute the `install()` function.

```R
install()
```
This step will begin the data download process. Please be aware that instalation will require about 5GB of space and up to 8 hours to complete. The code will output a confirmation message when the installation is finished, at which point you can proceed to use woodlandweather[options] for data retrieval.

## Using WoodlandWeather
The `woodlandweather` function is used to retrieve weather data for a specified site. The required arguments are:

| Required Argument | Description                    |
|-------------------|--------------------------------|
| s                 | Site name                      |
| lat               | Latitude of the site           |
| long              | Longitude of the site          |
| m                 | Month (MM) for data retrieval  |
| y                 | Year (YYYY) for data retrieval |
| n                 | Number of stations to retrieve |
{:.scroll-table-small}

**Example**:
```R
woodlandweather(s = "Centennial", lat = 44, long = -73, m = 06, y = 2022, n = 3)
```
This function will retrieve NCEI weather station data for the desired time period, reorder the stations by distance, and export a summary table. You can choose to export the variables for the identified station(s) as a CSV file.

## Help
To get assistance or view usage instructions, you can use the `help()` function:
This will provide information on required arguments and general usage.

For more information and updates, please visit the [GitHub Page](https://github.com/josephdwebb/woodlandweather) and feel free to contribute or contact Joseph at josephwebb4@hotmail.com for support and feedback.
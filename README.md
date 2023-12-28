## Table of Contents

- [About the Project](#about-the-project)
  - [Resources](#resources) 
- [Key Features of SA-IoTDG](#features)
  - [Data Source](#data-origin)
  - [Data Preparation](#data-preparation)
- [Model Training](#training)
- [Model Evaluation](#model-evaluation)
- [Results](#results)


## About the Project

SA-IoTDG is the tool that allows you to simulate IoT devices data with great flexibility. With this tool you won't need to code another new simulator for each IoT project.

### Key features of SA-IoTDG:

** Situation Description System: Defines and characterizes various states and transitions within the IoT application's operational context.
** SysML Model: Captures the functional and non-functional requirements of the IoT application for data generation.
** Markov Chain-Based Data Generation: Models the dynamic nature of IoT data by using a state-transition matrix to generate realistic data sequences, transitioning between situations based on their defined probabilities.


## Getting Started

**Prerequisites**
*docker* (v. 17.05+) and *docker-compose* should be installed

**Startup**
Run the following commands in the folder with *docker-compose.yml* and *.env* files from *release* folder:

    docker-compose pull
    docker-compose up

UI will be available by the following url:
http://localhost:8090 or http://docker-machine-ip:8090
depending on the OS or docker version.


![demo](https://user-images.githubusercontent.com/4072962/38543721-023134b4-3cae-11e8-8e97-ee6468771e2a.gif)

Simulator **features** that you will like:
1. Replay existing datasets with modified data (such as updated timestamps, generated ids etc);
2. Automatic derivation of dataset structure which allows you to customize your dataset without the need to describe its structure from scratch;
3. Generate datasets of any complexity. Generated data can be described via constructor or JavaScript function. Multiple rules are available in constructor such as "Random integer", "UUID" and others. JS function  gives you maximum flexibility to generate data - it supports popular JS libraries *lodash* and *momentjs*.
4. Send data to the platforms you use with minimum configuration (see *Supported target systems* section);
5. Customize frequency with which data will be sent - based on dataset timestamp properties or just constant time interval. The tool also supports relative timestamp properties which depend on other timestamp or date properties. It means that data can be replayed with the same interval between timestamps as in initial dataset.
6. Easy installation - all you need is to download 2 docker files and run 2 commands.

If you would like read more about why we created this tool, please read **Motivation** section.


 
##  Usage

**Generate data**

To generate data on the fly, navigate to *Add Situations* screen, then:

   1. Select the application for which data has to be generated
   2. Configure the situations;
   3. Select the situation transition parameters;
   4. You can select the frequency/no of data records to be generated
   5. Click on *Generate Data*. 
   





## Intended usage and useful scenarios




## Acknowledgements

This tool is extended from [link](https://github.com/IBA-Group-IT/IoT-data-simulator/).

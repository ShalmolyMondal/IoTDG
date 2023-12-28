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
** SysML Model: Captures the functional and non-functional requirements of the IoT application for data generation. The framework integrates a SysML model to capture and represent IoT application requirements effectively.
** Markov Chain-Based Transition: SA-IoTDG utilizes a Markov chain-based approach for smooth transitions in IoT data generation corresponding to different situations. It models the dynamic nature of IoT data by using a state-transition matrix to generate realistic data sequences, transitioning between situations based on their defined probabilities.

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



If you would like read more about why we created this tool, please read **Motivation** section.

Detailed work can be found here. [Publication](https://www.mdpi.com/1424-8220/23/1/7)

 
##  Usage

**Generating data**

The tool allows data to be generated based on two methods:

(1). Replay Data Generator

In this method, a small sample of data is provided as a seed to the tool. This approach allows for generating data that closely mimics real-world scenarios and helps ensure that the generated data is relevant and useful for the intended IoT
application or users.

(2). Situation based Data Generator 

This was developed by extending the [IoT data simulator tool](https://github.com/IBA-Group-IT/IoT-data-simulator/). 

To generate data on the fly, navigate to *Add Situations* screen, then:

   1. Select the application for which data has to be generated
   2. Configure the situations;
   3. Select the situation transition parameters;
   4. You can select the frequency/no of data records to be generated
   5. Click on *Generate Data*. 
   

## Experimental Results and Validation

Experimental evaluations validate SA-IoTDG's ability to generate IoT data resembling real-world scenarios and enable performance evaluations of IoT applications on various middleware platforms.

We demonstrate SA-IoTDG using a real-world traffic monitoring scenario, showcasing its ability to generate realistic traffic data.

Extensive experimental evaluations confirm:
* SA-IoTDG's ability to generate data statistically similar to real-world traffic data.
* The effectiveness of using generated data for performance evaluation of deployed IoT applications on different middleware platforms.

For the first method of data generation, which is the **replay method**, the analysis revealed that the input data followed a Gaussian distribution; hence, data with the same distribution was generated.

<p float="left">
  <img src="ExperimentalResults/gen_data_fit.png" width="300" />
  <img src="ExperimentalResults/metro_data_fit.png" width="300" /> 
</p>

For the second method, the **Situation Based**, the tool was validated to generate data based on a situation transition approach.

![SitDataGen](ExperimentalResults/SituationBasedDataGen.png)

## Intended usage and useful scenarios

The project includes a demonstration using a real-world example for a traffic monitoring scenario to showcase the practical application of SA-IoTDG.


## Acknowledgements

This tool is extended from [link](https://github.com/IBA-Group-IT/IoT-data-simulator/).

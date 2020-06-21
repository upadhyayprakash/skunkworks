# skunkworks

Code Name: **TOOLSPROJECTS** (SKUNKWORKS TOOLS)
<br/>
Alternate Name: **Skunk-DPipe**

SkunkWorks related Technical &amp; Research Artifacts

###### This document focuses on Tools & Interfaces that'll be used to automate the Data Collection, Pre-processing & Annotation for any ML based project for image/text/audio data types.

[![N|Solid](https://www.testing-whiz.com/media/2832/best-practices-for-effective-data-driven-test-automation-approach2.jpg)](http://theschoolof.ai/)

##### NOTE:

- This guide presents the research done for the Tools that can be used for the Data Pipeline of the ML Projects at SkunkWorks
- WorkFlow automation Tools are dealt in major details and proposal for the other Data Pipeline stages have been briefed as well.
- More extensive research is needed in Data Processing and Collection area to find the open-source alternatives or build one for our use-cases.
<br/>

# Modules
* Data Collection & Storage
	- Data Source Integration: DB, Excel/CSV, Unstructured Sources(web-scrapped), Streaming Source
	- Data Generators(Simulating Real-world Dataset)
	- Pre-Filter definition. E.g. of filters is, "Only 'JPEG' images of size '480p' and above"
	- Storage(S3, Annotation will be easily scaled)

* Data Pre-processing
	- Data Cleaning and Filtering (Image formats - PNG, JPEG, GIF, BMP)

* Data Annotation
	- Build the Pipeline for the Dataset Annotation
	- Data Source Definition/Integration
	- Defining the Output Format and its Storage

* Online Learning(Tackling the Dataset Shift)
	
* WorkFlow(ML Pipeline Automation): Identify the Data Pipeline 'Stages' and build 'Modules'

	- Workflow Definition, Automation & Monitoring
		- Apache "AirFlow" Orchestration [a DAG(Directed Acyclic Graph) based WF Automation Framework]
			- https://airflow.apache.org/
		- Kedro-AirFlow: A Kedro Plugin for AirFlow
			- https://github.com/quantumblacklabs/kedro
			- https://github.com/quantumblacklabs/kedro-airflow/
			- Powered-by 'CookieCutter' Project Structure Management:
				- https://github.com/drivendata/cookiecutter-data-science
				- http://drivendata.github.io/cookiecutter-data-science/
		- DVC(Data Version Control): https://github.com/iterative/dvc
			- Data and Model Version Tracking
    		- Manage Experiments
			- On-Cloud and On-Premise Data Integration
		- Using TPOT(https://github.com/EpistasisLab/tpot)
			- Similar to AutoML
		
        Finally, we can use previous mentioned projects or try these Open-Source Platform for ML Automation. We can replicate the features of these project or clone it to make changes.
		- ArangoML: A ML Pipeline 'Metadata' Management
			- https://github.com/arangoml/arangopipe
			- Documentation: https://github.com/arangoml/arangopipe/blob/master/documentation/README.md
			
		- Allegro.ai's "TRAINS" - Experiment Manager and MLOps (https://allegro.ai/)
			- Experiment Management
    		- Open-Source: https://allegro.ai/trains-open-source/
			- GitHub:
				- Backend Code: https://github.com/allegroai/trains/
				- Web UI Code(Angular9): https://github.com/allegroai/trains-web

	- Command-line utility(Manual Override)
		- A CLI utility for all the major Tasks.
	- Monitoring Dashboard for Status of the Data Pipeline to monitor
		- Stats of each dataset
		- Its progress & current status in the ML Data Pipeline
		- Anomaly Detection and Alert in process and data.

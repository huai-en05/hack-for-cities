# hack-for-cities

## Project Description
ArborGuard AI is a three-agent system designed to monitor tree vulnerability, anticipate weather-driven stress and support operational decision-making at scale. It helps managing agencies identify which trees are most at risk of failure and require closer attention.

Tree Health Agent evaluates the structural vulnerability of individual trees and computes a qualitative tree risk score that represents the likelihood of failure due to physical instability or poor health, as well as a computed probability of the tree falling. Climate Agent monitors weather conditions using the OpenMateo API dynamically adjusts risk thresholds and amplifying concern for structurally vulnerable trees. Risk Assessment Agent synthesises outputs from the Tree Health and Climate Agents to prioritise trees for inspection or closer monitoring.
 
## Setup Instructions
As you would have to manually set up the agents, please create an IBM account. 

### Setting up of the Tree Health Agent 
Under Build agents and tools, click the Create Agent button.
Select create from scratch and input the following: 
#### Name 
Tree Health Agent
#### Description 
Use this agent to analyze LiDAR data of trees in Singapore and detect potential weaknesses including pest infestation, diseases, nutrient deficiency, and root instability. Identify high-risk trees requiring immediate maintenance, assess fall probability, and generate a prioritized summary in JSON file format. Do not re-list trees or make maintenance scheduling decisions. 

#### Agent Style 
Default

#### Knowledge sources
Download all the files under the trees_csv folder in this Github and save it in your document. Upload all 4 files under the knowledge source.
Description:
The PDF file contains the instructions of how to process the LiDAR data to evaluate the health of the tree and determine whether it requires assistance. The CSV files contain the LiDAR data of some trees in Singapore. 

* Click edit knowledge setting and change max search results to 20 * 

#### Behavior
Scan the entire LiDAR CSV in your knowledge base. Identify every unique Tree_ID present in the file. List all 20 trees and provide the evaluated health output for each one. Do not summarize or skip any rows. Return me a JSON file containing the following: tree_id, region, species, probability of falling score, priority level.

#### Guidelines
Name: Selective reading of CSV file
Condition: No conditions, this should be implemented throughout
Action:
Rule 1: You are currently in 'Simulation Mode.' Whenever prompted, always start with the first CSV file titled t1.csv and do not read the other csv files first. Each of my CSV file contain 20 trees, please read all and return all 20 trees. Rule 2: If the user asks to 'Refresh Data' or after 1 minute, increment the Simulation Week and analyze the next file in the sequence. Return the update JSON file with processed data for the new simulation week only.

* Note that the refresh timing for the updated reading of the CSV file is 1 min to simulate a quick refresh, but in the actual scenario, it should refresh once new LiDAR data is captured *
 
####Channel - Home Page
Toggle if off

### Weather Agent 

### Risk Assessment Agent 




 
## Usage Guide
 Clear instructions on how to test or interact with the solution, with examples where applicable.


 
## Deployment Instructions (if applicable)
 Steps required to deploy the solution in a real-world or cloud environment.
 
## Contributors
 1. Charlize Teo Hui Zi
 2. Christy Gan
 3. Hellen
 4. Seah Shi Han
 5. Tan Huai En
 
### Additional Notes
Assume that The system assumes the availability of basic sensing infrastructure, such as periodic Light Detection and Ranging (LiDAR) scans. In the prototype, these inputs are simulated using representative datasets to demonstrate system behaviour in the absence of real-world data. 

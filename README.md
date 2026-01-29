# hack-for-cities

Project Description
ArborGuard AI is a three-agent system designed to monitor tree vulnerability, anticipate weather-driven stress and support operational decision-making at scale. The system is conceived as a city-level decision-support platform that helps managing agencies identify which trees are most at risk of failure and require closer attention.

The system assumes the availability of basic sensing infrastructure, such as periodic Light Detection and Ranging (LiDAR) scans. In the prototype, these inputs are simulated using representative datasets to demonstrate system behaviour in the absence of real-world data. This assumption reflects realistic deployment conditions in Singapore, where such data is increasingly available through smart city initiatives. At the core of ArborGuard AI is its agentic design. Each agent maintains its own goals and reasoning logic while sharing insights with the others to collectively reduce tree failure risk. 

Tree Health Agent evaluates the structural vulnerability of individual trees and computes a qualitative tree risk score that represents the likelihood of failure due to physical instability or poor health, as well as a computed probability of the tree falling.

Climate Agent monitors weather conditions using the OpenMateo API dynamically adjusts risk thresholds and amplifying concern for structurally vulnerable trees.

Risk Assessment Agent
Synthesises outputs from the Tree Health and Climate Agents to prioritise trees for inspection or closer monitoring.



 
Setup Instructions
 Step-by-step instructions to run the project locally, including required dependencies and configurations.



 
Usage Guide
 Clear instructions on how to test or interact with the solution, with examples where applicable.


 
Deployment Instructions (if applicable)
 Steps required to deploy the solution in a real-world or cloud environment.
 
Contributors
 1. Charlize Teo Hui Zi
 2. Christy Gan
 3. Hellen
 4. Seah Shi Han
 5. Tan Huai En
 
Additional Notes
Assume that The system assumes the availability of basic sensing infrastructure, such as periodic Light Detection and Ranging (LiDAR) scans. In the prototype, these inputs are simulated using representative datasets to demonstrate system behaviour in the absence of real-world data. 

Please ensure that the repository is well-organised, excludes any sensitive information (e.g. API keys or credentials), and is easy for judges to review.

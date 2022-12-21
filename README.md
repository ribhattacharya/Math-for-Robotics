# Math-for-Robotics
Math concepts/tools used in robotics

Platform used for these projects: osx-64 (MacBook Air M1 2020)

This file may be used to create an environment using Anaconda:

    $ conda create --name <your env name> --file <path to requirements.txt>

The assignments cover a range of topics in the robotics domain,

## HW1 - Checkerboard camera calibration / Plane-to-plane homography
<img src="https://user-images.githubusercontent.com/102079385/208622372-5cb50ad5-c6b2-4728-b85c-cf6f7a7abb49.png" width=50% height=20%>

## HW2 - Interpolation
### 10Hz ground truth data
| ![image](https://user-images.githubusercontent.com/102079385/208623189-46e001fa-c39d-4e86-9fcd-0ec2296a4969.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208623226-3b00f2de-ec3a-41a3-b11b-bc2e1f434c2f.png) 	|
|------------------------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------	|
| ![image](https://user-images.githubusercontent.com/102079385/208623247-bd984195-cdcc-4c8b-9de7-d7a9674fb8ca.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208623471-5f20d83b-8f9f-404e-8b6b-b218acef330f.png) 	|

### 1Hz ground truth data
| ![image](https://user-images.githubusercontent.com/102079385/208623335-b56e8147-40a3-4538-8627-fe4df68338a0.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208623393-ef236357-830f-48d7-adf1-6eb961a509c8.png) 	|
|------------------------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------	|
| ![image](https://user-images.githubusercontent.com/102079385/208623437-739cd9c8-1eef-41d0-b8f0-d1300ffc6f97.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208623490-85b90d59-37d0-45fe-9c71-cdc5b9765fe6.png) 	|


## HW3 - ODE numerical solver and plane estimation using RANSAC
### ODE solution
| ![image](https://user-images.githubusercontent.com/102079385/208831313-5d293897-aed2-4c98-b354-c2c1d13db84a.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208831335-45743cc9-2baf-4e0f-a8a6-ff6038b99265.png) 	|
|------------------------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------	|
| ![image](https://user-images.githubusercontent.com/102079385/208831348-30d4ac58-d925-467e-b473-e92c0a564a7e.png) 	| ![image](https://user-images.githubusercontent.com/102079385/208831360-f6b78863-18f5-4408-b0a9-391ca0094ed9.png) 	|

| Type       	            | Error     |
|--------------------------	|:-----:    |
| Euler    	                |1.12E00 	|
| Runge-Kutta (4th order) 	|1.98E-2    |
| Richardson (n=10)     	|5.23E-3    |
| Richardson (n=100)     	|5.23E-5    |
| Richardson (n=1000)     	|5.23E-7    |

### Plane estimation from point cloud using RANSAC
![image](https://user-images.githubusercontent.com/102079385/208831656-386717b4-1a14-43e0-bd4b-293365d04f87.png)
![image](https://user-images.githubusercontent.com/102079385/208831671-8ef786f4-07c6-4ebc-a40b-50ceb642d8d8.png)
![image](https://user-images.githubusercontent.com/102079385/208831696-faebcaa5-6e60-4dd3-87aa-6884effa2dd4.png)
![image](https://user-images.githubusercontent.com/102079385/208831713-8b8ce717-b406-48dc-8c8f-d6ed65de2912.png)


## HW4 - Machine learning and numerical solver (Lotka-Volterra predator prey model)
### Machine learning (using dimensionality reduction) for traffic sign classification (Germnan Traffic Sign benchmark dataset)
![image](https://user-images.githubusercontent.com/102079385/208834095-e3e8d3bf-2cfd-40ee-9424-596a05a3a6c8.png)
![image](https://user-images.githubusercontent.com/102079385/208834116-d0366f42-1765-473a-8af8-5db544d07a67.png)
![image](https://user-images.githubusercontent.com/102079385/208834156-090c7eb7-08cd-468b-af22-19bbe742a084.png)
Correct | Incorrect classification on testing data = 84.22%, 15.78%
![image](https://user-images.githubusercontent.com/102079385/208834191-8acc7310-c48e-44f3-acc6-355d12b141ba.png)
Correct | Incorrect classification on testing data = 84.85%, 15.15%

| Reduction method    	| Correct 	| Incorrect 	|
|---------------------	|:-------:	|:---------:	|
| PCA (25)            	|   74%   	|    26%    	|
| PCA (50)            	|   84%   	|    16%    	|
| PCA (50) + LDA (25) 	|   85%   	|    15%    	|

### Lotka-Volterra predator prey model
![image](https://user-images.githubusercontent.com/102079385/208834359-e55f059f-e384-4693-93ab-63213b18dbba.png)
![image](https://user-images.githubusercontent.com/102079385/208834376-dffa4630-f6f4-4914-b1b0-dbb0eaa38a9f.png)
![image](https://user-images.githubusercontent.com/102079385/208834396-e13c2ff9-d1a9-4ab1-b1ef-5ed6815e1291.png)


## HW5 - Motion planning
### Environment
![image](https://user-images.githubusercontent.com/102079385/208834559-d4db9dbe-9167-48b8-97fe-e6d0aedd8db0.png)
### Configuration space (C-space)
![image](https://user-images.githubusercontent.com/102079385/208834578-fc14b2a4-97bd-4f26-a0f8-dc75828601a4.png)
### Shortest path
![image](https://user-images.githubusercontent.com/102079385/208834648-9faa9b8b-82dc-4fb8-8f3e-df2922c39800.png)
### Safest path using Voronoi diagrams
![image](https://user-images.githubusercontent.com/102079385/208834668-296f3d68-0792-4f6d-a23a-316cd86396bb.png)
![image](https://user-images.githubusercontent.com/102079385/208834678-5e7e97ed-f20c-4400-bab5-1d67251d940b.png)

### PRM (Probabilistic Roadmaps)
#### Changing $N_\text{samples}$, everything else constant
![image](https://user-images.githubusercontent.com/102079385/208834797-1c44b3e0-1fdc-4867-aa95-236cf331f584.png)

| $N_\text{samples}$ (with $k=25$)      | Path length (Euclidean units)	|
|---------------------	                |:-----------------------------:|
| 50            	                    |   722   	                    |
| 100            	                    |   654   	                    |
| 500            	                    |   638   	                    |

#### Changing $k_\text{nearest}$, everything else constant
![image](https://user-images.githubusercontent.com/102079385/208834895-8a4daf1c-4efe-4fdf-94c9-a13064c3dd71.png)

| $k$ (with $N_\text{samples}=1000$)    | Path length (Euclidean units)	|
|---------------------	                |:-----------------------------:|
| 15               	                    |   660   	                    |
| 25            	                    |   639   	                    |
| 35            	                    |   635   	                    |

### RRT (Rapidly exploring Random Trees)
![image](https://user-images.githubusercontent.com/102079385/208834998-11ce5ddf-019f-46d0-a684-648028fa2f9b.png)
| $N_\text{samples}$ 	| $\epsilon = 10$ 	| $\epsilon = 15$ 	| $\epsilon = 20$ 	|
|:------------------:	|:---------------:	|:---------------:	|:---------------:	|
|        1500        	|       739       	|       802       	|       914       	|
|        2000        	|       767       	|       797       	|       775       	|
|        2500        	|       759       	|       831       	|       804       	|

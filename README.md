<h1 align='center'> Students_Performance_In_Exams <h1>

**Implementing end to end machine learning project :)**


*************************************************************************************************************
## Complete Life Cycle Of ML Projects:
    * Understanding The Problem Statement
    * Data Collection
    * Exploratory Data Analysis (EDA)
    * Feature Engineering
    * Feature Selection
    * Model Creation
    * Model Hyperparameter Tunning
    * Deploy The Model
    * Retraining Approach
*************************************************************************************************************

## Steps

* create the env and activate
```bash
conda create -p ml2 python==3.8 -y
conda activate ml2/
```

create req.txt file and setup.py
```bash
touch requirements.txt setup.py
```

* create required dir and files
```
mkdir src src/components src/pipeline
mkdir notebooks

touch setup.py
touch src/__init__.py src/exception.py src/logger.py src/utils.py
touch src/components/__init__.py src/components/data_ingestion.py src/components/data_transformation.py src/components/model_trainer.py
touch src/pipeline/__init__.py src/pipeline/predict_pipeline.py src/pipeline/train_pipeline.py
```
**Note:** In Python, **setup.py** is a module used to build and distribute Python packages. It typically contains information about the package, such as its name, version, and dependencies, as well as instructions for building and installing the package. This information is used by the pip tool, which is a package manager for Python that allows users to install and manage Python packages from the command line. By running the setup.py file with the pip tool, you can build and distribute your Python package so that others can use it.

* create setup.py and add code to it 
```
touch setup.py
```

* add packages for installation to requirements.txt and run the below commands
```bash
pip install -r requirements.txt
```

**Note: when we use -e . inside req.txt, it automatically trigger setup.py**

**Note:** The python **sys module** contains methods and variables for modifying many elements of the Python Runtime Environment. It allows us to access parameters and functionalities specific to the system

**Note:** In Python, the **logging module** provides a flexible and configurable way to capture and output log messages from your application. The main purpose of using a logger is to record information that can help you debug issues, monitor the execution flow, and gather data for analysis.

* add code to logger.py and exception.py, finally test it.

* Getting the dataset, EDA, Feature Engineering, Model Training
* install teh jupyter notebook in VS Code
```bash
pip install jupyter
jupyter-lab
```

* to install some packages:
```bash
python3 -m pip install [package_name]
```

* Data ingestion part is completed

**Note:** The **utils.py** makes it easy to execute common tasks in Python scripts

* Data transformation is done successfully

* Model train is done!

* hyperparameter tunning is done!

### creating flask app and prediction pipeline


### Docker Setup in EC2

* Create a docker file
```bash
touch Dockerfile
```
* Build a docker image
```bash
docker build -t student-app .
docker ps
```
* Running the app
```bash
docker run -p 8000:8000 student-app
```

### AWS
* create IAM User
* Go for ECR and create a repository (060145207853.dkr.ecr.ap-south-1.amazonaws.com/student-performance)
* Go to EC2 and launch an instance

#### Docker Setup In EC2 commands to be Executed

**optinal**
```bash
sudo apt-get update 
sudo apt-get upgrade -y
```

**required**

```bash
curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
```

#### Configure EC2 as self-hosted runner:

* Setup github secrets:
```bash
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
AWS_ECR_LOGIN_URI
ECR_REPOSITORY_NAME
```
*************************************************************************************************************

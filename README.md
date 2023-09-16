# Machine-Learning-Project-Parkinson-Desease-Prediction
Repository for Machine Learning Project (Parkinson Desease Prediction) within Machine Learning course in the master's studies of the Faculty of Mathematics, Belgrade

Theme of the project is Parkinson Desease Prediction.

What is Parkinson and what causes Parkinson's disease? 
- Parkinson’s disease is a brain disorder that causes unintended or uncontrollable movements, such as shaking, stiffness, and difficulty with balance and coordination.
Symptoms usually begin gradually and worsen over time. As the disease progresses, people may have difficulty walking and talking. They may also have mental and behavioral changes, sleep problems, depression, memory difficulties, and fatigue. [Literature 1]

- The most prominent signs and symptoms of Parkinson’s disease occur when nerve cells in the basal ganglia, an area of the brain that controls movement, become impaired and/or die. Normally, these nerve cells, or neurons, produce an important brain chemical known as dopamine. When the neurons die or become impaired, they produce less dopamine, which causes the movement problems associated with the disease. Scientists still do not know what causes the neurons to die. [Literature 1]

Dataset used for this project is Oxford Parkinson's Disease Detection Dataset (https://archive.ics.uci.edu/dataset/174/parkinsons)

About this dataset:

The dataset was created by Max Little of the University of Oxford, in 
collaboration with the National Centre for Voice and Speech, Denver, 
Colorado, who recorded the speech signals. The original study published the 
feature extraction methods for general voice disorders.

This dataset is composed of a range of biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD). Each column in the table is a particular voice measure, and each row corresponds one of 195 voice recording from these individuals ("name" column). The main aim of the data is to discriminate healthy people from those with PD, according to "status" column which is set to 0 for healthy and 1 for PD. 

The data is in ASCII CSV format. The rows of the CSV file contain an instance corresponding to one voice recording. There are around six recordings per patient, the name of the patient is identified in the first column.

Dataset results collected and described in document 'Suitability of dysphonia measurements for telemonitoring of Parkinson's disease', IEEE Transactions on Biomedical Engineering
(Max A. Little, Patrick E. McSharry, Eric J. Hunter, Lorraine O. Ramig (2008)) [Literature 2]

Dataset's attributes informations:
    name - ASCII subject name and recording number
    MDVP:Fo(Hz) - Average vocal fundamental frequency
    MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
    MDVP:Flo(Hz) - Minimum vocal fundamental frequency
    MDVP:Jitter(%),MDVP:Jitter(Abs),MDVP:RAP,MDVP:PPQ,Jitter:DDP - Several 
    measures of variation in fundamental frequency
    MDVP:Shimmer,MDVP:Shimmer(dB),Shimmer:APQ3,Shimmer:APQ5,MDVP:APQ,Shimmer:DDA - Several measures of variation in amplitude
    NHR,HNR - Two measures of ratio of noise to tonal components in the voice
    status - Health status of the subject (one) - Parkinson's, (zero) - healthy
    RPDE,D2 - Two nonlinear dynamical complexity measures
    DFA - Signal fractal scaling exponent
    spread1,spread2,PPE - Three nonlinear measures of fundamental frequency variation 

Project Idea: 

The model can be used to differentiate healthy people from people having Parkinson’s disease.
The algorithm that is useful for this purpose is XGboost which stands for extreme gradient boosting, it is based on decision trees.

Due to the size of the dataset, I decided to build multiple models and compare their results.
Models that are used:<br />
&emsp;1. Logistic regression <br />
&emsp;2. XGBoost <br />
&emsp;3. KNearestNeighbors <br />
&emsp;4. ensamble BaggingClassifier (KNearestNeighbors) <br />
&emsp;5. DecisionTreeClassifier <br />

Jupyter notebook scripts are numbered for viewing order.

Team members of the project:
    1. Nikola Micic

Used literature:<br />
&emsp;1. https://www.nia.nih.gov/health/parkinsons-disease<br />
&emsp;2. https://ieeexplore.ieee.org/document/4636708<br />
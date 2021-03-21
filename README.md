# Automatic-Medical-reports-by-Using-Deep-Learning.
# Introduction :
In real world, we may encounter to analyze generating medical reports by observing x-rays, So this project will help us to understand generating reports automatically.

# Objective :
To build Web - App for generating report by using x-ray images.

# Data:
The data for this problem is provided by the Indiana University hospital network. The data contains two parts.
X-rays: http://academictorrents.com/details/5a3a439df24931f410fac269b87b050203d9467d
Reports: https://academictorrents.com/details/66450ba52ba3f83fbf82ef9c91f2bde0e845aba9

Zip file : 1.28GB
No of Images : 7174
Files : xml,png.

Dataset statistics :
Exratcing features from xml file having some tags like Impression,findings,Indication. Based on the tags, We used to collect reports for x-ray images.
we observed that one person may have couple of x-ray image,So by using the histogram, we concluded that we will going to use 2 x-ray per person id.
If person having only one image we will duplicating same image into image2. 
Finally created new csv file for modeling (datafinal.csv).
<img src="https://github.com/anant123-ai/Medical-Report-Generation-Using-Deep-Learning/blob/main/1_ZJ7IviuFk9P2Nj7YGhPoQQ.png">
<img src="https://github.com/anant123-ai/Medical-Report-Generation-Using-Deep-Learning/blob/main/1_ssDAFqny1fJXY15AuoufaA.png">

Data Fields Explanation

    Patient id : character
    image_1 : character
    image_2 : character
    report : text
    
# EDA Objective
Analysing the data & plot the required graphs to show that these conclusions are true:


# Model Building
    Model-1: We have used simple encoder and decoder model by using relu activation and tanh activation functiuons with Adam optimizer, got validation loss is very less(0.0014)
    Model-2:We have used additive attension mechanism with Bidirectional GRU; got validation loss score

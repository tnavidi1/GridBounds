# GridBounds

The code in this repository was used to simulate the experiments performed in the paper submitted by Thomas Navidi and Chloe Leblanc in 2020.  

Dependencies:  
Package         Version  
cvxpy           1.0.24     
matplotlib      3.1.1      
numpy           1.16.4     
pandas          0.24.2     
pip             19.0.3     
PYPOWER         5.1.4      
scikit-learn    0.21.2     
scipy           1.3.0      
statsmodels     0.10.0 


The large Pecan Street and NREL data sets used in the simulation have not been included in this repository   


To run enter commands:  

python EV_Profiles.py --evPen=5  
echo made EV profiles

python makeDemand.py --solarPen=5 --storagePen=1 --evPen=5  
echo made demand files

python pypowerTest.py --Qcap=-0.79 --solarPen=5 --storagePen=0 --final=0  
echo simulated voltages for training data

python SVR_code.py --train=1 --solarPen=5 --storagePen=0  
echo trained SVR models

python BoundsOptimization.py --solarPen=5 --storagePen=1 --evPen=5 --bounds=1  
echo ran simulation

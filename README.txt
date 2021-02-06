---------------------------------------------------------------------------|

Deep learning framework for geological symbol detection on geological maps 
                                                                          
How to use the datasets:                                                   
                                                                           
    Datasets used for the experiments articulated in the paper have been   
provided and located in paths ./SSDN_DATASET and ./DAGCN_DATASET.         
                                                                          
    Please unzip the related dataset zip files and modify parameters of the
dataset root paths set in ./SSDN/train.py, ./DAGCN/train_DAGCN.py, and     
./DAGCN/train_Other_GCNN.py according to your device. Then, the code can be
run directly.                                                              
                                                                           
    Note that, using DAGCN_DATASET/DatasetProcess/Dizhitu_graph/Process/   
data.zip->Dizhitu_graph_2_for_Paper2_1_added_EXP_Chg_1 as an example, the  
documents named in this format are referred to the experiments mentioned in
Section 5.2, where `Chg` is the compound symbol name and the `1` denotes   
the number of the `Chg` existing in the modified dataset.                 
																		   
	Please use `labelme` (a site package of python) to visualize the raw   
datasets (see ./SSDN_DATASET_RAW and ./DAGCN_DATASET_RAW). The interpretation 
of the marks for `DAGCN_DATASET_RAW` is located in the APPENDIX B of this file. 																   
                                                                           
How to use the codes:                                                      
                                                                          
    The codes in this repository are all python codes and can be run by    
Pycharm directly. Please see the following guide for further operations    
and correct the path(s) according to your own device(s), when you run any  
python files.                                                              
                                                                           
Single Symbol Detection Network:                                           
                                                                           
    Run ./SSDN/train.py to train the model. Run ./SSDN/train_see_results   
.py to see the training result. Please modify the class Config in the      
above-mentioned files in accordance with your purpose.                     
                                                                           
Distance-Attention Graph Convolutional Network:                            
                                                                           
    Run ./DAGCN/train_DAGCN.py to train the model. Run ./DAGCN/train_Other 
_GCNN.py to train other GCN models. Training and testing results will be   
recorded automatically by local files. Please modify the parameters in the 
related python files to control the network structure.                     
                                                                           
    Thank you for your reading!                                            
---------------------------------------------------------------------------|

---------------------------------------------------------------------------|
APPENDIX A: PYTHON ENVIRONMENT					     				       
																		   
python 3.6.3											  				   
																		   
																		   
APPENDIX PYTHON Site-packages											   
																		   
albumentations            0.4.3											   
apex                      0.1											   
Cython                    0.29.14										   
labelme                   4.5.7											   
matplotlib                3.3.1											   
numpy                     1.18.1										   
opencv-contrib-python     4.1.2.30										   
opencv-python-headless    4.1.2.30										   
scikit-image              0.16.2										   
torch                     1.1.0											   
torch-geometric           1.4.2											   
torch-scatter             1.2.0											   
torch-sparse              0.4.0											   
torchvision               0.2.1											   
---------------------------------------------------------------------------|


---------------------------------------------------------------------------|
																		   
APPENDIX B: 															   
{																		   
            '0': "background_class",									   
            "a01": "ArFai",												   
            "a10": "ArHggv",											   
            "a1": "Ar2SggyDeltaO",										   
            "a12": "Ar2SHggyDeltaO",									   
            "a13": "Ar2WggvDelta",										   
            "a20": "Ar3FN",												   
            "a201": "Ar3CN",											   
            "a2": "Ar3Ggg",												   
            "a21": "Ar3JggyDelta",										   
            "a22": "Ar3Kggyo",											   
            "a23": "Ar3Qgg",											   
            "Ce1": "Cent1+2",											   
            "5": "Cent2m+zh",										       
            "6": "Cent3chm",											   
            "c": "Cent1ch",												   
            "c00": "Ch",												   
            "c1": "Chg",												   
            "c2": "Chd",												   
            "c21": "Chd+g",												   
            "c30": "Chch",												   
            "c30t": "Chch-t ",											   
            "c31": "Chchl-d",											   
            "c32": "Chchl+t",											   
            "c3": "Chch+chl",											   
            "c4": "Cht+d",												   
            "c41": "Cht",												   
            "E": "Exl",								    				   
            "7": "Jxw",									    			   
            "J": "Jxh",										    		   
            "t": "Jxt",											    	   
            "j2": "J2j",												   
            "j21": "J2l",												   
            "y": "J3t",												       
            "y1": "J3tch",												   
            "2": "J3shh",												   
            "f0": "J3dsh",												  
            "f": "J3fsh",												   
            "f1": "J3shy",												   
            "g1": "J3lch",												   
            "g2": "J3tp",												   
            "g21": "J3xj",												  
            "g22": "Jxy",												   
            "g3": "J3au",												   
            "g31": "J3EfecilongPai",									   
            "g4": "J3zh",												   
            "1": "K1xsh",												   
            "3": "K1hsh",												   
            "31": "K1shch",												   
            "9": "K1dj",												   
            "k1": "K1jx",												   
            "k2": "K1tl",												  
            "k3": "K1ym",												   
            "n1": "Nql",												   
            "pt2": "Pt2Shd",											   
            "pt3": "Pt2dy",												   
            "4": "Qbl+j",												   
            "jey": "Qbj",												   
            "lsz": "Qbl",												   
            "8": "Qbx",													   
            "q1": "Qhpl",												   
            "q11": "Qhpal",												   
            "q12": "Qhal",												   
            "qp2": "Qp2Zh",												   
            "qpm1": "Qp3mpal",											   
            "qpm2": "Qp3mpl",											   
            "qpm3": "Qp3m",												   
            "qpm4": "Qp3mdl",											   
            "GuJ": "EBetaMiu",										   	   
            "Tq1": "TqbDeltaMiu",										   
            "Tz1": "TzhwyPai",											   
}															   			   
																		   
---------------------------------------------------------------------------|
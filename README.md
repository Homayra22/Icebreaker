# Icebreaker
Team Goal: Prediction of  Greenland ice bed topography 

Dataset: This dataset contains information on Greenalnd Icebed Topography. It has 5 features. They are 'surf_SMB', 'surf_dhdt', 
'surf_elv', 'surf_vx' and 'surf_vy'. Some preprocessing activities are carried out 
to prepare the training and testing dataset. [To find corresponding pixel in input grids  The features have 1201*1201 dimension. 



Input data: 2D grids (150 m resolution, HDF5 format)
Ice surface elevation [m] (surf_elv)
Ice flow velocity vectors [m/yr] (surf_vx, surf_vy)
Ice thinning rates [m/yr] (surf_dhdt )
Snow accumulation [m/yr] (surf_SMB)

Coordinates of cell centers [m]: surf_x, surf_y

Training set: 1D flight line data (along lines)
track_bed_training
1st column: x [m]
2nd column: y [m]
3rd column: bed height [m]
For each point (x,y)
The corresponding pixel in input grids 
Prepare input data
Infer bed height
Compare to measured bed height

Testing set: 1D flight line data not used in training set
track_bed_testing
1st column: x [m]
2nd column: y [m]



Approach: Regression analysis is used to predict the icebed topography.  The model is evaluated using the RMSE score.




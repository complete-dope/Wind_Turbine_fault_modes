# Wind Turbine Fault Modes Classification 

We conducted an analysis on data obtained from the Supervisory Control and Data Acquisition (SCADA) system of a wind turbine from April 2014 to April 2015, along with associated faults that occurred during operation. The SCADA system provides over 60 records of all wind turbine components such as the nacelle, inverter, bearing, and others. There were five identified fault modes, labeled FF, AF, EF, MF, and GF. We found a significant increase in the number of faults in October 2014.

During the faulty times, the wind turbine components exhibited anomalous behavior. For instance, during GF, the temperatures of all wind turbine components were lower than normal, while during AF and EF, the temperatures were higher. Also, reactive power was anomalously high during EF, while power was lower during MF. Thus, we were able to classify fault modes based on various SCADA measured components.

To classify the fault modes, we developed an Adaptive Boosting (AdaBoost) based predictive model. However, the data was largely imbalanced among fault modes, so we implemented SMOTE within a 5-fold CV pipeline. With this approach, we obtained a macro F1 score of 64-65%, with two problematic classes, EF and FF, being falsely predicted. To improve the model performance, we performed hyperparameter tuning on four AdaBoost hyperparameters. After tuning, the macro F1 score improved to 69-70%, and the number of false predictions for EF classes successfully reduced.


## The F1 score is 70% 

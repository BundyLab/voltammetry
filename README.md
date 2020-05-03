# voltammetry
cobalt voltammetry code

This code integrates Co peaks generated from the NOVA 1.8 software. 
Text files of the data output from NOVA 1.8 software can be saved automatically from each scan, and this code is then used to 
determine peak areas. The signal is first smoothed using the Savitzky-Golay smoothing function (span 5, degree 3), and then the first 
derivative of the voltammetric signal between -1.4 and -1.1 V is calculated in order to find the start and end of the Co(DMG)2 peak. 
The baseline is then drawn and linearly interpolated between the start and the end of the peak. The final peak height is determined 
by finding the maximum of the signal and subtracting it from the baseline. Peak heights from the “zero addition” scans are then plotted 
along with the standard additions, and a linear regression is computed from all seven scans.

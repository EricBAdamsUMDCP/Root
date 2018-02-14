# Root
A log of code and notes for using root in the Mignerey lab
EM = electromagnetic
HAD= Hadronic
  1, 2, 3, 4
 RPD= Reaction Plane Detector have 2 of them
    1-16
Have 2 detectors
have a positive and a negative side
neg has RPD
pos has the HAD and EM (PHAD) and (PEM)
DEAD RPD 10,
Not connected EM 1, 2, 4, 5
Each channel has 10 histrograms thats why have e.g. posEM3fC[10]. 
TIME SLICES have 0 - 10 can have a signal in a few time slices but have a peak in one of ten. Times slices are 25 ns wide.
ADC = analog to digital converter
Phototube collects charge -> convert ADC-> fempto coulombs (fc). Uses a log like scale. Get lines in neutron spectra when switching between algorithims
ADC= 127 is saturation becaause it is 8 bit. (ADC tells us about our saturation)
* ADC=127 is maximum possible signal measurement but signal in reality may be higher!!!
USE fc to get the signals out
We use multiple time slots to deal with saturation as the thing gets saturated we switch to the next time slot and get the bleed off (its like a ccd).

Always Initialize variables otherwise it may not work!
e.g.
 Double_t         centrality[1];

  Double_t 		   HADsum=0;
  Double_t		   PEMsum=0;
  Double_t		   RPDsum=0;
  Double_t         ETsum = 0;
  Double_t		   NEMsum = 0;
  Double_t		   NHADsum = 0;
  Double_t		   PHADsum = 0;

Time slices that have no data in them are used for NOISE Subtraction e.g. 0-2

The commands used to set fc values to greater than zero are used after noise compensation/subtraction so no negative values are made by accident

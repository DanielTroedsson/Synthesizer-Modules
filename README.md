# Synthesizer-Modules

//  BIQUAD LOWPASS FILTER / DIRECT FORM 1 - DANIEL TROEDSSON 18/12-2024
//  -------------------------------------------------------------------

//  Implementable low-pass biquad filter with frequency cutoff and Q-factor as parameters. Cutoff value range is between 0 and Nyquist frequency. 
//  while Q-factor is considered a Q18.14 FP-number and has a value range of 11583-163840 corresponding to a attenuation of -3dB to 20dB at the cutoff frequency. 

//  The filter should be implemented according to the following difference equation:
//  y[n] = (b0 * x[n]) + (b1 * x[n-1]) + (b2 * x[n-2]) - (a1 * y[n-1]) - (a2 * y[n-2])

//  Note that all filter coefficiants have been normalized, thus we only have five coefficiants. 
//  Filter coefficiants are calculated as Q16.16 FP and this needs to be considered through the filtering process. 

//  Call the get_filter_coefficiants function with the desired cutoff and Q-factor value as arguments to recieve your filter struct
//  containing the corresponding filter coefficiants.

//  -----------------------------------------------------------------------------------------------------------------------------
//  Many thanks to RBJ and his article "Cookbook formulae for audio EQ biquad filter coefficients" which this code is based upon. 
//  -----------------------------------------------------------------------------------------------------------------------------


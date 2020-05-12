# Strong-Grainlet-Synthesis
A Max/MSP experiment combining trainlet synthesis and karplus-strong
The patch is an experiment starting from Maurizio Giri's asynchronic trainlet implementation on Max/MSP. 
Therefore some external object from his library are required to make the patch work properly.

This synthesis technique is an attempt to experiment the behaviour of karplus-strong physical model in the particle domain.
Grainlets are fed into the karplus strong algorithm instead of note-based triggers. 
Parameters: 
rate of metro (generation of grainlets) + percentage of variation 
duration of grainlets + percentage of variation per grainlet
frequency of grains for each grainlet + percentage of variation per grainlet
frequency of resonance of the karplus strong + percentage of variation per grainlet
minimum and maximum value of karplus strong feedback 
stereo width in percentage
shape of grain envelope (gaussian, quasi-gaussian, expodec, rexpodec, etc.)

TODO: 
• implement a different way to generate clicks, allowing for spectral variations in the karplus strong trigger input
• try envelopes for each grainlet cloud
• improve the response of the algorithm on low range of the spectrum 
• try a bank of resonant filters as further processing after the algorithm,
  relating the frequency of resonance of the karplus strong to the frequency of resonance of the whole cloud;
  possibly allowing glissandi during the cloud envelope 
• try a reverb algorithm inside the poly~ changing parameters at each grainlet 

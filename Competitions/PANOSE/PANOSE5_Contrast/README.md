# PANOSE Contrast Competition

The purpose of this competition is to develop algorithms that can predict the PANOSE Contrast classification from an image of a letter. The training, testing and validation data consist of letters classified by the type designer. Not all type designers spend time classifying their typeface. Sometimes type designers classify some aspects of their typeface such as Serif Style or Proportion but not Contrast in which case the values of 0 or 1 are associated with the Contrast.  For that reason only letters with the PANOSE 5 Contrast values of 2 through 9 were included in these data.  

Accurate algorithmic tools to do this task would assist type designers and allow the thousands of typefaces that are unclassified to be accurately classified.  This project is part of the larger Cognitive Type <a href="http://cognitivetype.org/">CognitiveType.org</a> and <a href='http://warhol.ai/'>Warhol.ai</a> projects whose purpose is to create computational tools to assist designers and artists.  


## What is PANOSE Contrast?

By "contrast", we mean the difference between the widths of thick and thin strokes.

0: any contrast  
1: no fit  
2: no contrast  
3: very low    
4: low   
5: medium low  
6: medium   
7: medium high   
8: high   
9: very high   

<img src='https://github.com/nikbearbrown/Kaggle/blob/main/Art/PANOSE_5_Contrast_A.png?raw=true' />


Contrast is measured from the single letter 'O' of a given font:    

<img src='https://github.com/nikbearbrown/Kaggle/blob/main/Art/PANOSE_5_Contrast_B.png?raw=true' />


If a and b are the maximum widths (calculated perpendicularly to the stroke's "midline") and c and d are the minimum widths, then the contrast κ is equal to κ = min(c,d)/max(a,b).  


The continuous parameter's values are grouped into classes according to the thresholds below:

2: no contrast, if κ > 0.8    
3: very low, if 0.65 < κ ≤ 0.8   
4: low, if 0.48 < κ ≤ 0.65    
5: medium low, if 0.3 < κ ≤ 0.48   
6: medium, if 0.2 < κ ≤ 0.3     
7: medium high, if 0.15 < κ ≤ 0.2  
8: high, if 0.08 < κ ≤ 0.15   
9: very high, if κ ≤ 0.08  


References:

Haralambous, Yannis (2007) Fonts & Encodings _O'Reilly Media_ https://learning.oreilly.com/library/view/fonts-encodings/9780596102425/   

Coles, Stephen (2012) The Anatomy of Type _Harper Design_ https://typeanatomy.com 

Schulz, Florian (2017) The Anatomy of a Thousand Typefaces https://medium.com/@getflourish/the-anatomy-of-a-thousand-typefaces-f7b9088eed1   





 # SRAM ( Description of 1-bit storage cell)
 
 The project is a description of all the necessary components used in making 1-bit 6T-SRAM cell and their analysis using the tool ESIM.
 
 ## Contents
 
 ## Definition
 SRAM (Static Random Access Memory)
 
 It is a random access memory that has a access time independent of the physical location of the data.
 
 The main components are:-
 - Bitcell	 
 - Sense Amplifier
 - Write Driver
 - Precharge circuit
 
 ## Modes of Operation
 
 ### Standby Mode/ Hold Mode
 
 The word line is not active and the bitcell will retain the value.
 
 ### Read Mode 
 Intially the bit line and bit bar line is precharged to Vdd.The word line is made active and bit line or bit line bar changes value according to the values present at q & qb.Sense amplifier senses the values at bl & blb and produced the desired output.
 
 ### Write Mode
 The bl & blb are precharged to Vdd. Whatever value we want to write into the cell should be present at bl. Using write drive we make bl/blb ,0/1.  
 
 
 ## Advantage of SRAM over DRAM
 
 Faster because periodic refreshing is not required.
 
 ## Disadvantage of SRAM over DRAM 
 
 - Uses more power 
 - Required larger area.
 
 ## Bitcell

 
![bitcell](https://user-images.githubusercontent.com/69419719/89906113-996b0c00-dc08-11ea-8896-fc0470bd273f.PNG)

 Below are the circuits and curves for hold , read and write case without feedback connections.
 
 
 
 ### Read Curve
 
 ![read_cir_curve](https://user-images.githubusercontent.com/69419719/89909295-89edc200-dc0c-11ea-9f9a-d806897353f2.PNG)
 
 ### Write Curve
 
 ![write_cir _curve](https://user-images.githubusercontent.com/69419719/89909305-8c501c00-dc0c-11ea-8db6-184161ff8110.PNG)
 
 
 ## Precharge Circuit
 ![precharge](https://user-images.githubusercontent.com/69419719/89909294-89edc200-dc0c-11ea-8f4b-48fff17b5cbb.PNG)
 
 
 ## Sense Amplifier
 ## Write Driver
 ![write_driver](https://user-images.githubusercontent.com/69419719/89909307-8c501c00-dc0c-11ea-8ef9-d22f875c1ce1.PNG)
 
 
 ## Trigate 
 
 ![trigate](https://user-images.githubusercontent.com/69419719/89909302-8bb78580-dc0c-11ea-86f3-6abc316a718f.PNG)
 
##### Waveform

![in in_iv](https://user-images.githubusercontent.com/69419719/89972403-6746c200-dc7b-11ea-8578-c7bffbfbd2ae.PNG)
![en enb](https://user-images.githubusercontent.com/69419719/89972401-66159500-dc7b-11ea-969c-4ba89dabdd96.PNG)
![out](https://user-images.githubusercontent.com/69419719/89972405-67df5880-dc7b-11ea-861e-766465236cd5.PNG)

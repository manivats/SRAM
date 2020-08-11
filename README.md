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
 ![bitcell](https://user-images.githubusercontent.com/69419719/89881164-bf7db580-dbe2-11ea-8673-a803f829fabc.PNG)
 
 Below are the circuits and curves for hold , read and write case without feedback connections.
 
 

 
 ## Precharge Circuit
 ## Sense Amplifier
 ## Write Driver

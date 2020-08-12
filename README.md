 # SRAM ( Description of 1-bit storage cell)
 
 The project is a description of all the necessary components used in making 1-bit 6T-SRAM cell and their analysis using the tool ESIM.
 
 ## Contents
 - [Definition](https://github.com/manivats/SRAM-/edit/master/README.md)
 - [Bitcell](https://github.com/manivats/SRAM-/edit/master/README.md)
 - [Precharge Circuit](https://github.com/manivats/SRAM-/edit/master/README.md)
 - [Sense Amplifier](https://github.com/manivats/SRAM-/edit/master/README.md)
 - [Write Driver](https://github.com/manivats/SRAM-/edit/master/README.md)
 - [Trigate](https://github.com/manivats/SRAM-/edit/master/README.md) 
 - [Read operation](https://github.com/manivats/SRAM-/edit/master/README.md)
 
 
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
 
 ### Hold Mode
 
 ![hold_cir](https://user-images.githubusercontent.com/69419719/89983647-8a7e6b00-dc95-11ea-91e1-c7b83f5f962e.PNG)


Type the following command in the `ngspice window`
``` html
plot qb vs q q vs q1
```
![hold_curve](https://user-images.githubusercontent.com/69419719/89974244-1daca600-dc80-11ea-9a4b-7400266d459d.PNG)

 ### Read Mode
 
 ![read_cir_curve](https://user-images.githubusercontent.com/69419719/89909295-89edc200-dc0c-11ea-9f9a-d806897353f2.PNG)
 
 Type the following command in the `ngspice window`
``` html
plot qb vs q q vs q1
```
 ![read_curve](https://user-images.githubusercontent.com/69419719/89974247-1f766980-dc80-11ea-848b-42c2e3538698.PNG)
 
 ### Write Mode
 
 ![write_cir _curve](https://user-images.githubusercontent.com/69419719/89909305-8c501c00-dc0c-11ea-8db6-184161ff8110.PNG)
 
 Type the following command in the `ngspice window`
``` html
plot qb vs q q vs q1
``` 
 ![write curve](https://user-images.githubusercontent.com/69419719/89974250-200f0000-dc80-11ea-93c6-528ad29c0cb9.PNG)
 
 ### SNM calculated table
 
 | NMOS | PMOS | ACCESS | HOLD SNM | READ SNM |
 | --- | --- | --- | ---| --- |
 | 0.44u | 0.28u | 0.35u | 0.6v | 0.3v |
 | 0.44u | 0.88u | 0.35u | 0.75v | 0.36v |
 | 0.7u | 0.35u | 0.35u | 0.61v | 0.35v | 
 | 0.36u | 0.9u | 0.27u | 0.6v | 0.4v |
 | 1.20u | 0.66u | 0.60u | 0.62v | 0.38v |
 
 ## Precharge Circuit
 ![precharge](https://user-images.githubusercontent.com/69419719/89909294-89edc200-dc0c-11ea-8f4b-48fff17b5cbb.PNG)
 ![pr_en](https://user-images.githubusercontent.com/69419719/90015857-cbdb3e80-dcc6-11ea-8c53-51c1a65f08ca.PNG)
 ![bl](https://user-images.githubusercontent.com/69419719/90015848-caaa1180-dcc6-11ea-806f-c7c54e6ffa86.PNG)
 ![blb](https://user-images.githubusercontent.com/69419719/90015851-cb42a800-dcc6-11ea-98f7-c033d9de7f04.PNG)
 
 
 ## Sense Amplifier
 ![sense_amp](https://user-images.githubusercontent.com/69419719/90015170-de08ad00-dcc5-11ea-8919-000ffcd64db9.PNG)
 
 ![bl_blb](https://user-images.githubusercontent.com/69419719/90009086-0e971980-dcbb-11ea-8f0d-e65747a38063.PNG)
 ![en](https://user-images.githubusercontent.com/69419719/90009087-0f2fb000-dcbb-11ea-9a5e-39a8b849e9b0.PNG)
 ![q1_qb1](https://user-images.githubusercontent.com/69419719/90009082-0ccd5600-dcbb-11ea-8ee8-53610a054c23.PNG)
 
 
 ## Write Driver
 ![write_driver](https://user-images.githubusercontent.com/69419719/89909307-8c501c00-dc0c-11ea-8ef9-d22f875c1ce1.PNG)
 
 ![din_dinb](https://user-images.githubusercontent.com/69419719/90015385-29bb5680-dcc6-11ea-94db-4ecc9c3a5e58.PNG)
 ![bbl bblb](https://user-images.githubusercontent.com/69419719/90015378-288a2980-dcc6-11ea-8cd3-ca3cb1796cea.PNG)
 ![pr_en](https://user-images.githubusercontent.com/69419719/90015386-2a53ed00-dcc6-11ea-8728-20b5f71cf297.PNG)
 ![bl_blb](https://user-images.githubusercontent.com/69419719/90015381-2922c000-dcc6-11ea-9705-7ea55b53599e.PNG)
 
 ## Trigate 
 
 ![trigate](https://user-images.githubusercontent.com/69419719/89909302-8bb78580-dc0c-11ea-86f3-6abc316a718f.PNG)
 
![in in_iv](https://user-images.githubusercontent.com/69419719/89972403-6746c200-dc7b-11ea-8578-c7bffbfbd2ae.PNG)
![en enb](https://user-images.githubusercontent.com/69419719/89972401-66159500-dc7b-11ea-969c-4ba89dabdd96.PNG)
![out](https://user-images.githubusercontent.com/69419719/89972405-67df5880-dc7b-11ea-861e-766465236cd5.PNG)

### Read Operation

![1half_read](https://user-images.githubusercontent.com/69419719/90018622-d5ff3c00-dcca-11ea-8ce3-e903534c6029.PNG)
![2half_read](https://user-images.githubusercontent.com/69419719/90018617-d4ce0f00-dcca-11ea-9581-38bc5353a5ee.PNG)
 
 ![wl pr_en](https://user-images.githubusercontent.com/69419719/89995643-5ca22200-dca7-11ea-927e-1817bb162570.PNG)
 ![q qb](https://user-images.githubusercontent.com/69419719/89995637-5b70f500-dca7-11ea-8119-90072cc0f241.PNG)
 
![bl_blb](https://user-images.githubusercontent.com/69419719/89995628-5a3fc800-dca7-11ea-8579-f182a5a2799e.PNG)
![en](https://user-images.githubusercontent.com/69419719/89995636-5ad85e80-dca7-11ea-92b8-457668c970f0.PNG)
![q1 qb1](https://user-images.githubusercontent.com/69419719/89995639-5c098b80-dca7-11ea-903c-19cd5933158f.PNG)


# Contributors
- Manisha Vats
- Kunal Ghosh
- Philipp Gühring

# Contact Information
- Manisha Vats, M.Tech(VLSI Design),CDAC,Noida vatsm1105@gmail.com
- Kunal Ghosh, Director, VSD Corp. Pvt. Ltd. kunalghosh@gmail.com
- Philipp Gühring, Software Architect, LibreSilicon Assocation pg@futureware.at


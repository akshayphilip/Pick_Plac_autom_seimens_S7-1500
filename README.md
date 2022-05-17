# Pick_Plac_autom_siemens_S7-1500

In this automation, i have designed the wrote programme using siemens S7 and the Plc used S7 1500, for the visual HMI i have use TIA, the main objective is programme is that completed parts are fed along a conveyor that leads to a weight check station. The part is weighed and 
then either picked up or rejected. If the weight is in the 
appropriate range, a Pick and Place unit will pick up the part 
and place it into a case for shipping. The pick and place is 
equipped with a vacuum gripper that will carry the part to 
the case. If the weight is outside the appropriate range, the 
conveyor is tipped and the part slides into a reject bin.

## Table of contents
1. [Demonstration link](#demonstration-link)
1. [system control](#system-control)
1. [pick and place control](#pick-and-place-control)
1. [production statistics](#production-stats)
1. [weight check station](#weight-check-station)
1. [faults](#faults)



### Demonstration link
[![youtube link](https://github.com/akshayphilip/Pick_Plac_autom_seimens_S7-1500/blob/master/Screenshot%202022-05-17%20131050.png)](https://www.youtube.com/watch?v=eO4HlRVqijs&t=6s&ab_channel=AkshayPhilip)

### System Control 
In the system control functional block , we write a programme to start , stop , MCR active and cycle active condition, here start PB is sealed with the start light output , and also run the conveyor when cycle is active snap of the rung is given below

### Pick and place control
For me this is most important fucntional block of the entire project, where the entire movement of solenoid , conveyor and pick and place  and the gripper is controlled, inshort entire sensor and actuators are controlled, intially we check the weight of the part a decide that the part should go to the reject bin or not , if the part is in the range the plc will detect the position of the part and use a gripper to take hold of the part, then solenoid retracts and another solenoid extends and final solenoid retract and gripper will relase and place the part at the desired position , who solenoid arms returns back to normal postion for the next part, i know i made little complex if there is any doubt contact me , link is provided in the contact session

### production stats
In this fuctional block i have use various counters and timers to get the production stats

* calculated the number of good parts
* noted cycle time of the gripper complete the one process
* Calculated total number of bad parts
* process time of the part

i have provided the snap of the logic below it

### Weight check station
In this station we check the weight of product form the analog data, first covert the data from analog signal to weight in Gms using a compute function and displayed in HMI, since analog data is varying so we wrote logic to obtian and save the maximum weight and displayed in HMI, using a limt function i have stored values in range to bool tag

### Faults
In this block i have used a timer to identify a faults , if there is any display to an indicator, snaps of the rung is given below


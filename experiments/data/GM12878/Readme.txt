**********************************************************************************
Author: Oluwatosin Oluwadare (oeow39@mail.missouri.edu)

Message to Users:
Please cite this work when you use this data in your research. Thanks
**********************************************************************************


## Normalization ##

The Abbreviation for the normalization technique used to nomalize data.
+---------------+-----------------------------------+
| Abbreviation  | Normalization Technique full Name |
+---------------+-----------------------------------+
| VC            | Vanilla Coverage                  |
+---------------+-----------------------------------+
| Yaffe_Tanay   | Yaffe and Tanay                   |
+---------------+-----------------------------------+
| KR            | Knight-Ruiz                       |
+---------------+-----------------------------------+

## About Directory and Files ##

1) Files in any Directory named with one of the normalization technique Abbreviation (VC, KR,Yaffe_Tanay) signifies that they have been normalized using that technique.
2) When a directory has format VC_100kb, VC_1mb, KR_1mb e.t.c. This signifies that the dataset is presented in more than one resolution. The Resolution is attached, like VC_1mb, to differentiate
the dataset for each Resolution. 
3) Files not in any of the normalization technique Abbreviation Directory are unnormalized. 

## Algorithms Input ##

For each algorithm, the contact matrix input format they accept and the input file name extension/suffix used for the 3D structure Construction are as follow:

+--------------+-----------------------------------------------------------------------------------+----------------------------+
| Algorithm    | Input Format                                                                      | GSDB Input filename suffix |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| LorDG        | 3-column Matrix                                                                   | _list.txt                  |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| 3DMax        | 3-column Matrix                                                                   | _list.txt                  |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| MOGEN        | 3-column Matrix                                                                   | _list.txt                  |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| Pastis       | 3-column Matrix(bin1,bin2,IF) and mapping coordinate(chr, start_pos,end_pos, bin) | .n_contact, .cbins         |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| Chromosome3D | n x n Square Matrix                                                               | _matrix.txt                |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| HSA          | 2-column bin positon with n x n Square Matrix                                     | _HSA.txt                   |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| miniMDS      | Chromosome,positon,IF(chr,start_pos1,end_pos1,chr, start_pos2,end_pos2,IF)        | .bed                       |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| ShRec3D      | n x n Square Matrix                                                               | _matrix.txt                |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| GEM          | 2-column bin positon with n x n Square Matrix                                     | _HSA.txt                   |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| ChromSDE     | 3-column Matrix and mapping coordinate                                            | .n_contact, .cbins         |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| SIMBA3D      | n x n Square Matrix                                                               | .npy                       |
+--------------+-----------------------------------------------------------------------------------+----------------------------+
| InfMod3DGen  | n x n Square Matrix                                                               | _matrix.txt                |
+--------------+-----------------------------------------------------------------------------------+----------------------------+

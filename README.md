# Finite Element Library Project (ELFI)

Mini finite element library made as part of the CSM master 1 at the university of Rennes.

## Project Architecture

**The documentation of each function** is found in the header associated with it (each folder contains a header declaring the functions found in it).

Each TP is associated with a main file that implements the functions produced.

Compilation and execution must be done in the "Executables/" folder.
Simply run the associated .sh file, then the resulting .exe.

The project is carried out in 5 phases.

### Phase 1 : Geometric Pre-processing

TP1 : Construction of the triangulation

- Discretization of the domain $\Omega$ into triangles ($P_1$) or quadrangles ($Q_1$).
- Assignment of references for the boundary conditions.

Functions produced :

- maillage : Creates - from the bounds defining the domain, the number of points on the sides, the type of elements to build and the 5 reference numbers - a mesh file
- lecfima : Reads a mesh file and fills in the associated variables in the program
- etiqAr :

### Phase 2

TP2a : Utility procedures for elementary computations

The files that were produced as part of this TP are in the folder "2a_ElementaireA/".

TP2b : Elementary computations

The files that were produced as part of this TP are in the folder "2b_ElementaireB/".

### Phase 3

TP3 : Assembly
Construction of the linear system.

### Phase 4

TP4 : Linear System & Project
Taking Dirichlet boundary conditions into account.

### Phase 5

TP5 : putting into practice
Solving and Post-Processing
Analysis of the results and writing of a report

#### Computation of the functions

Computation of $F_{\Omega}$ :

## List of files of which we are not the original authors

- alloctab.c
- freetab.c
- impcalel.c
- ww.c
- assmat.f (Fortran)
- affsmd.f (Fortran)
- cdesse.f (Fortran)
- tri.f    (Fortran)
- affsmo.f (Fortran)
- forfun.h (Fortran)
- affsol.f (Fortran)
- dsmoapr.o
- impmpr.f (Fortran)
- ltlpr.f  (Fortran)
- rsprl.f  (Fortran)
- rspru.f  (Fortran)
- solex.c

## Project structure

```text
├── 1_Maillage
│   ├── etiqAr.c
│   ├── lecfima.c
│   ├── maillage.c
│   ├── maillage.h
│   ├── main1.c
│   └── modeSaisie2.c
├── 2a_ElementaireA
│   ├── elementairesa.h
│   ├── fct_elementairesa.c
│   └── main2a.c
├── 2b_ElementaireB
│   ├── adwdw.c
│   ├── cal1Elem.c
│   ├── elementairesb.h
│   ├── fct_def_pb.c
│   ├── impcalel.c
│   ├── intAret.c
│   ├── intElem.c
│   ├── main2b.c
│   ├── w.c
│   └── ww.c
├── 3_Assemblage
│   ├── affsmd.f
│   ├── affsmd.o
│   ├── assemblage.c
│   ├── assemblage.h
│   ├── assmat.f
│   ├── assmat.o
│   ├── main3.c
│   └── READMEtp3
├── 4_Construction_SL
│   ├── affsmo.f
│   ├── affsmo.o
│   ├── cdesse.f
│   ├── cdesse.o
│   ├── construction_SL.h
│   ├── dSMDaSMO.c
│   ├── main4.c
│   ├── tri.f
│   └── tri.o
├── 5_Resol_Post-Trait
│   ├── affsol.f
│   ├── affsol.o
│   ├── CalSol.c
│   ├── dSMOaPR.c
│   ├── dsmoapr.h
│   ├── dsmoapr.o
│   ├── impmpr.f
│   ├── impmpr.o
│   ├── ltlpr.f
│   ├── ltlpr.o
│   ├── main5Test.c
│   ├── ResolSyst.c
│   ├── rsprl.f
│   ├── rsprl.o
│   ├── rspru.f
│   ├── rspru.o
│   └── solex.c
├── Donnees_1
│   ├── car1x1q_4
│   ├── car1x1t_1
│   ├── car1x1t_4
│   ├── car3x3t_3
│   ├── ficInput.txt
│   ├── ficOutput.txt
│   └── verif_lecfima.txt
├── Donnees_2
│   ├── NUMREF.Test
│   ├── Tests.1x1
│   └── Tests.3x3
├── Donnees_3
│   ├── tp3_RESU1
│   ├── tp3_RESU1_NeumannHomogene
│   ├── tp3_RESU3
│   └── tp3_RESU3_NeumannHomogene
├── Donnees_4
│   ├── tp4_RESU1
│   └── tp4_RESU3
├── Donnees_5
│   ├── Maillages
│   │   ├── d1q1_16
│   │   ├── d1q1_2
│   │   ├── d1q1_32
│   │   ├── d1q1_4
│   │   ├── d1q1_64
│   │   ├── d1q1_8
│   │   ├── d1t1_16
│   │   ├── d1t1_2
│   │   ├── d1t1_32
│   │   ├── d1t1_4
│   │   ├── d1t1_64
│   │   ├── d1t1_8
│   │   ├── d2q1_16
│   │   ├── d2q1_2
│   │   ├── d2q1_32
│   │   ├── d2q1_4
│   │   ├── d2q1_64
│   │   ├── d2q1_8
│   │   ├── d2t1_16
│   │   ├── d2t1_2
│   │   ├── d2t1_32
│   │   ├── d2t1_4
│   │   ├── d2t1_64
│   │   ├── d2t1_8
│   │   └── README
│   └── tp5_RESU_d1t1_2_complet
├── Executables
│   ├── main1.exe
│   ├── main1.sh
│   ├── main2a.exe
│   ├── main2a.sh
│   ├── main2b.exe
│   ├── main2b.sh
│   ├── main3.exe
│   ├── main3.sh
│   ├── main4.sh
│   ├── main5Test.sh
│   ├── mainAff.sh
│   ├── mainErreur.exe
│   ├── mainErreur.sh
│   ├── main.exe
│   ├── plot.exe
│   ├── plot.sh
│   └── testProfil.exe
├── Resultats
│   ├── Graphes
│   │   ├── 111.png
│   │   ├── 112.png
│   │   ├── 121.png
│   │   ├── 122.png
│   │   ├── 131.png
│   │   ├── 132.png
│   │   ├── 211.png
│   │   ├── 212.png
│   │   ├── 221.png
│   │   ├── 222.png
│   │   ├── 231.png
│   │   └── 232.png
│   ├── fort.111
│   ├── fort.112
│   ├── fort.121
│   ├── fort.122
│   ├── fort.131
│   ├── fort.132
│   ├── fort.211
│   ├── fort.212
│   ├── fort.221
│   ├── fort.222
│   ├── fort.231
│   ├── fort.232
│   └── plot.c
├── Utilitaire
│   ├── alloctab.c
│   ├── allocvec.c
│   ├── freetab.c
│   ├── freevec.c
│   ├── print.c
│   └── utilitaires.h
├── Compte_Rendu_Amyne_Xavier.pdf
├── forfun.h
├── mainAff.c
├── mainErreur.c
└── README.md
```

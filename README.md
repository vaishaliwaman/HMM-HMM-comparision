# Step-by-step guide for HMM-HMM comparision
# Validate members of a superfamily (whether they are significant homologues using hhalign/HHsuite)

STEP 1: Run jackhmmer to obtain MSA For each member, generate MSA using jackhmmer *The alignment is saved in '.sto' format

STEP 2: Genrate profile HMM using hhmake 
      a. convert .sto --> .a3m using reformat.pl
      b. Use hhmake to convert .a3m --> .hhm 

STEP 3: All-against-all HMM-HMM comparision using hhalign
(Probaility > 60, E-value < 1e-10 + also verify scores)

STEP 4: Other checks- structural comparision , PDB structure quality , Chainsaw chopping.

STEP 5: Decision on superfamily validation - 'approve', 'remove', 'remove and merge' 

STEP 6: Superfamily annotation and assignment of CATH codes



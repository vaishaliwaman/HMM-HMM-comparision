# Step-by-step guide for HMM-HMM comparision
# PDB novel folds (n=253) members clustered in new SuperFamilies (by Foldseek)
  We clustered the novel folds members found in PDB (n=253 reps, 2,054 members) into 272 SuperFamilies using the easy-cluster command as below. 
  The results are here  /mnt/sda2/holdingpen_plus_s95/PDB-253/  and they've been ran with this command
  Command and parameters:
../foldseek/bin/foldseek easy-cluster novel_folds_members_pdb/ novel_folds_to_sfams tmp --tmscore-threshold 0.7 -c 0.6 --alignment-type 1 --cov-mode 5 

# Validation of Foldseek-superfamily assignment using HMM-HMM comparision (HHsuite)

STEP 1: Obtain MSA for each member: Run jackhmmer to generate MSA - saved in '.sto' format

STEP 2: Genrate profile HMM using hhmake 
      a. convert .sto --> .a3m using (reformat.pl by HHsuite)
      b. Use hhmake to convert .a3m --> .hhm  

STEP 3: All-against-all HMM-HMM comparision using hhalign
(Probaility > 60, E-value < 1e-3 + also verify scores)

STEP 4: Other checks- structural comparision , PDB structure quality , Chainsaw chopping.

STEP 5: Decision on superfamily validation - 'Approve', 'Remove', 'Merge' 

STEP 6: Superfamily annotation and assignment of CATH codes 



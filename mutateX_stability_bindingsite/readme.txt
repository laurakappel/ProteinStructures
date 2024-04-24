The commands that are run in the MutateX stability

To run the MutateX stability we run the following command line:
nohup mutatex 2B8U_noH2O.pdb -p 4 -m mutation_list.txt -x /home/ctools/foldx5_2024/foldx -f suite5 -R repair_runfile_template.txt -M mutate_runfile_template.txt -q poslist.txt -L -l -v -C deep & 

To generate the energy file we run the following command line:
/home/ctools/anaconda3_2021.11/bin/ddg2excel -p 2B8U_noH2O.pdb -l mutation_list.txt -q poslist.txt -d results/mutation_ddgs/final_averages/ -F csv

To generate the density plot we run the following command line:
/home/ctools/anaconda3_2021.11/bin/ddg2density -p 2B8U_noH2O.pdb -l mutation_list.txt -q poslist.txt -d results/mutation_ddgs/final_averages/

To generate the heatmaps we run the following command line:
/home/ctools/anaconda3_2021.11/bin/ddg2heatmap -p 2B8U_noH2O.pdb -l mutation_list.txt -q poslist.txt -d results/mutation_ddgs/final_averages/ -n -2 -x 5 

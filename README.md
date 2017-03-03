# Object-Oriented Reinforcement Learning in Cooperative Multiagent Domains
This is the codification used in the BRACIS 2016 paper proposing the Multiagent Object-Oriented approach. You are free to use all or part of the codes here presented for any purpose, provided that the paper is properly cited and the original authors properly credited. All the files here shared come with no warranties.

Paper bib entry: <br><br>
<i>
 @inproceedings{Silvaetal2016,<br>
  author    = {Silva, Felipe Leno da and <br>
  			  Ruben Glatt and <br>
               Anna Helena Reali Costa},<br>
  title     = {{Object-Oriented Reinforcement Learning in Cooperative Multiagent Domains}},<br>
  booktitle = {Proceedings of the 5th Brazilian Conference on Intelligent Systems (BRACIS)},<br>
  pages     = {19--24},<br>
  year      = {2016}<br>
 }
 </i>
 <br><br>

This project was built on BURLAP2 (http://burlap.cs.brown.edu/). I included the Burlap version I used to avoid incompatibility issues, it is expected that you would need to change some lines on the code if you use a newer BURLAP version.

# Files
The folder <b>code</b> contains the Java implementation (as an Eclipse project) and the BURLAP source files.

The file <b>experiment_Results.zip</b> is the .csv files generated in our experiments for the paper.

The file <b>generateGraphFromBurlapFile.m</b> is a MATLAB implementation to read the .csv files and output graphs.

# How to use

The folder <b>code</b> stores all implementations. <b>GoldMineMultiagent</b> is a project with the Multiagent implementations and <b>GoldMineSingleAgent</b> is the Single-agent implementation. 

Import the project you want to use folder to Eclipse, or import all files (including the burlap jar in the lib folder as an library) in your preferred IDE.

The experiments of our paper are replicated by executing the <b>main</b> method in the <b>ExperimentBRACIS2016</b> class (I recommend executing the VM with the parameters -Xms1024m -Xmx14024m). 

After executing this method, .csv files will be generated with the experiments results, that can be used to print graphs on matlab by executing the file <b>generateGraphFromBurlapFile.m</b>.

We advise you to implement your own script to generate graphs, as the matlab file is not very well commented.

# Attention
Our DOO-Q and DQL implementations are highly optimized to execute experiments faster, which means that the memory consumption is huge. If you want to use it to applications or in a pc with low memory resources, you will need to change our implementation.

A huge amount of memory can be saved if the implementation of <b>DOOQPolicy</b> is changed to only store entries on <b>policyMemory</b> in case there is two Q-values tied as the best action. However, if you do so, the experiments will run slower.


# Contact

For questions about the Multiagent domain or algorithms, please send an email to the first author.

For questions about the Single-agent domain, please send an email to the second author.

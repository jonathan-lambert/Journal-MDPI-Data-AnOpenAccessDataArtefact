# Journal MDPI Data: An Open Access Data Artefact
The advantages of Java Runtime Environment (JRE) Java Virtual Machine (JVM) tiered execution compared to JVM interpretive execution are well recognised, but more research is needed to understand their performance differences relative to modern workloads. While interpretive execution offers benefits like adaptability, simplicity, portability, reduced complexity/costs, and more straightforward debugging/profiling, just-in-time compilation excels in execution time efficiency. However, contemporary questions regarding interpretive execution's performance advantages over tiered execution, specifically concerning power and energy consumption, still need to be answered. 

This paper describes an extensive dataset encompassing a rich collection of variables that capture JRE JVM performance behaviour. We developed the dataset to analyse the runtime behaviour of 198 JRE JVM variants. The dataset is comprehensive regarding its associated variables. It comprises categorical variables that encode the JRE JVM version, the compiler versions used within the build toolchain of the JRE, JRE JVM execution modes, and garbage collector variants, for example. In addition, the dataset contains many numerical variables, capturing microarchitectural behaviour such as branch misprediction rates, L1 and L2 data cache behaviour, for example, and an extensive collection of power and energy consumption variables, with factors capturing average, standard deviation, min, and max characteristics associated with system voltage, current, power, and energy consumption behaviour. 

The richness of the variables included within the data artefact introduced within this paper will allow for more nuanced assessments of JRE JVM performance beyond the typical null hypothesis significance testing techniques and, in particular, beyond single factor analysis. The data artefact offers numerous opportunities to analyse the JRE JVM from a multi-factor perspective, as well as from a multi-variant perspective. The dataset variables will allow interested researchers to undertake analyses regarding its principal component structure; the dataset can be used to construct multiple regression models and has enough observations to build machine learning models such as neural networks.



\textbf{Factor}   | \textbf{Type} | \textbf{Description} | \textbf{Label} | \textbf{Values} \\|
---|---|---|---|---|
\toprule|||||
"CPU utilised	|	Numerical	|	The proportion of all processor CPUs utilised	|	cpu	|	[	0	 …	4	]	\\|"
"Instructions executed	|	Numerical	|	The total number of microarchitectural instructions executed	|	ti	|	[	1.0E+10	 …	1.2E+13	]	\\|"
"Instructions per cycle	|	Numerical	|	The number of instructions executed per clock cycle	|	ipc	|	[	3.1E-01	 …	1.1E+00	]	\\|"
\midrule|||||
"Branches taken	|	Numerical	|	The total number of branch instructions executed	|	tbr	|	[	1.8E+09	 …	1.9E+12	]	\\|"
"Branches per total instructions	|	Numerical	|	The proportion of branch instructuions executed per total instructions executed	|	tbrpti	|	[	1.2E+01	 …	2.3E+01	]	\\|"
"Branches Mps	|	Numerical	|	The proportion of branch instructions executed in millions per second	|	brmps	|	[	8.9E+01	 …	3.1E+02	]	\\|"
"Branch misses	|	Numerical	|	The total number of branch misses incurred	|	tbmr	|	[	9.9E+07	 …	2.0E+11	]	\\|"
"Branch miss-rate	|	Numerical	|	The branch misprediction rate	|	bmr	|	[	7.3E-01	 …	2.0E+01	]	\\|"
\midrule|||||
"L1 data cache loads	|	Numerical	|	The total number of L1 data cache loads	|	tl1dl	|	[	3.4E+09	 …	5.3E+12	]	\\|"
"L1 data loads per instructions	|	Numerical	|	The propotion of L1 data cache loads per total instructions executed	|	tl1dlpti	|	[	2.2E+01	 …	5.0E+01	]	\\|"
"L1 data cache loads Mps	|	Numerical	|	The proportion of L1 data cache loads in millions per second	|	l1dlmps	|	[	1.7E+02	 …	7.5E+02	]	\\|"
"L1 data cache misses	|	Numerical	|	The total number of L1 data cache misses incurred	|	tl1dlmr	|	[	1.2E+08	 …	1.8E+11	]	\\|"
"L1 data cache miss-rate	|	Numerical	|	The L1 data cache miss-rate	|	l1dlmr	|	[	5.6E-01	 …	6.0E+00	]	\\|"
\midrule|||||
"L2 data cache loads	|	Numerical	|	The total number of L2 data cache loads	|	tl2dl	|	[	3.8E+08	 …	4.5E+11	]	\\|"
"L2 data loads per instructions	|	Numerical	|	The propotion of L2 data cache loads per total instructions executed	|	tl2dlpti	|	[	6.0E-01	 …	1.1E+01	]	\\|"
"L2 data cache loads Mps	|	Numerical	|	The proportion of L2 data cache loads in millions per second	|	l2dlmps	|	[	8.9E+00	 …	6.0E+01	]	\\|"
"L2 data cache misses	|	Numerical	|	The total number of L2 data cache misses incurred	|	tl2dlmr	|	[	2.1E+07	 …	1.0E+10	]	\\|"
"L2 data cache miss-rate	|	Numerical	|	The L2 data cache miss-rate	|	l2dlmr	|	[	2.8E-01	 …	3.9E+01	]	\\|"
\midrule|||||
"Page faults	|	Numerical	|	The total number of page faults incurred	|	tpf	|	[	3.6E+04	 …	1.2E+06	]	\\|"
"Page faults per instructions	|	Numerical	|	The proportion of page faults per total instructions executed	|	tpfpti	|	[	1.9E-06	 …	1.0E-03	]	\\|"
"Page fault miss-rate	|	Numerical	|	The page fault miss-rate	|	pfmr	|	[	1.5E-03	 …	3.7E-01	]	\\|"
"Page faults Kps	|	Numerical	|	The total number of page faults in thousands per second	|	pfkps	|	[	1.0E-03	 …	9.8E-01	]	\\|"
\midrule|||||
"Other instructions	|	Numerical	|	The total number of instructions executed, other than branches, L1 data cache loads, or L2 data cache loads	|	to	|	[	4.4E+09	 …	4.3E+12	]	\\|"
"Other instructions per instructions	|	Numerical	|	The total proportion of other instructions executed per toatl instructions executed	|	topti	|	[	3.2E+01	 …	5.8E+01	]	\\|"
\midrule|||||
"Benchmark execution time	|	Numerical	|	The benchmark execution time	|	rtp	|	[	6.1E+00	 …	4.0E+03	]	\\|"
"Task clock (msec)	|	Numerical	|	The task clock in miliseconds	|	tc	|	[	8.3E+03	 …	1.2E+07	]	\\|"
\midrule|||||
"Average current	|	Numerical	|	The average current measured	|	meanA	|	[	6.7E-01	 …	1.0E+00	]	\\|"
"Standard deviation current	|	Numerical	|	The standard deviation associated with average current measurements	|	stdA	|	[	3.9E-02	 …	2.1E-01	]	\\|"
"Minimum current	|	Numerical	|	The minimum current measured	|	minA	|	[	4.4E-01	 …	6.1E-01	]	\\|"
"Maximum current	|	Numerical	|	The maximum current measured	|	maxA	|	[	1.1E+00	 …	1.9E+00	]	\\|"
"Total current samples taken	|	Numerical	|	The total number of current samples taken	|	samplesA	|	[	1.2E+07	 …	8.1E+09	]	\\|"
\midrule|||||
"Average voltage	|	Numerical	|	The average voltage measured	|	meanV	|	[	5.0E+00	 …	5.0E+00	]	\\|"
"Standard deviation voltage	|	Numerical	|	The standard deviation associated with average voltage measurements	|	stdV	|	[	8.9E-03	 …	4.1E-02	]	\\|"
"Minimum voltage	|	Numerical	|	The minimum voltage measured	|	minV	|	[	4.8E+00	 …	4.9E+00	]	\\|"
"Maximum voltage	|	Numerical	|	The maximum voltage measured	|	maxV	|	[	5.1E+00	 …	5.1E+00	]	\\|"
"Total voltage samples taken	|	Numerical	|	The total number of voltage samples taken	|	samplesV	|	[	1.2E+07	 …	8.1E+09	]	\\|"
\midrule|||||
"Average power	|	Numerical	|	The average power measured	|	meanW	|	[	3.3E+00	 …	5.2E+00	]	\\|"
"Standard deviation power	|	Numerical	|	The standard deviation associated with average power measurements	|	stdW	|	[	1.9E-01	 …	1.0E+00	]	\\|"
"Minimum power	|	Numerical	|	The minimum power measured	|	minW	|	[	2.2E+00	 …	3.0E+00	]	\\|"
"Maximum power	|	Numerical	|	The maximum power measured	|	maxW	|	[	5.4E+00	 …	9.2E+00	]	\\|"
"Total power samples taken	|	Numerical	|	The total number of power samples taken	|	samplesW	|	[	1.2E+07	 …	8.1E+09	]	\\|"
\midrule|||||
"Capacitance	|	Numerical	|	The overall system capacitance	|	C	|	[	4.5E+00	 …	3.5E+03	]	\\|"
"Amp hours	|	Numerical	|	The total current hours	|	Ah	|	[	1.2E-03	 …	9.7E-01	]	\\|"
"Energy consumed	|	Numerical	|	The total energy consumed in Joules	|	energyJ	|	[	2.2E+01	 …	1.7E+04	]	\\|"
"Energy consumed	|	Numerical	|	The total energy consumed in Watt-hours	|	energyWh	|	[	6.2E-03	 …	4.8E+00	]	\\|"![image](https://github.com/jonathan-lambert/Journal-MDPI-Data-AnOpenAccessDataArtefact/assets/57734342/29458912-32c8-41eb-9a25-fe6fe58ec3ff)

Steps to Generate movingaverages.py file.

1) In the param.input file, do the below sequentially.
	a.	Increase or decrease the window size by changing the value for variables startWindow and endWindow respectively.
	b.	Give the location of the Source file on local file system.
	c.	Give the location of the output file on local file system
	d.  Follow Steps b & C to load the second source file and to specify the output directory.

2) To Generate the python file, execute the below:
	sed -f 3_param.input 4_movingaverages.py.template > movingaverages.py

3) To execute:
	a. Issue the below:
		spark-submit movingaverages.py

	b. If pypark is configured to work with Jyupter Notbooks, launch JN from the current working directory, open up a new python 3 notebook and issue the below command:
		!python movingaverages.py

4) The output files with moving averages should be available in the output directory defined at Step 1.b & Step 1.d

5) If multiple sources needs to be tested, plese uncomment from line 35-51 from the template file and configure the paths accordingly in param.input file.

Constraints:
1) This App is developed and tested in Spark Local mode on my local machine.

To run the program in cluster mmode:

1) We need to change the input and output file path to HDFS.
2) Change the master to cluster mode.



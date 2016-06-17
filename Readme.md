#Vehicular Clouds

Description: The goal of this project is to simulate a datacenter implemented on the cars in the parking lot of a medium-sized airport. Since the cars arrive and depart randomly, the challenge facing the implementation of the datacenter is to maintain high availability and reliability in the face of the
dynamically changing resources. Have successfully implemented the data replication and job migration before the car departs in the parking lot. Thus with the improved migration strategy, reduced the chances of job failures



Following are the output files that are generated during the simulation.

1. CarsAndJobDetails.txt: This file includes the specific car details such as arriving time, departure time, Spot number that car is assigned. 
			  In addition, it has job details of a car once the job is assigned. Job details include job number, jobsize, carnumber 
			  that the job is assigned, job duration time, amount of data that is produced.

2. SpotDetails.txt: This file has parking spot details in the range 1-2560. For every parking spot with this, we know the cluster number that it belongs to, 
		    group center number and region center number.

3. TurnedAwayCars.txt: Total number of cars turned away during the simulation.

4. PossiblePassedJob: This has the rough estimate of possible cars that may complete the jobs with the total count at the end of the file.

5. PossibleFailedJob: This has the rough estimate of possible cars that may fail to complete the jobs. The total failed jobs are mentioned at the end of the file.

6. SuccessfullyMigratedJobs: This file has the details about the number of jobs migrated during the simulation.

7. FailedMigratedJobs: This file has the details about the number of jobs failed to migrate. The count of it is mentioned at the end of the file.

8. replicationData: This file has the replication of car data to different cars within the same cluster and also to the cars of different cluster belonging to same region.

9. NewCarsAssignedtoSpot: This file has the details of assigning the new cars at time 't' to the parking spot once the car departs at this time.



Running the file instructions:

1. Copy the files VehicleParking.cpp, makeFile, FileGenerater.cpp into one of the directories by logging into atria.cs.odu.edu in putty.

2. Compile and Run the file FileGenerater.cpp to generate the arrival and departure of flights which will be generated as two output files.

   Following is the command to run the above file
		g++ FileGenerater.cpp
		./a.out

	This will generate the following output files.
	1. input_departure_time_of_flight.txt
	2. input_arrival_time_of_flight.txt

	These files are used in our program as input to calculate the arrival and departure time of cars.

3. Compile  project file VehicleParking.cpp in the following way.
	makeFile 

	This will generate the executable named VEHICLEPARKING.exe

	Run the executable in the following way to execute the simulation.

	VEHICLEPARKING

4. Analyze the output files that are generated in the same directory.

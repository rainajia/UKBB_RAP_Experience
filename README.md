# Common errors when running jobs on RAP 

These are common errors that may occor when using the mrcepid applets (https://github.com/mrcepid-rap) on RAP (18/03/2022 update). 

| Error message | Reasons for error | Solutions/Notes |
| ---| --- | --- |
| **The machine running the job was terminated by the cloud provider** |  This error is due to spot interruption when using a low priority instance | There is charge for the time the job has already ran. This error is sponateous, there is nothing else the user can do about it except either restarting the job or changing to a high priority instance |
| **The machine running the job became unresponsive**   | This error occurs when the machine runs out of memory   | This error is not charged for the time that has ran, as DNAnexus decides that this kind of error is not due to user's fault. Try reduces the number of input files, if still not working, consdering changing to an instance with a larger memory |
| **Failed to run properly...** | This error is due to a bug on the backend of the RAP platform (something to do with the file storage system). It is supposed to be a temprory issue | The error tends to occur around 6:30am in the morning. The charge is applied for the time the the job has ran. It is adviced to time the job submission time wisely to avoid having a job running over 6:30am. This issue still has not been fixed by DNAnexus as of 18th March 2022. |
| **DXError: Invalid ID of class file:** | This error occurs when using the mrc-associationtesting applet. It is due to the occurance of one or more blank lines in the input file with the list of input file IDs. | Check if there are any empty lines in the input file |
| **Other applet specific errors** | These kinds of error usually specify what the the problem was in the report. | If no obvious mistakes are identified in the input and output files, should consult [Eugene Gardner](https://github.com/eugenegardner) about the problem. |
 

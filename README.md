# Common error messages when running jobs on RAP                                                                                                                              
These are common errors that may occur when using the mrcepid applets (https://github.com/mrcepid-rap) on RAP (18/03/2022 update). 

| Error message | Reasons for error | Solutions/Notes |
| ---| --- | --- |
| **The machine running the job was terminated by the cloud provider** | This error is due to spot interruption when using a low priority instance | There is a charge for the time the job has already ran. This error is spontaneous, there is nothing else the user can do about it except either restarting the job or changing to a high priority instance |
| **The machine running the job became unresponsive**   | This error occurs when the machine runs out of memory   | This error is not charged for the time that has ran, as DNAnexus decides that this kind of error is not due to user's fault. Try reducing the number of input files, if still not working, considering changing to an instance with a larger memory |
| **Failed to run properly...** | Usually an internal app issue | The error was previoulsy mainly due to the backend storage issue, which had been resolved by DNAnexus in April 2022. It could still occur as of now and it would be due to an internal app issue. If no obvious mistakes are identified in the input files or codes, consult [Eugene Gardner] (https://github.com/eugenegardner) about the problem.  |
| **DXError: Invalid ID of class file:** | This error occurs when using the [mrcepid-runassociationtesting](https://github.com/mrcepid-rap/mrcepid-runassociationtesting) applet. It is due to the occurrence of one or more blank lines in the input .txt file with file IDs | Make sure there is no empty rows in the .txt input file |
| **Other applet specific errors** | This kind of error usually specify what the problem is in the error log. | If no obvious mistakes are identified in the input files or codes, consult [Eugene Gardner] (https://github.com/eugenegardner) about the problem. |


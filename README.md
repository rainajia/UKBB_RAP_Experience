# Common errors on RAP 

## These are common error that may occure to a job submission when using the mrcepid applets (https://github.com/mrcepid-rap) on RAP  

| Error message | Reason for error | Notes |
| ---| --- |
| The machine running the job was terminated by the cloud provider   |  This error is due to spot interruption when using a low priority instance | There is charge for the time the job has already ran. This error is sponateous and there is nothing else the user can do about excep restart the job or change to a high priority instance |
| The machine running the job became unresponsive    | This error occurs when the machine runs out of memory   | This error is not charged for the time that has ran, as DNAnexus decides that this kind of error is not due to user's fault.|
| Failed to run properly... | This error is due to a bug on the backend of the RAP platform (something to do with the file storage system) | The job tends to fail at 6:30am in the morning. The charge is applied for the time the the job has ran. This is supposed to be a temporary issue. It has not been fixed by DNAnexus as of 18th March 2022
| DXError: Invalid ID of class file: | This error occurs when using the mrc-associationtesting applet, the applet returns an error when there is a blank line in the input file of the file ID list | Avoid having any empty lines in the input file
| Other applet specific errors | these kind of errors usually specify the problem | if no obvious mistakes are identified in the input and output file, should consult Eugene Gardner about the slution 

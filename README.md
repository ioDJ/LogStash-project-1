# LogStash Project 1
This is my first repo on GitHub for a LogStash pipeline.

I was tasked with creating a solution that could structure the fields within the security log data entry "LogData-1" into JSON format.

Located in the repo: 
* the LogData-1.txt input file with the the security log data entry,
* the Project1.conf LogStash config file used in LogStash,
* the Output-1.json output file of the solution.

## Short Description of Project1.conf file

The task was to create a solution that could parse the fields within the security log data entry "LogData-1".

* I chose to leave the input source and the output destination empty in the .conf file due to them already being uploaded to the repo. 
* The .conf file uses a grok filter to extract matching regular expressions.
* The remaining data appeared to be in a "key=value" format, so I opted to use the "kv" filter next.
* I also used the mutate filter to remove extra fields with "remove_field" and appropriately rename keys with "rename".

I tested the pipeline with PowerShell and the Windows command prompt, and constructed it in Visual Studio Code.

Thanks!

***

## Troubleshooting

For the most part, the task presented was straightforward and challenging as a first project, despite my grokking and parsing experience!

I came across only one issue I couldn't overcome within the deadline:

The task requested the "severity" value to formatted as "High" rather than "1". I attempted to run the data through: 

* "if { mutate { update } }"
* "if { mutate { replace } }"
* "if { mutate { convert } }"

However, the output remained virtually the same as the result in the Output-1.json file, regardless of any mutate filters/syntax changes.
Feel free to provide any insight as you see fit!

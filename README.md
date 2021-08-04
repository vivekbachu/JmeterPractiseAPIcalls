# JmeterPractiseAPIcalls

How to Run Get API -

'jmeter -JRESPONSEOUTPUT="Outputfilepath.csv" -n -t GetRecordAPI.jmx -JUser=1 -JLoopCount=3'

How to Run "CreateRecordAPI.jmx" jmx

'jmeter -JRESPONSEOUTPUT="Outputfilepath.csv" -n -t CreateRecordAPI.jmx -JUser=1 -JLoopCount=1'

How to Run "PutupdateRecordAPI.jm"

'jmeter -JRESPONSEOUTPUT=/Users/vivekbachu/Desktop/put.csv -n -t PutupdateRecordAPI.jmx -JUser=1 -JLoopCount=1'

If the scripts need to be run through the Docker -

Get jmeter Docker image from below - https://hub.docker.com/r/justb4/jmeter/

docker run -v "{FilePathOfLocalDirectorywherejmxarepresent}":"{DirToBeCreatedInContainer}" justb4/jmeter -n -t {FilePathofjmx.jmx} -JRESPONSEOUTPUT="{DirToBeCreatedInContainer/.csv}" -JUser={NoOfUsers} -JLoopCount={NoOfLoopCount}



# xargs

can use this to execute on multiple cores

-P <no_of_cores>	the number of cores to use
-I <identifier> the identifier to pass the output of the script before the | as
-c <command> execute the command
-0 ensures the separator between the inputs to the command is the null character
	for example, use print0 with find and -0 with xargs to ensure inputs can be processed

pipe the output of one command into another command which will be executed in parallel

## example

find . -type f -print0 | xargs -0 sed "s/=/#/g"

list of the files in this directory and subdirectories
pipe them into xargs
execute sed "/s=/#/g" on each file


kubectl get nodes -o wide | awk '{print $6}' | xargs -I {} scp retagged-images.tar {}:/home/eccd
  get all the information about the worker nodes
  awk out the ips
  scp a file on each ip


awk '{print $6}' <(cat nodes.txt) | xargs -I {} ssh {} sudo docker load -i retagged-images.tar;
  had to output the node information to file so I could delete the entries which didn't have valid ips

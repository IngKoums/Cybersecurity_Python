<b>Python</b>

Algorithm for file updates in Python</b>

Project description</b>

You are a security professional working at a health care company. As part of your job, you're required to regularly update a file that identifies the employees who can access restricted content. The contents of the file are based on who is working with personal patient records. Employees are restricted access based on their IP address. There is an allow list for IP addresses permitted to sign into the restricted subnetwork. There's also a remove list that identifies which employees you must remove from this allow list.
Your task is to create an algorithm that uses Python code to check whether the allow list contains any IP addresses identified on the remove list. If so, you should remove those IP addresses from the file containing the allow list.

Here is how i went throught this scenario : 

 1- Open the file that contains the allow list

The file that i want to open is called "allow_list.txt". i assigned a string containing this file name to the import_file variable. Then, used a with statement to open it. Use the variable file to store the file while you work with it inside the with statement.
 <br/>
 
<img src="https://i.imgur.com/J1PdczB.png" height="80%" width="80%"/>
<br />
<br />

 2- Read the file contents
 
Next, i used the .read() method to convert the contents of the allow list file into a string so that i can read them. Stored this string in a variable called ip_addresses.

<img src="https://i.imgur.com/05WdReK.png" height="80%" width="80%"/>
<br />
<br />

 3- Convert the string into a list
 
In order to remove individual IP addresses from the allow list, the IP addresses need to be in a list format. Therefore, i used the .split() method to convert the ip_addresses string into a list.
 
   <img src="https://i.imgur.com/97us32V.png" height="80%" width="80%"/>
<br />
<br />

4- Remove IP addresses that are on the remove list

In the body of my iterative statement, i added code that will remove all the IP addresses from the allow list that are also on the remove list. First, created a conditional that evaluates if the loop variable element is part of the ip_addresses list. Then, within that conditional, applied the .remove() method to the ip_addresses list and removed the IP addresses identified in the loop variable element. 

<img src="https://i.imgur.com/VdQ067g.png" height="80%" width="80%"/>
<br />
<br />

 5- Update the file with the revised list of IP addresses 
 
Now that i have removed these IP addresses from the ip_address variable, i completed the algorithm by updating the file with this revised list. I first converted the ip_addresses list back into a string using the .join() method, then Applied .join() to the string "\n" in order to separate the elements in the file by placing them on a new line.

<img src="https://i.imgur.com/2SYK4Ng.png" height="80%" width="80%"/>
<br />
<br />

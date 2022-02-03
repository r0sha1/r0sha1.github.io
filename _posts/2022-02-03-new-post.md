## Jerry HTB 

First lets start by checking connection to the target.
<img width="822" alt="Screen Shot 2022-02-03 at 13 02 33" src="https://user-images.githubusercontent.com/98924222/152298124-b6d93f85-3aec-4f4a-90ef-d6d31e0f8646.png">

First as usual lets run NMAP scan , i have never seen these type of scans. LOL


![image](https://user-images.githubusercontent.com/98924222/152298372-a2eca251-5e3a-4445-b597-deb674cb8c88.png)

Anyway, below are the results;


<img width="819" alt="Screen Shot 2022-02-03 at 13 05 45" src="https://user-images.githubusercontent.com/98924222/152298504-40977598-23f0-4486-ba0a-29c04e120910.png">


Since port 80 is open. lets input the IP in firefox. Well no results.


<img width="817" alt="Screen Shot 2022-02-03 at 13 06 28" src="https://user-images.githubusercontent.com/98924222/152298609-ba7456d3-923f-4bbc-8d24-6b76413faa09.png">

<img width="847" alt="Screen Shot 2022-02-03 at 13 10 52" src="https://user-images.githubusercontent.com/98924222/152299563-46275321-532c-41b3-a95c-b80581e6c830.png">

ok, i didnt knew I needed to specify the port number so,

<img width="815" alt="Screen Shot 2022-02-03 at 13 07 19" src="https://user-images.githubusercontent.com/98924222/152298691-825ae070-1129-4af3-bc0a-789bd38bc08b.png">


Ok now lets click on server status, a dialog box appear for password and username. upon clicking cancel username and password is revealed which is tomcat s3cret.


<img width="820" alt="Screen Shot 2022-02-03 at 13 07 53" src="https://user-images.githubusercontent.com/98924222/152298787-7d83dc51-0d5c-4d01-afd1-a4c0ce4c0220.png">


Click list applications here we can see, WAR file to upload. UPON resaerch its an java type payload.

 <img width="818" alt="Screen Shot 2022-02-03 at 13 08 51" src="https://user-images.githubusercontent.com/98924222/152298906-ec46ada6-480f-490e-bd2c-d529a8e25ac1.png">
 
 
 lets create payload in msfvenom
 <img width="817" alt="Screen Shot 2022-02-03 at 13 09 49" src="https://user-images.githubusercontent.com/98924222/152299016-572069b9-9e15-46ec-ac83-51fcd7410625.png">


now lets upload this WAR file

<img width="813" alt="Screen Shot 2022-02-03 at 13 10 32" src="https://user-images.githubusercontent.com/98924222/152299099-1ec9adff-26dc-4fff-84d1-552d0b66b511.png">

Screen Shot 2022-02-03 at 13.10.52<img width="847" alt="image" src="https://user-images.githubusercontent.com/98924222/152299767-0c12cff3-cabe-4c76-bad4-f23494b218b9.png">

we can see /runme in list of apps now 

lets start the playload
on terminal lets listen on p 4444
Screen Shot 2022-02-03 at 13.11.19<img width="821" alt="image" src="https://user-images.githubusercontent.com/98924222/152299828-afee366e-8ed5-4bd8-ab8e-d8bf3708720c.png">


ok we have a shell now

 <img width="818" alt="Screen Shot 2022-02-03 at 13 11 38" src="https://user-images.githubusercontent.com/98924222/152299269-c55ea81a-38d5-4af6-9477-b751ccfeb480.png">
 
 
 i was tying ls, sorry about that. so i have GOD permission. GAME OVER. SYSTEM BREACHED.
 
 
<img width="811" alt="Screen Shot 2022-02-03 at 13 12 25" src="https://user-images.githubusercontent.com/98924222/152299347-fa8b9ad7-3cf2-42b4-897e-8e56dd383be6.png">


<img width="803" alt="Screen Shot 2022-02-03 at 13 12 33" src="https://user-images.githubusercontent.com/98924222/152299389-0df86532-e916-422c-9e7c-0d664c556410.png">



I GOT THE FLAG. MISSION COMPLETED.


 
 



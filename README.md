# Linux-File-Permissions
# File permissions in Linux


## Project description

Task is to examine existing permissions on the file system and determine if the permissions match the authorization that should be given. Need to modify permissions to authorize appropriate users and remove unauthorized access.


## Check file and directory details

I used linux commands shown below to determine the current permissions in the specified directory. We can see that the research_team is the group that owns the files in this directory. 



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")



## Describe the permissions string

The permissions string is a sequence of 10 characters that can be broken down to understand who has access to the file and what kind of access they have. Here’s what each character signifies:



* 1st character: This character can either be a ‘d’ or a hyphen (-). If it’s a ‘d’, it means the file is a directory. If it’s a hyphen (-), it means the file is a regular file.
* 2nd to 4th characters: These characters represent the read (r), write (w), and execute (x) permissions for the user who owns the file. If any of these characters is a hyphen (-), it means that the corresponding permission is not granted to the user.
* 5th to 7th characters: These characters represent the read (r), write (w), and execute (x) permissions for the group that owns the file. If any of these characters is a hyphen (-), it means that the corresponding permission is not granted to the group.
* 8th to 10th characters: These characters represent the read (r), write (w), and execute (x) permissions for all other users on the system. If any of these characters is a hyphen (-), it means that the corresponding permission is not granted to these users.

 


## Change file permissions

I used the linux commands shown below to change file permissions according to the following instructions. The file project_k.txt should not be writable  by others. The file `project_m.txt` is a restricted file and should not be readable or writable by the group or other; only the user should have these permissions on this file. 



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")



## Change file permissions on a hidden file

Used linux commands below to change file permissions on a hidden file becauseThe file `.project_x.txt` is a hidden file that has been archived and should not be written to by anyone. (The user and group should still be able to read this file.) 

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")



## Change directory permissions

Used linux commands  below to change directory permissions because only the `researcher2` user should be allowed to access the `drafts` directory and its contents. This means that only researcher2 should have execute permissions.



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")



## Summary

I adjusted a number of permissions for files and directories in the projects directory to reflect the degree of authorization that my organization required. Checking the directory's permissions with ls -la was the initial step in this process. This helped me make decisions about what to do next. I then changed the permissions of files and directories several times using the chmod program.

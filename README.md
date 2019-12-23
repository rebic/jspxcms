# jspxcms XXE
jspxcms:v9.5.1 JDK:v1.7.0_80

homepage: http://www.jspxcms.com/

download URL: http://www.jspxcms.com/uploads/jspxcms-9.5.1-release-src.zip

## Affected version
v9.5.0～9.5.1

v8.0.0~8.0.4

v7.0.1~7.0.2

v6.5.1~6.5.4

## Vulnerability details
step1:Log in the background system as Administrator，Access system management -> site management, select the default site, and click export
![](https://github.com/rebic/jspxcms/blob/master/11.png)

setp2:Unzip the exported package. After unzip, the file list is as follows
![](https://github.com/rebic/jspxcms/blob/master/12.png)

step3:Modify the info.xml file, For more intuitive test results, delete redundant test data,keep a piece of test data

Insert the following statement in the second line of the XML file：

  "\<!DOCTYPE aa \[
  \<!ENTITY file SYSTEM "file:///etc/passwd" \>\]\>"
  
Modify the text property value of info object to: & file; the result is as follows
![](https://github.com/rebic/jspxcms/blob/master/info.png)


step4:Compress the modified file to zip again

step5:Import compressed file
![](https://github.com/rebic/jspxcms/blob/master/15.png)

step6:The passwd file was successfully written to the database, can be viewed at the front-end site
![](https://github.com/rebic/jspxcms/blob/master/passwd.png)

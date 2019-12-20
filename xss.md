
# jspxcms XSS
jspxcms:v9.5.1

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

step3:Modify the site.xml file, modify the data in line 79, as follows
![](https://github.com/rebic/jspxcms/blob/master/xss.png)


step4:Compress the modified file to zip again

step4:Import compressed file
![](https://github.com/rebic/jspxcms/blob/master/15.png)

step5:Refresh the background home page and find malicious pop ups
![](https://github.com/rebic/jspxcms/blob/master/alert.png)

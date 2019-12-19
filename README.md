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
![](https://github.com/rebic/jspxcms/blob/master/1.png)

setp2:Extract the exported compressed file and modify the site.xml file
![](https://github.com/rebic/jspxcms/blob/master/2.png)

step3.Recompress the extracted file to zip after modification
![](https://github.com/rebic/jspxcms/blob/master/3.png)
step4.Import compressed file
![](https://github.com/rebic/jspxcms/blob/master/4.png)

step.Result
![](https://github.com/rebic/jspxcms/blob/master/5.png)

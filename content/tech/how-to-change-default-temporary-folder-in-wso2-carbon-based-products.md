+++
title = "How to change default temporary folder in WSO2 carbon based products"
date = 2012-03-11T22:37:00Z
updated = 2012-03-11T22:44:54Z
tags = ["carbon", "wso2", "windows", "linux", "temp"]
blogimport = true 
[author]
	name = "Shelan Perera"
	uri = "https://plus.google.com/110975611609309023449"
+++

<div dir="ltr" style="text-align: left;" trbidi="on">In wso2 carbon based products default temporary folder is {product_home}/tmp.<br /><br />&nbsp;If you need to change that location to a  different location here is the way to do it.<br /><br />&nbsp;You can change the location by changing the locations in start up scripts.<br /><br />&nbsp;1) In Linux (/bin/wso2server.sh) change following parameter's location.<br /><br /><pre class="brush:js;"><br />&nbsp;-Djava.io.tmpdir="$CARBON_HOME/tmp"<br /><br /></pre><br /> &nbsp;2) In Windows (/bin/wso2server.bat) change the following parameter's location.<br /><pre class="brush:js;"><br />&nbsp;-Djava.io.tmpdir="%CARBON_HOME%\tmp"</div><br /></pre>

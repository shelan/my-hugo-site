+++
title = "How to disable automatic service creation with WSDL upload"
date = 2013-04-22T10:07:00Z
updated = 2013-04-26T19:19:14Z
tags = ["greg", "registry", "wsdl"]
blogimport = true 
[author]
	name = "Shelan Perera"
	uri = "https://plus.google.com/110975611609309023449"
+++

<div dir="ltr" style="text-align: left;" trbidi="on"><br />When you upload a WSDL to WSO2 Governance Registry it will create a Service Artifact automatically for that WSDL. But in case you do not want that to be automated and need to add services differently this is how to disable that feature.<br /><br />1) Open GREG_HOME/repository/conf/registry.xml<br /><br />2) Search for&nbsp;<span style="font-family: Courier New, Courier, monospace;"> </span><br /><pre><pre style="background-color: #eeeeee; border: 0px; font-family: Consolas, Menlo, Monaco, 'Lucida Console', 'Liberation Mono', 'DejaVu Sans Mono', 'Bitstream Vera Sans Mono', 'Courier New', monospace, serif; font-size: 14px; line-height: 18px; margin-bottom: 10px; max-height: 600px; overflow: auto; padding: 5px; vertical-align: baseline; width: auto;"><code style="border: 0px; font-family: Consolas, Menlo, Monaco, 'Lucida Console', 'Liberation Mono', 'DejaVu Sans Mono', 'Bitstream Vera Sans Mono', 'Courier New', monospace, serif; margin: 0px; padding: 0px; vertical-align: baseline;">&lt;property name="createService"&gt;false&lt;/property&gt;</code></pre></pre>and uncomment them.<br /><br />There will be two locations generally for normal WSDL handler and for ZIP or archive based upload handler (Where you upload multiple WSDL files together).<br /><br />Save registry.xml and restart your server. Now you can observe that it will not create Services automatically for WSDL uploads.</div>

+++
title = "How to send CDATA inside your SOAP message payload"
date = 2013-03-26T22:07:00Z
updated = 2013-07-18T09:45:17Z
tags = ["cdata", "soap", "transformation"]
blogimport = true
categories=["tech"] 
[author]
	name = "Shelan Perera"
	uri = "https://plus.google.com/110975611609309023449"
+++

<div dir="ltr" style="text-align: left;" trbidi="on"><span style="background-color: #ea9999;">(Please note this a temporary workaround and this will be addressed properly in future releases)</span><br /><br />If you need to send a SOAP message payload ever and if it resulted something like this.<br /><br /><span style="color: #434343; font-family: Courier New, Courier, monospace; font-size: 13px; line-height: 19px;"><b>&amp;lt;task:customerSchema&gt;&amp;lt;ext:value&gt;&amp;amp;lt;maxStops&gt;2&amp;amp;lt;/maxStops&gt;&amp;lt;/ext:value&gt;&amp;lt;/task:customerSchema&gt;</b></span><br /><span style="color: #434343; font-family: Arial, Helvetica, Verdana, monospace, san-serif; font-size: 13px; line-height: 19px;"><br /></span>Because  by default, a StAX parser must be in non coalescing mode (It overrides  the default settings mandated by the StAX specification) and as a side effect of that parser coaelsce CDATA sections. [1]<span style="color: #434343; font-family: Arial, Helvetica, Verdana, monospace, san-serif; font-size: 13px; line-height: 19px;"><br /></span>You need to add the&nbsp;XMLInputFactory.properties file with the following entry to CARBON_HOME/ (root) folder.<br /><div><br /></div><div><b></b><br /><pre><b><code>javax.xml.stream.isCoalescing=false</code></b></pre></div><div><br /></div><div>For more information</div><div>[1] http://people.apache.org/~veithen/axiom/userguide/ch04.html#factory.properties<br /><br />[2]&nbsp;http://wso2.org/forum/thread/10891</div><div><br /></div></div>

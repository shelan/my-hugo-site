+++
title = "How to correct ERROR 2002 (HY000): Can't connect to local MySQL server through socket /tmp/mysql.sock on Mac OS X"
date = 2014-10-25T02:35:00Z
updated = 2014-11-02T22:47:15Z
tags = ["OSX", "mysql", "mysqld", "Mac", "yosemite", "brew"]
blogimport = true 
categories=["tech"]
[author]
	name = "Shelan Perera"
	uri = "https://plus.google.com/110975611609309023449"
+++

<div dir="ltr" style="text-align: left;" trbidi="on"><br />I tried to install mysql using home-brew. Everything was successful But could not connect to the server. Obviously server have not started.<br /><br /><div style="background-color: black; color: whitesmoke; font-family: Monaco; font-size: 12px;">ERROR 2002 (HY000): Can't connect to local MySQL server through socket '/tmp/mysql.sock' (2)</div><div><br /></div><div>Sigh..</div><div><br /></div><div>Following command rescued me..</div><div><br /></div><div><pre class="lang-sql prettyprint prettyprinted" style="background-color: #eeeeee; border: 0px; font-family: Consolas, Menlo, Monaco, 'Lucida Console', 'Liberation Mono', 'DejaVu Sans Mono', 'Bitstream Vera Sans Mono', 'Courier New', monospace, serif; font-size: 14px; line-height: 17.804800033569336px; margin-bottom: 10px; max-height: 600px; overflow: auto; padding: 5px; vertical-align: baseline; width: auto; word-wrap: normal;"><code style="border: 0px; font-family: Consolas, Menlo, Monaco, 'Lucida Console', 'Liberation Mono', 'DejaVu Sans Mono', 'Bitstream Vera Sans Mono', 'Courier New', monospace, serif; margin: 0px; padding: 0px; vertical-align: baseline; white-space: inherit;"><span class="pln" style="background-color: transparent; border: 0px; margin: 0px; padding: 0px; vertical-align: baseline;">mysqld stop<br />mysql</span><span class="pun" style="background-color: transparent; border: 0px; margin: 0px; padding: 0px; vertical-align: baseline;">.</span><span class="pln" style="background-color: transparent; border: 0px; margin: 0px; padding: 0px; vertical-align: baseline;">server start</span><span class="kwd" style="background-color: transparent; border: 0px; color: darkblue; margin: 0px; padding: 0px; vertical-align: baseline;"></span></code></pre>I found it in this stack overflow answer.</div><div><a href="http://stackoverflow.com/questions/15016376/cant-connect-to-local-mysql-server-through-socket-homebrew" target="_blank">http://stackoverflow.com/questions/15016376/cant-connect-to-local-mysql-server-through-socket-homebrew</a></div></div>

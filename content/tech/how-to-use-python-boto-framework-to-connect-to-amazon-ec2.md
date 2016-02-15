+++
title = "How to use python BOTO framework to connect to Amazon EC2 "
date = 2015-02-17T13:55:00Z
updated = 2015-02-17T13:55:47Z
tags = ["how to", "autoscaling", "Boto", "python", "cloud", "EC2", "automation"]
blogimport = true 
categories=["tech"]
[author]
	name = "Shelan Perera"
	uri = "https://plus.google.com/110975611609309023449"
+++

<div dir="ltr" style="text-align: left;" trbidi="on"><br />&nbsp;Python Boto framework is an excellent tool to automate things with Amazon. You have almost everything to automate Amazon EC2 using this comprehensive library.<br /><br />A quick guide on how to use it in your project<br /><br />1) Configure your EC2 credentials to be used by your application using one of the followings.<br /><br /><ul class="simple" style="color: #3e4349; font-family: 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, Arial, sans-serif; font-size: 14px;"><li style="line-height: 1.5em;">/etc/boto.cfg - for site-wide settings that all users on this machine will use</li><li style="line-height: 1.5em;">~/.boto - for user-specific settings</li><li style="line-height: 1.5em;">~/.aws/credentials - for credentials shared between SDKs&nbsp;</li></ul><br /><a href="http://boto.readthedocs.org/en/latest/boto_config_tut.html">http://boto.readthedocs.org/en/latest/boto_config_tut.html</a><br /><br />2) Refer the API and choose what you need to do.<br /><br /><a href="http://boto.readthedocs.org/en/latest/#currently-supported-services">http://boto.readthedocs.org/en/latest/#currently-supported-services</a><br /><br />3) Sample code for a simple autoscaler written using Boto framework. You may reuse the code in your projects quickly. This autoscaler spawn new instances based on the spike pattern of the load.<br /><br /><br /><blockquote class="tr_bq"></blockquote></div>

<script src="https://gist.github.com/shelan/b4a3f3ed0ccf9b4777e5.js"></script>

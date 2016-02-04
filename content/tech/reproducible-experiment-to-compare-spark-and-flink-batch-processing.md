+++
date = "2016-01-31T23:35:00+01:00"
draft = false
title = "Reproducible Experiment to Compare Apache Spark and Apache Flink batch processing"

+++

How do you reproduce distributed experiments? 


Have you ever experienced the pain of installing and configuring necessary 
software to run a distributed experiment.

[Karamel](http://karamel.io) comes to rescue you if you are struggling in that problem.
 
 Karamel is an orchestration engine which helps you design and run distributed experiments on the cloud such as Amazon EC2
 Google Compute Engine, Open Stack etc.It provides a convenient GUI to design reproducible experiments and also a Domain Specific Language (DSL) 
 to declare dependencies and software tools that are required to setup and run the experiments.
 This is a starting to make painful distributed experiments as easy as running it locally with a single click. How easy
 and convenient it would be for a  researcher to tune few knobs of the experiment and re run in a total different scale.
 
 Watch these two clips and experience it yourself.
 
 http://www.karamel.io/?q=content/video-tutorials
 
We recently made [Dongwong's] (http://eastcirclek.blogspot.se/2015/06/terasort-for-spark-and-flink-with-range.html) Apache Flink
 vs Apache Spark experiment reproducible on Amazon EC2. If you want to reproduce the same experiment conveniently with
 different configurations you can follow the steps mentioned [here](https://github.com/karamel-lab/batch-processing-comparison).


Following is the presentation about the results we obtained.

<iframe src="//www.slideshare.net/slideshow/embed_code/key/iORw4on0Oy1WZI" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/shelan1/apache-flink-vs-apache-spark-reproducible-experiments-on-cloud" title="Apache Flink vs Apache Spark - Reproducible experiments on cloud." target="_blank">Apache Flink vs Apache Spark - Reproducible experiments on cloud.</a> </strong> from <strong><a href="//www.slideshare.net/shelan1" target="_blank">Shelan Perera</a></strong> </div>


<h6>System level performance results of the experiments.</h6>

[200GB workload] (shelan.org/flink-spark-batch-reports/terasort-200/report_cpu.html)

[400GB workload] (shelan.org/flink-spark-batch-reports/terasort-400/report_cpu.html)

[600GB workload] (shelan.org/flink-spark-batch-reports/terasort-600/report_cpu.html)

You can find the full report of the project [here](https://www.scribd.com/doc/297923938/Apache-Spark-vs-Apache-Flink-Reproducible-Experiments-on-cloud).

<h6> Acknowledgment </h6>

[Jim Dowling] (https://www.sics.se/people/jim-dowling)

[Kamal Hakimzadeh](https://github.com/kamalhakim)

[Ashansa Perera] (https://github.com/ashansa)
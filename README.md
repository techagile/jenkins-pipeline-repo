# jenkins-pipeline-repo
A way to learn Continuous Delivery pipeline using Jenkinsfile<br>
in this demo, Jenkinsfile is setup in your code repo which runs through various stages. 
Jenkinsfile is codified using Declartive as oppose to Scripted Syntax<br> Well both type of syntax are very similar but Declartive syntax is much easier to codify<br>
<br>

Initially, the pipeline started with elementary test of stages (one at a time), then added post stage which based on the case how the pipeline resulted i.e. always, success, failure, unstable, changed 
<br><br>

Finally, a new element of making the stages run in parallel is introduced with the use of keyword 'parallel'

<br>

Additionally, the pipeline was triggered by upstream jobs thus showing value stream map, similar to GoCD
<br>
This is initial run that shows various stages and how trivial to work with Jenkinsfile. Other projects would show the real power of Jenkinsfile, using complex examples<br>
Stay tuned! <br>
<br>
References:<br>
<a href="https://www.youtube.com/watch?v=-GsvomI4CCQ">Jenkins Pipeline build & learn</a>

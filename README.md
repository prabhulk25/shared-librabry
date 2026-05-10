**How to define and use Libraries in Jenkins pipeline**

1. Create functions under the repo within "vars" folder ex: vars/greet.groovy
2. Librabries includes functions, based on the requriement define parameters for the same and that need to call from the pipeline
3. To use the librabries inside Jenkins pipeline, need to follow below steps
       1. Add librabries under Manage Jenkins > System > Global Trusted Pipeline Librabries
       2. The details required to add libraries are name(the same name should be added in the pipeline), repo url and if it is private repo then only you need to creds else you can ignore.
4. Then inorder to use librabry inside pipeline, need to add library name which you configured uder system. ex: sample-jenkinsfile

**Use Jenkinsfile from repo**

We can use Jenkins pipeline script from repo, Just we have to change the Definition of pipeline from **Pipeline Script** to **Pipeline script from SCM**
Note: Jenkins filename is need not to have as a Jenkinsfile, you can keep anything and same can be configured over job.

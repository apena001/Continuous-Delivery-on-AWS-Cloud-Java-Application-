# Continuous Delivery on AWS Cloud [Java Application]

## Flow of Execution
* Login to AWS account
* Code Commit
    * Create codecommit repo
    * Syn it with local repository
* Code Artifact
    * Create repository
    * Update settings.xml file in source code top level directory
    * update pom.xml file with repo details
    * Generate token and store in SSM parameter store
* Sonar Setup
    * Create sonar cloud account
    * Generate token and store in ssm parameter store
    * Create build project
    * Update codebuild role to access SSMparameter
* Create notification for sns or slack
* Build Project
    * Create variables in  SSM => parameter
    * Create build project
* Create Pipeline
    * Codecommit 
    * Testcode
    * Build
    * Deploy to s3 bucket
* Test Pipeline
* Create Beanstalk & RDS
* Update RDS sec grp
* Deploy DB in rds
* Switch to cd-aws branch
* Update settings.xml & pom.xml
* Create another build job to create artifact with buildspec file in cd-aws
* Create a deploy job to beanstalk
* Create a build job for software testing
* Update Pipeline
    * Codecommit
    * Testcode
    * Build & Store
    * Deploy to s3 buckect
    * Build & Release
    * Deploy to Beanstalk
    * Build job for Selenium test scripts
    * Upload result to s3
* Test Pipeline


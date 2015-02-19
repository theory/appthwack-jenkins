#appthwack-jenkins

[AppThwack](https://appthwack.com) integration with Jenkins CI.


Status
======

Latest release: v1.9  
Latest release date: 07/20/2014


Resources
=========

For more information, check out the following:

*  [AppThwack Plugin (Jenkins Wiki)](https://wiki.jenkins-ci.org/display/JENKINS/AppThwack+Plugin)
*  [Continuous Integration for Mobile Apps with AppThwack and Jenkins](http://blog.appthwack.com/continuous-integration-for-mobile-apps/)
*  [Continuous Integration for Mobile Apps with AppThwack and Jenkins (Part 2)](http://blog.appthwack.com/continuous-integration-for-mobile-apps-appthwack-jenkins-part-2/)
*  [Real Devices, Real Tests - Using a Device Cloud with Jenkins](http://blog.cloudbees.com/2014/01/real-devices-real-tests-using-device.html)


Usage
=====

*  1.) Install AppThwack Plugin

    *  a.) Navigate to *Manage Jenkins > Manage Plugins* inside your running Jenkins server.
    *  b.) Click the *Available* tab and search for *AppThwack*.
    *  c.) Install the AppThwack plugin.

*  2.) Configure System Settings

    *  a.) Navigate to *Manage Jenkins > Configure System*.
    *  b.) Enter your AppThwack API Key. This can be found on [here](https://appthwack.com/user/profile).

*  3.) Configure Project Settings

    *  a.) Navigate to your Jenkins project of choice and select *Configure* from the menu.
    *  b.) Click on the *Add post-build action* button and select *Run Tests on AppThwack*.
    *  c.) Select your AppThwack project and devicepool from the respective dropdowns.
    *  d.) Enter file pattern for finding your Application build artifact. Make sure iOS build artifacts are built with the "Pack application and build .ipa?" settings checkbox checked in the relevant Xcode build steps.
    *  e.) Select the test type you wish to use and configure it as necessary.
    *  f.) Once you're ready, hit *Save*.

*  4.)  Running Tests

    *  a.) Your build/test artifacts will automatically be uploaded to AppThwack on your next Jenkins build. AppThwack results/graphs will periodically update as tests run.


Screenshots
===========

## Add AppThwack Post-Build Step

![action](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/action.png)

## Automatically Populated Project/Device Pool Fields

![config-dropdowns](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/config-dropdowns.png)

## Most Recent Results

![recent-results](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/recent-results.png)

## Test Result Trends

![result-trends-graph](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/result-trends-graph.png)

## Automatically Downloaded Test Artifacts

![artifacts](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/artifacts.png)

## Test Performance Trends

![result-graphs](https://raw.github.com/appthwack/appthwack-jenkins/master/ext/result-graphs.png)


Dependencies
============

*  [appthwack-java](https://github.com/appthwack/appthwack-java)

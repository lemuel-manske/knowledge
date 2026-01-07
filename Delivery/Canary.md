# Canary Release

Described in [[ContinuosDelivery]] Canary release is a technique to reduce the risk of introducing a new software version in production by slowly rolling out the change to a small subset of users before rolling it out to the entire infrastructure and making it available to everybody.

When you are happy with the new version, you can start routing a few selected users to it. As you gain more confidence in the new version, you can start routing more users to the new version.

A benefit of using canary releases is the ability to do capacity testing of the new version in a production environment with a safe rollback strategy if issues are found.

> Like blue-green deployments, you need to initially deploy the new version of the application to a set of servers where no users are routed to. You can then do smoke tests and, if desired, capacity tests, on the new version. Finally, you can start to route selected users to the new version of the application. Some companies select “power users” to hit the new version of the application first. You can even have multiple versions of your application in production at the same time, routing different groups of users to different versions as required.

One drawback of using canary releases is that you have to manage multiple versions of your software at once.

Another scenario where using canary releases is hard is when you distribute software that is installed in the users' computers or mobile devices. In this case, you have less control over when the upgrade to the new version happens.


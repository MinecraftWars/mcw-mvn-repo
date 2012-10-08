mcw-mvn-repo
============

Maven repository for Minecraft-Wars Maven-enabled projects.

To deploy an artifact here, you need a local clone of this repo. Then a deployment command would look like this:

    mvn -DaltDeploymentRepository=mcw-repo::default::file:~/mcw-mvn-repo/releases clean deploy

or for snapshots:

    mvn -DaltDeploymentRepository=snapshot-repo::default::file:~/mcw-mvn-repo/snapshots clean deploy


To deploy a third party jar, for example Factions:

    mvn deploy:deploy-file -DgroupId=massivecraft -DartifactId=factions -Dversion=1.7.6pre -Dpackaging=jar -Dfile=factions-1.7.6pre.jar -DrepositoryId=mcw-repo -Durl=file:~/mcw-mvn-repo/releases

In all cases, paths need to be adjusted.
Then the updates need to be pushed :)


This is a demo of the JavaSpace 'notify' functionality.

Written by Dr Gary Allen, University of Huddersfield.

Updated to Apache River 3.0


There are two versions of a JavaSpace 'hello world' program:

The first (HelloWorldSpace) simply writes an object to the space and then reads it back again.  This is really just for comparison to the second version.

The second (HelloWorldNotify) adds a listener to the space, then writes an object.  The space the notifies the code that the object has arrived, and the object is read back again.

As usual, if using an IDE like IntelliJ or eclipse you need to create a java project with the correct classes added as libraries, then paste the code in and run it.
You also need to create a Run Configuration and pass the correct VM arguments in order to get the 'notify' version of the code to run.  Add this:

    -Djava.rmi.server.useCodebaseOnly=false  -Djava.security.policy=policy.all

to the VM args of the Run Configuration.

NOTE - All paths mentioned here assume running the code on the university linux network.  If at home you need to amend the paths accordingly.



If running from a command line, set up the classpath with:

	. jinicl

then compile with:

	javac *.java

and run the simple version with:

	java HelloWorldSpace

Then run the 'notify' version with:

    java -Djava.rmi.server.useCodebaseOnly=false  -Djava.security.policy=policy.all HelloWorldNotify

OR by running the above command as a script:

    RunHelloWorldNotify

Look at the code, which has extensive comments, to see what is happening.



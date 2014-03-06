usage
=====
build
-----
Running the build command will pull the latest crdb source (into a crdb subdirectory) and configure the container for use (including a bundle install):

`$ sudo ./build`

run
---
After the build has completed, you can now run the container.

The run command will start the container and display the output to the screen (good for troubleshooting):

`$ sudo ./run`

You can also run the container as a daemon:

`$ sudo ./daemon`

If you need to make changes in the container before starting the WEBrick server:

`$ sudo ./shell`

changing branch
---------------
You may want to run an alternative branch for testing, this should be done sometime AFTER you run your first build.

Go in to the crdb source directory:

`$ cd crdb`

Change to the desired branch (Note this must be run as root since the source was originally downloaded using sudo):

`$ sudo git checkout other_branch`

Navigate back to the docker/crdb directory:

`$ cd ..`

Build and run:

`$ sudo ./build && sudo ./run`

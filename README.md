# dockerNodew
A script to run node scripts or npm commands in a docker container for portability. Put this script in your project and then use it in place of the npm and node binaries if you don't want to manage your own node environment (or on a build server).

Usage Examples: 

    ./dockerNodew npm install
    ./dockerNodew path/to/file.js

The user running the command and group are dynamically added in the container so file permissions are correct from an npm install.  

Also the node version to use will be picked up from a .nvmrc file or the NODE_VERSION environment variable or fallback to a default if not specified.

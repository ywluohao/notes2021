

To start in Linux/macOS:

- To run NiFi in the **foreground**, run `bin/nifi.sh run`. This will leave the application running until the user presses `Ctrl-C`. At that time, it will initiate shutdown of the application.

- To run NiFi in the **background**, instead run `bin/nifi.sh start`. This will initiate the application to begin running. To check the status and see if NiFi is currently running, execute the command `bin/nifi.sh status`. NiFi can be shutdown by executing the command `bin/nifi.sh stop`.
- Issuing `bin/nifi.sh start` executes the `nifi.sh` script that starts NiFi in the background and then exits. If you want `nifi.sh` to wait for NiFi to finish scheduling all components before exiting, use the `--wait-for-init` flag with an optional timeout specified in seconds: `bin/nifi.sh start --wait-for-init 120`. If the timeout is not provided, the default timeout of 15 minutes will be used.
- If NiFi was installed with **Homebrew**, run the commands `nifi start` or `nifi stop` from anywhere in your file system to start or stop NiFi.

To get started, open a web browser and navigate to [`http://localhost:8080/nifi`](http://localhost:8080/nifi). The port can be changed by editing the `nifi.properties` file in the NiFi `conf` directory, but the default port is 8080.




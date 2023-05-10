# Capstone-Project3
##  Anti-pattern detection in Jaeger/Grafana tracking tool for microservices: Jaeger/Grafana Plugin
For our group, we picked the [Train-Ticket](https://github.com/FudanSELab/train-ticket) Microservice OSS Project.

## Team
Team Leader: `Eric Jaroszewski`

Team Members: `Evan Berryman`,`Yangzekun Gao`,`Zhengyan Hu`,`Maiqi Hou`

---
## Log Trace File
___Make sure you have deployed Train-ticket and Jaeger before you run this executable file___

Our group provides a `Jaeger Tracing.exe` to help users to trace each microservices and comprehensive a completed local file. 
__If the exectuable file has some problem, please open the Python Program and run app.py___

Once you open the executable file, it allows users to enter an IP address and a port, which is the IP and port of your developed Jaeger.
We also offer two options for tracing mode: `5m`-traceing recently 5 minutes data and `ALL`-tracing data within 2 days.

![exefile](https://github.com/EJaro00/CapSP3-JaegerGrafana-Plugin/blob/main/IMG/1.png)

After you enter the above information, you should access http://localhost:5000 in your browser. If it show a "Hello, World" page, this means that `Jaeger Tracing.exe` has run successfully and it can trace microservices data now.

![exefile1](https://github.com/EJaro00/CapSP3-JaegerGrafana-Plugin/blob/main/IMG/2.png)

Now you can access using http://localhost:5000/logging and it is your tracing file. All of our Grafana data source get their data from this URL.

![exefile2](https://github.com/EJaro00/CapSP3-JaegerGrafana-Plugin/blob/main/IMG/3.png)

---
## Grafana panel
___Make sure you have run `Jaeger Tracing.exe` first___

* Prerequisites
    1. Grafana: higher than 7.0.0 (For my Grafana version is 9.3.6)
    2. NodeJS:  >= 14 (16 Recommanded for Ubuntu 22.04 LTS)
    3. yarn 
* **If you NodeJS version lower than 14, you many follow next command:**
    1. Remove nodejs that you have already installed
    ```bash
    sudo apt-get remove nodejs
    ```
    2. add Node.js v16.x repositories:
    ```bash
    curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
    ```
    3. Re-install node.js
     ```bash
    sudo apt-get install nodejs
    ```

Download the train-ticket-plugin folder, using VS code open it, and call the terminal to run these commands.
1. Install dependencies

   ```bash
   yarn install
   ```

2. Build plugin in development mode or run in watch mode

   ```bash
   yarn watch
   ```

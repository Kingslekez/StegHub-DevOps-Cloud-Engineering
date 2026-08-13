Importing the GPG keyring ensures the downloaded MongoDB installation packages are authentic and cryptographically signed.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Installing%20gnupgcurl%2C%20adding%20MongoDB%20PGP%20key.png)

Adding the repository URL to <mark>sources.list.d</mark> enables APT to find and fetch official MongoDB software packages.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Adding%20MongoDB%207.0%20apt%20repository%20source%20list.png)

Running <mark>apt-get install</mark> downloads and sets up the core MongoDB server along with its associated command-line tools.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Running%20apt%20update%2C%20installing%20mongodb-org%20packages%20successfully.png)

Displaying <mark>--version</mark> confirms the MongoDB binary installed correctly and reveals the specific release details and architecture.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Checking%20installed%20mongod%20version%207.0.40%20confirmed.png)

The <mark>systemctl</mark> command starts the database daemon and displays its current running state and system process ID.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Starting%20mongod%20service%2C%20confirming%20active%20running%20status.png)

Initializing <mark>npm init</mark> creates the foundational <mark>package.json</mark> file needed to manage dependencies for a Node.js project.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Installing%20body-parser%2C%20initializing%20new%20Books%20npm%20project.png)

Viewing <mark>server.js</mark> shows the Node.js backend configuration, including Express middleware routing and the local Mongoose connection.

![image alt](https://github.com/Kingslekez/StegHub-DevOps-Cloud-Engineering/blob/404a0cbac882edad931b0185bf2f7c8fe6e225cc/MEAN%20STACK/Images/Editing%20server.js.%20Express%2C%20Mongoose%2C%20MongoDB%20connection%20setup.png)
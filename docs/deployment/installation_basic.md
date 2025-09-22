## Basic Installation

### Step 1
The only pre-requisite to run your own instance of ATON on your machine is [Node.js](https://nodejs.org/). You can install it on Windows, Linux, and Mac OS.

<p align="center">
    <a href = "https://nodejs.org/en" target="_blank">
        <img src="/assets/Node.js-logo.png" alt="Node.js" width="200"/>
    </a>
</p>

### Step 2
Download a copy of ATON framework from [GitHub](https://github.com/phoenixbf/aton) or grab the zip package. If you are not so familiar with git, dont worry: just grab the [zip](https://codeload.github.com/phoenixbf/aton/zip/refs/heads/master) and extract somewhere on your machine. In general however, the best solution is to git clone the repository: this allows you to periodically update your instance without messing with your custom configuration.

To clone the repository using the terminal run:
```
git clone https://github.com/phoenixbf/aton.git
``` 

<p align="center">
    <a href = "https://osiris.itabc.cnr.it/aton/" target="_blank">
        <img src="/assets/aton-logo.png" alt="ATON" width="150"/>
    </a>
</p>


### Step 3
Download a copy of THOTH from [Github](https://github.com/Xenobii/thoth_v2) and place it in the /wapps folder located directly inside the aton folder. Similarly to ATON, either download the [zip](https://github.com/Xenobii/thoth_v2) or clone the repository inside the wapps folder. 
```
git clone https://github.com/Xenobii/thoth_v2.git
```

<p align="center">
    <a href = "https://github.com/Xenobii/thoth_v2" target="_blank">
        <img src="/assets/thoth-logo.png" alt="THOTH" width="150"/>
    </a>
</p>

### Step 4
Launch **setup.bat** (Windows) or execute **setup.sh** (Linux and Mac OS) from the ATON main folder. Alternatively, open your terminal, go to the main ATON folder (`cd /your/ATON/folder/`) and just type this command:

```
npm install
```

This installs and updates all node.js modules required by ATON.

### Step 5
Once you have installed all the above prerequisites, you can launch the main ATON service by launching **quickstart.bat** (Windows) or **quickstart.sh** (Linux or Mac OS). Alternatively, you can run the following command from your terminal:
```
npm start
```

This will run and deploy a basic instance of ATON on your machine.

To verify everything runs properly, navigate to [http://localhost:8080/](http://localhost:8080/) on your web browser. 
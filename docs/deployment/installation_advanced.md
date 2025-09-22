## Advanced Installation

In order to install ATON and THOTH using this method, you must first follow the steps shown in the [Basic Installation section](./installation_basic.md) first.

<p align="center">
    <a href = "https://pm2.keymetrics.io/" target="_blank">
        <img src="/assets/pm2-logo.png" alt="PM2" width="400"/>
    </a>
</p>

To install PM2 (on any OS) you should just type on command-line:

```
npm install pm2 -g
```

On debian-based systems (Linux OS servers) you should use sudo before the command, in order to install PM2 globally.

Now, you can simply run and deploy all ATON services by typing (from main folder):

```
pm2 start
```

Finally, if you want to stop all services, you can type:

```
pm2 stop all
```
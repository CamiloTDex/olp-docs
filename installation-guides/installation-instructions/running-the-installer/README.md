# Running the Installer

Before starting installation, ensure that you have at hand your api-key, as we are in beta phase, only the allowed keys will be able to install the node.

#### Installing the node as a service (Linux only) (Recommended)

In order to install the node as a service, execute the following commands:

```
npm i -g @olptools/cli
sudo olp-cli install --service <your-api-key>
```

Installing the node as a service will automatically run, update and restart the node whenever a new version is available.  The process will be started in background and will be available to manage as a regular linux service.

#### Installing the node for running manually

In order to install the node, execute the following commands:

```
npm i -g @olptools/cli
sudo olp-cli install <your-api-key>
```

It will output a set of URLs, go to the public URL of your server (typically the last one) in order to continue the process.

```
[Wed, 07 Dec 2022 21:34:15 GMT] Cloning git@bitbucket.org:CamiloTDex/olp-installation-wizard.git into /usr/local/share/.config/yarn/global/node_modules/@olptools/cli/olp-installation-wizard
[Wed, 07 Dec 2022 21:34:15 GMT] Please continue the installation in one of the following urls:
[Wed, 07 Dec 2022 21:34:15 GMT] · http://172.17.0.1:7577
[Wed, 07 Dec 2022 21:34:15 GMT] · http://10.142.0.20:7577
[Wed, 07 Dec 2022 21:34:15 GMT] · http://127.0.0.1:7577
[Wed, 07 Dec 2022 21:34:15 GMT] · http://35.237.53.7:7577
```

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

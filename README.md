## Mycroft alternatives repo

This is an alternative debian repository for the Mycroft Mark-1


### Add repo to a device
To add the repo to your device ssh into it or connect a screen and keyboard perform the following operations:

#### Add the public key
To make sure the repo is trusted by the OS add the public key:

```
wget -O - http://forslund.github.io/mycroft-alternatives/conf/mycroft-alternatives.gpg.key | sudo apt-key add -
```

#### Add repository
Add the repo to the list of available repositories:

```
echo "deb http://forslund.github.io/mycroft-alternatives jessie main" | sudo tee /etc/apt/sources.list.d/mycroft.alternatives.list
sudo apt-get update
```

Now packages can be installed from the repostiory. Try for example

```
sudo apt-get install mycroft-python
```

# openfaas-identicon
> OpenFaaS function to generation Identicons

This is a simple [FaaS](https://github.com/openfaas/faas) function inspired by Bart Fokker's [post](https://blog.bartfokker.nl/identicon/).  This is a forked and updated version of [the original](https://github.com/ganesshkumar/openfaas-identicon).

## Prerequisite
* Make sure you have deployed OpenFaaS using the instructions in the [OpenFaaS docs](https://docs.openfaas.com/deployment/).
* Install [faas-cli](https://docs.openfaas.com/cli/install/)

## Usage

**Deploy the pre-built function**
```
$ export OPENFAAS_URL=http://127.0.0.1:8080

$ faas deploy
```

**Build and deploy**
```
$ export OPENFAAS_URL=http://127.0.0.1:8080

$ DOCKER_USER=<your_Docker_user> faas up
```
> Note: Ensure you're logged in to Docker hub

**Test the function**
```
$ curl -sSL "${OPENFAAS_URL}/function/identicon" --data "rgee0" \
> sample/rgee0.png
```

![Sample image generated for OpenFaaS](sample/openfaas.png)

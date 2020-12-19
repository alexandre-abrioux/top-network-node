#  Top Network Node :whale: Dockerized

> Disclaimer: I am not currently running any Top Network Node on the mainnet.
> This was a POC (Proof of Concept) for my own research,
> this is why this project has been archived and won't receive any update.

## :link: Links

- [Top Network > Website](https://www.topnetwork.org/)
- [Top Network > Topio Documentation](http://developers.topnetwork.org/en/Tools/TOPIO/Command-line_Options/)

## :arrow_forward: Usage

You can clone this repository or use the provided `docker/Dockerfile` and `docker-compose.yml` as a base template for your own setup.

A `Makefile` is included for convenience but `make` is not required to run the node.

Use `make` or `make help` to list the available shortcuts.

### 1. Setup

Use `make wallet` and `make key` to create your wallet and node key.

The data will be persisted on your host in a `./data-node` repository.

### 2. Fill up the environment variables

Complete the `.env` file with the information generated in the previous step.
You can also add a custom name to your node via the `TOPIO_NODE_NAME` environment variable.

### 3. Run the Node

Use `make up` to start the node in a detached mode.

You can access the logs at any time by running `make logs`.

## Donation :beer:

If you find this template useful you may consider the option of offering me a beer through a donation. Support is very appreciated :slightly_smiling_face:

ETH / ERC20 Token: `0x18f199E8DAb38257ca84D4858FF6F73De1A697eA`

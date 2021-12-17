# name-block

**A balenaBlock for fun device renaming**

## Highlights

- **Bored of your device names?**: Let this block rename them for you!
- **Loads of categories**: From rude names to pirates names, there's something for everyone!
- **Contribute categories**: We're open to fun and entertaining categories, PRs are welcome!

## Setup and configuration

Use this as standalone functionality with the button below:

[![template block deploy with balena](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/bucknalla/name-block)

Or add the following service to your `docker-compose.yml`:

```yaml
version: '2'
services:
  name:
    image: ghcr.io/bucknalla/name-block
    restart: no # required to avoid container restarting indefinitely
    labels:
      io.balena.features.balena-api: 1 # required to use the balena API
    environment:
      CATEGORY: pirate # if not specified will default to season
      DEBUG: name # not required unless debugging
```

If you don't like the name we've chosen for your device, you can navigate to the `device variables` tab on balenaCloud and delete the `NAME` variable.
Restarting the name-block service will then prompt the block to generate a new name.

## Warning

You may find some of the names generated by this block to be rude... this is intentional.
However, we do not tolerate discrimination of any sort and as such contributions that are themed this way will not be accepted.

## Documentation

Head over to our [docs](https://github.bucknalla.io/name-block/docs/) for detailed installation and usage instructions, customization options and more!

## Motivation

After a while, balenaCloud-generated device names get boring... why not spice it up with some new categories!

- Rude
- Pirate
- Seasonal
- Custom URLs
- More to come!

## Getting Help

If you're having any problem, please [raise an issue](https://github.com/bucknalla/name-block/issues/new) on GitHub and we will be happy to help.

## Contributing

Do you want to help make name-block better? Take a look at our [Contributing Guide](https://github.bucknalla.io/name-block/contributing). Hope to see you around!

## License

name-block is free software, and may be redistributed under the terms specified in the [license](https://github.com/bucknalla/name-block/blob/master/LICENSE).

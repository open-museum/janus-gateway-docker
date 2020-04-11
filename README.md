# Janus Gateway Docker

Docker for [Janus](https://janus.conf.meetecho.com/), the general purpose WebRTC server.

[<img src="android-chrome-512x512.png" align="right" width="100">](https://open-museum.github.io/janus-gateway-docker/)

[![GitHub issues](https://img.shields.io/github/issues/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/issues)
[![GitHub forks](https://img.shields.io/github/forks/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/network)
[![GitHub stars](https://img.shields.io/github/stars/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/stargazers)
[![GitHub license](https://img.shields.io/github/license/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/blob/master/LICENSE.md)

## Installation

Edit `/src/conf/janus.jcfg` to your liking. Take special care to enable/disable the plugins:

```text
# You can choose which of the available plugins should be
# enabled or not. Use the 'disable' directive to prevent Janus from
# loading one or more plugins: use a comma separated list of plugin file
# names to identify the plugins to disable. By default all available
# plugins are enabled and loaded at startup.
plugins: {
	#disable = "libjanus_voicemail.so,libjanus_recordplay.so"
	disable = "libjanus_nosip.so,libjanus_recordplay.so,libjanus_sip.so,libjanus_streaming.so,libjanus_textroom.so,libjanus_videocall.so,libjanus_videoroom.so,libjanus_voicemail.so"
````

Use [Docker](https://www.docker.com/) to build the image.

```bash
docker build -t openmuseum/janus-gateway-docker ./src/.
```

## Usage

```bash
docker-compose up -d
```

## Support

This project is maintained by [@maehr](https://github.com/maehr). Please understand that we won't be able to provide individual support via email. We also believe that help is much more valuable if it's shared publicly, so that more people can benefit from it.

| Type                   | Platforms                                                    |
| ---------------------- | ------------------------------------------------------------ |
| 🚨 **Bug Reports**      | [GitHub Issue Tracker](https://github.com/open-museum/janus-gateway-docker/issues) |
| 🎁 **Feature Requests** | [GitHub Issue Tracker](https://github.com/open-museum/janus-gateway-docker/issues) |
| 🛡 **Report a security vulnerability**      | [GitHub Issue Tracker](https://github.com/open-museum/janus-gateway-docker/issues) |

## Roadmap

No changes are currently planned.

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/open-museum/janus-gateway-docker/tags).

## Authors and acknowledgment

- **Moritz Mähr** - _Initial work_ - [maehr](https://github.com/maehr)

See also the list of [contributors](https://github.com/open-museum/janus-gateway-docker/graphs/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

All emojis designed by [OpenMoji](https://openmoji.org/) – the open-source emoji and icon project. License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/#)
# Janus Gateway Docker

[Janus](https://janus.conf.meetecho.com/) the general purpose WebRTC server.

[<img src="android-chrome-512x512.png" align="right" width="100">](https://open-museum.github.io/janus-gateway-docker/)

[![GitHub issues](https://img.shields.io/github/issues/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/issues)
[![GitHub forks](https://img.shields.io/github/forks/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/network)
[![GitHub stars](https://img.shields.io/github/stars/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/stargazers)
[![GitHub license](https://img.shields.io/github/license/open-museum/janus-gateway-docker.svg)](https://github.com/open-museum/janus-gateway-docker/blob/master/LICENSE.md)

## Installation

Create certificates in `/example/certificates/`.

Copy the config files in `/example/conf/`.

```bash
cd example/conf/
cp janus.eventhandler.sampleevh.jcfg.sample janus.eventhandler.sampleevh.jcfg
cp janus.eventhandler.wsevh.jcfg.sample janus.eventhandler.wsevh.jcfg
cp janus.jcfg.sample janus.jcfg
cp janus.plugin.audiobridge.jcfg.sample janus.plugin.audiobridge.jcfg
cp janus.plugin.echotest.jcfg.sample janus.plugin.echotest.jcfg
cp janus.plugin.nosip.jcfg.sample janus.plugin.nosip.jcfg
cp janus.plugin.recordplay.jcfg.sample janus.plugin.recordplay.jcfg
cp janus.plugin.sip.jcfg.sample janus.plugin.sip.jcfg
cp janus.plugin.streaming.jcfg.sample janus.plugin.streaming.jcfg
cp janus.plugin.textroom.jcfg.sample janus.plugin.textroom.jcfg
cp janus.plugin.videocall.jcfg.sample janus.plugin.videocall.jcfg
cp janus.plugin.videoroom.jcfg.sample janus.plugin.videoroom.jcfg
cp janus.plugin.voicemail.jcfg.sample janus.plugin.voicemail.jcfg
cp janus.transport.http.jcfg.sample janus.transport.http.jcfg
cp janus.transport.pfunix.jcfg.sample janus.transport.pfunix.jcfg
cp janus.transport.websockets.jcfg.sample janus.transport.websockets.jcfg
```

Edit the files:

* Enable secure transport protocols in `janus.jcfg`, `janus.transport.http.jcfg` and `janus.transport.websockets.jcfg` and set `cert_pem = "/usr/share/certificates/cert.pem"`and `cert_key = "/usr/share/certificates/key.pem"`
* Set `stun_server = "stun.l.google.com"`and `stun_port = 19302` in `janus.jcfg`
* Disable unused plugins in `janus.jcfg`

Use [Docker](https://www.docker.com/) to build the image.

```bash
cd example
docker build .
```

## Usage

```bash
cd example
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

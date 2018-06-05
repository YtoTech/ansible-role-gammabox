# Ansible role : Gamma Box

[![Build Status](https://travis-ci.org/YtoTech/ansible-role-gammabox.svg?branch=master)](https://travis-ci.org/YtoTech/ansible-role-gammabox)

Ansible role for installing the [Gamma Box](https://github.com/MonsieurV/GammaBox) on a Raspberry Pi (Raspbian).

## Requirements

A Raspberry Pi with Raspbian, accessible from SSH.

## Role Variables

| Variable      | Use           | Default to  |
| ------------- |:-------------:| -----:|
| `gammabox_path` | Where to checkout and install the Gamma Box code | `/home/pi/.gammebox/GammaBox` |
| `gammabox_web.port` | The port on which to run the HTTP Gamma Box web server and API | `80` |

## Example Playbook

To deploy the Gamma Box on the `8080` port of your `rpi` host:

```
- name: Deploy Gamma Box on my RPi
  hosts: rpi
  tasks:
    - name: GammaBox@rpi deploy
      include_role:
        name: gammabox
      vars:
        gammabox_web:
          port: 8080
```

## License

MIT

## Author Information

[Yoan Tournade](mailme:yoan@ytotech.com) @ YtoTech
https://blog.ytotech.com

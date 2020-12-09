# Ansible Role: ansible-apps_kafka_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_kafka_exporter.svg?branch=master)](https://travis-ci.com/lotusnoir/ansible-apps_kafka_exporter)[![License](https://img.shields.io/badge/license-MIT%20License-brightgreen.svg)](https://opensource.org/licenses/MIT)[![Ansible Role](https://img.shields.io/badge/ansible%20role-apps__kafka_exporter-blue)](https://galaxy.ansible.com/lotusnoir/ansible-apps_kafka_exporter/)[![GitHub tag](https://img.shields.io/badge/version-latest-blue)](https://github.com/lotusnoir/ansible-apps_kafka_exporter/tags)

Deploy [kafka_exporter](https://github.com/danielqsj/kafka_exporter/) to expose kafka metrics to prometheus.

## Role variables

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `kafka_exporter_version` | 1.2.0 | kafka_exporter version |
| `kafka_exporter_temp_dir` | /tmp | temporary directory to uncompress package |
| `kafka_exporter_install_dir` | /usr/local/bin | directory to install binary |
| `kafka_exporter_force_install` | false | force install variable |
| `kafka_exporter_port` | 9102 | port to expose prometheus metrics |

## Examples

	---
	- hosts: apps_kafka_exporter
	  become: yes
	  become_method: sudo
	  gather_facts: yes
	  roles:
	    - role: ansible-apps_kafka_exporter
	  environment: 
	    http_proxy: "{{ http_proxy }}"
	    https_proxy: "{{ https_proxy }}"
	    no_proxy: "{{ no_proxy }}

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

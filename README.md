# Ansible Role: ansible-apps_kafka_exporter

## Description

[![Build Status](https://travis-ci.com/lotusnoir/ansible-apps_kafka_exporter.svg?branch=master?style=flat)](https://travis-ci.com/lotusnoir/ansible-apps_kafka_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)
[![Ansible Role](https://img.shields.io/badge/galaxy-apps_kafka_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_kafka_exporter?color=orange&style=flat)
![Ansible Quality Score](https://img.shields.io/ansible/quality/52300)
[![downloads](https://img.shields.io/ansible/role/d/52300)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_kafka_exporter.svg)](https://github.com/lotusnoir/ansible-apps_kafka_exporter/releases/)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kafka_exporter&metric=alert_status)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kafka_exporter)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kafka_exporter&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kafka_exporter)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kafka_exporter&metric=reliability_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kafka_exporter)
[![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=lotusnoir_ansible-apps_kafka_exporter&metric=security_rating)](https://sonarcloud.io/dashboard?id=lotusnoir_ansible-apps_kafka_exporter)


Deploy [kafka_exporter](https://github.com/danielqsj/kafka_exporter/) to expose kafka metrics to prometheus.

## Role variables

| Name                           | Default Value  | Description                        |
| ------------------------------ | -------------- | -----------------------------------|
| `kafka_exporter_version`       | 1.2.0          | kafka_exporter version |
| `kafka_exporter_temp_dir`      | /tmp           | temporary directory to uncompress package |
| `kafka_exporter_install_dir`   | /usr/local/bin | directory to install binary |
| `kafka_exporter_force_install` | false          | force install variable |
| `kafka_exporter_port`          | 9102           | port to expose prometheus metrics |

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

## Prometheus rules

TODO

## Grafana dashboard

A sample dashboard is available here: [https://grafana.com/grafana/dashboards/13572](https://grafana.com/grafana/dashboards/13572)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

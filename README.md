# ansible-apps_kafka_exporter

[![Galaxy Role](https://img.shields.io/badge/galaxy-apps_kafka_exporter-purple?style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
[![Version](https://img.shields.io/github/release/lotusnoir/ansible-apps_kafka_exporter.svg)](https://github.com/lotusnoir/ansible-apps_kafka_exporter/releases/latest)
[![GitHub repo size](https://img.shields.io/github/repo-size/lotusnoir/ansible-apps_kafka_exporter?color=orange&style=flat)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
[![downloads](https://img.shields.io/ansible/role/d/52269)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
[![Ansible Quality Score](https://img.shields.io/ansible/quality/52269)](https://galaxy.ansible.com/lotusnoir/apps_kafka_exporter)
[![License](https://img.shields.io/badge/license-Apache--2.0-brightgreen?style=flat)](https://opensource.org/licenses/Apache-2.0)

## Description

Deploy [kafka_exporter](https://github.com/danielqsj/kafka_exporter/) to expose kafka metrics to prometheus.
## Requirements

none

## Role variables

See [variables](/defaults/main.yml) for more details.

## Examples

        ---
        - hosts: apps_kafka_exporter
          become: true
          become_method: sudo
          gather_facts: true
          roles:
            - role: ansible-apps_kafka_exporter

## Grafana Dashboard

You can find a grafana dashboard [here](https://grafana.com/grafana/dashboards/13572)

## License

This project is licensed under Apache License. See [LICENSE](/LICENSE) for more details.

## Author Information

- [Philippe LEAL](https://github.com/lotusnoir)

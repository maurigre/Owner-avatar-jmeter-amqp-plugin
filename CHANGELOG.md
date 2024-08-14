# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Dependency Updates

* Up amqp-client version to 5.20.0.

## [0.3.0]

> 2023-09-27

Minor release with some new features, bug fixes, UI improvements, and dependency upgrades.

### Added

* `App_id` message property for AMQP Publisher [#29](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/29) (see [jlavallee#37](https://github.com/jlavallee/JMeter-Rabbit-AMQP/issues/37)).
* `Timestamp` message property for AMQP Publisher [#50](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/50) (see [jlavallee#37](https://github.com/jlavallee/JMeter-Rabbit-AMQP/issues/37)).
* Help link on the title panel in AMQP Publisher and Consumer samplers.

### Fixed

* Fix error on JMeter startup caused by manifest absence [#48](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/48). Thanks to [@AbstractBike](https://github.com/AbstractBike).
* `setResponseData` removed from AMQP Publisher.
* `setSamplerData` removed from AMQP Consumer.

### Infra

* Release action workflow added.
* Java 21 added to CI workflow.

### Dependency Updates

* Up jmeter-core version to 5.6.2.
* Up amqp-client version to 5.18.0.

## [0.2.0]

> 2022-08-02

Update RabbitMQ amqp-client from 4.x to 5.x.\
Look into [changes between 4.x.x and 5.0.0](https://github.com/rabbitmq/rabbitmq-java-client/releases/tag/v5.0.0) for details.

### Changed

* RabbitMQ amqp-client compatibility bumped from 4.x.x to 5.x.x [#8](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/8). Thanks to [@t-h-e](https://github.com/t-h-e).
* Single jar with dependencies provided as release artifact [#1](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/1).

### Fixed

* NullPointerException on purging queue in AMQP Consumer [#10](https://github.com/aliesbelik/jmeter-amqp-plugin/pull/10). Thanks to [@t-h-e](https://github.com/t-h-e).

### Infra

* CodeQL and SonarCloud analysis workflows added.

### Dependency Updates

* Up jmeter-core version to 5.5.
* Up amqp-client version to 5.15.0.

## [0.1.0]

> 2022-01-15

Initial release.

### Added

* `Content-encoding` message property (for AMQP Publisher). Thanks to [@gybandi](https://github.com/gybandi).
* Queue `x-max-priority` & message `priority` parameters (see [jlavallee#42](https://github.com/jlavallee/JMeter-Rabbit-AMQP/pull/42)). Thanks to [@gregLibert](https://github.com/gregLibert), [@looseend](https://github.com/looseend).
* Request (for AMQP Publisher) and response (for AMQP Consumer) headers.
* Option to configure transactional AMQP consumer from the UI (see [jlavallee#38](https://github.com/jlavallee/JMeter-Rabbit-AMQP/pull/38)). Thanks to [@nicklascarnegie](https://github.com/nicklascarnegie).
* `Auto-delete` property for exchange (see [jlavallee#33](https://github.com/jlavallee/JMeter-Rabbit-AMQP/pull/33)). Thanks to [@wneild](https://github.com/wneild).
* `Heartbeat` option (see [zeph1rus/JMeter-Rabbit-AMQP@efddefa](https://github.com/zeph1rus/JMeter-Rabbit-AMQP/commit/efddefad62aa54eed4a96dd4cc0b9fe2fb040e1a)). Thanks to [@zeph1rus](https://github.com/zeph1rus).
* Jar with dependencies.
* Extra exception handling.

### Changed

* Samplers configuration screens adjusted.
* Example scenario updated.
* Switch to SLF4J API for logging.
* Code cleanup.

### Fixed

* No header in `reply-to` message issue (see [jlavallee#41](https://github.com/jlavallee/JMeter-Rabbit-AMQP/issues/41)). Thanks to [@gregLibert](https://github.com/gregLibert).
* Checkstyle issues.

### Infra

* Maven instead of ant & ivy.
* Switch to maven directory layout.

### Dependency Updates

* Up jmeter-core version to 5.4.3.
* Up amqp-client version to 4.12.0.
* Redundant dependencies removed.

[Unreleased]: https://github.com/aliesbelik/jmeter-amqp-plugin/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/aliesbelik/jmeter-amqp-plugin/releases/tag/v0.3.0
[0.2.0]: https://github.com/aliesbelik/jmeter-amqp-plugin/releases/tag/v0.2.0
[0.1.0]: https://github.com/aliesbelik/jmeter-amqp-plugin/releases/tag/v0.1.0

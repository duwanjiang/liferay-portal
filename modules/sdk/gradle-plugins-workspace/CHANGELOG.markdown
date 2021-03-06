# Liferay Gradle Plugins Workspace Change Log

## 1.0.41 - 2016-09-26

### Changed
- [LPS-66853]: Update the [Liferay Gradle Plugins] dependency to version 2.0.41.
- [LPS-67656]: Use Liferay 7.0.2 GA3 by default.

## 1.1.0 - 2016-09-28

### Added
- [LPS-68293]: Add support for WAR projects, contained in the `wars` directory
of a Liferay Workspace. For each WAR project, the following configuration is
applied:
	- applies the [`war`](https://docs.gradle.org/current/userguide/war_plugin.html)
	plugin
	- adds a `deploy` task
	- configures the `distBundleTar` and `distBundleZip` task to save the
	generated WAR file in the `osgi/war` directory of the bundle

### Changed
- [LPS-67352]: Update the [Liferay Gradle Plugins] dependency to version 2.0.45.
- [LPS-67573]: Make most methods private in order to reduce API surface.

## 1.2.0 - 2016-10-24

### Added
- [LPS-68293]: Add the [Liferay CDN](https://cdn.lfrs.sl/repository.liferay.com/nexus/content/groups/public)
as default repository in WAR projects. This behavior can be disabled by setting
the `liferay.workspace.wars.default.repository.enabled` property in
`gradle.properties` to `false`.
- [LPS-68822]: Add the ability to specify a root directory for the archives
generated by the `distBundleTar` and `distBundleZip` tasks via the
`liferay.workspace.bundle.dist.root.dir` property in `gradle.properties`.

### Changed
- [LPS-66906]: Update the [Liferay Gradle Plugins] dependency to version 3.0.23.

### Fixed
- [LPS-68849]: Preserve last modified times and empty directories in the outputs
of the `distBundleTar`, `distBundleZip`, and `initBundle` tasks.
- [LPS-68849]: Fix overwriting bundle files through the `configs` directory.

## 1.2.1 - 2016-11-30

### Added
- [LPS-68849]: Apply [`LifecycleBasePlugin`](https://docs.gradle.org/current/javadoc/org/gradle/language/base/plugins/LifecycleBasePlugin.html)
to the root project.
- [LPS-69473]: Add the Maven central repository (if enabled) as the first
default repository for module and WAR projects.

### Changed
- [LPS-69445]: Update the [Liferay Gradle Plugins] dependency to version 3.0.43.

### Fixed
- [LPS-69294]: Include theme and WAR files inside the archives generated by the
`distBundleTar` and `distBundleZip` tasks.

## 1.2.2 - 2016-12-06

### Changed
- [LPS-69501]: Update the [Liferay Gradle Plugins] dependency to version 3.0.47.

## 1.2.3 - 2017-01-27

### Changed
- [LPS-70282]: Update the [Liferay Gradle Plugins] dependency to version 3.1.2.

## 1.2.4 - 2017-01-30

### Changed
- [LPS-70336]: Update the [Liferay Gradle Plugins] dependency to version 3.1.3.
- [LPS-70353]: Update the [Gradle Download Task] dependency to version 3.2.0.
- [LPS-70362]: Use the Liferay CDN to download bundles by default.

## 1.2.5 - 2017-02-08

### Changed
- [LPS-70515]: Update the [Liferay Gradle Plugins] dependency to version 3.1.8.

## 1.3.0 - 2017-02-27

### Added
- [LPS-70677]: Add the ability to precompile the JSP files of OSGi modules via
the `liferay.workspace.modules.jsp.precompile.enabled` property in
`gradle.properties`.

### Changed
- [LPS-66853]: Update the [Liferay Gradle Plugins] dependency to version 3.2.9.

### Fixed
- [LPS-67573]: Move all properties available in the `gradle.liferayWorkspace`
extension object into the public API.

## 1.4.0 - 2017-05-05

### Added
- [LPS-71724]: Add the ability to download and upgrade the Plugins SDK
directories by executing the `upgradePluginsSDK` task in the root project.
- [LPS-71724]: Add [Liferay CDN](https://cdn.lfrs.sl/repository.liferay.com/nexus/content/groups/public)
as the default repository in the root project. This behavior can be disabled by
setting the `liferay.workspace.default.repository.enabled` property to `false`
in `gradle.properties`.

### Changed
- [LPS-72252]: Update the [Liferay Gradle Plugins] dependency to version 3.3.9.

## 1.5.0 - *(Unreleased)*

### Added
- [LPS-73056]: Add the ability to download the Liferay bundle from
[www.liferay.com](https://www.liferay.com) via authentication token. This
behavior can be enabled by setting the `liferay.workspace.bundle.token.download`
property to `true` in `gradle.properties`.

### Changed
- [LPS-73156]: Update the [Liferay Gradle Plugins] dependency to version 3.3.31.
- [LPS-73248]: Use Liferay 7.0.3 GA4 by default.

[Gradle Download Task]: https://github.com/michel-kraemer/gradle-download-task/
[Liferay Gradle Plugins]: https://github.com/liferay/liferay-portal/tree/master/modules/sdk/gradle-plugins
[LPS-66853]: https://issues.liferay.com/browse/LPS-66853
[LPS-66906]: https://issues.liferay.com/browse/LPS-66906
[LPS-67352]: https://issues.liferay.com/browse/LPS-67352
[LPS-67573]: https://issues.liferay.com/browse/LPS-67573
[LPS-67656]: https://issues.liferay.com/browse/LPS-67656
[LPS-68293]: https://issues.liferay.com/browse/LPS-68293
[LPS-68822]: https://issues.liferay.com/browse/LPS-68822
[LPS-68849]: https://issues.liferay.com/browse/LPS-68849
[LPS-69294]: https://issues.liferay.com/browse/LPS-69294
[LPS-69445]: https://issues.liferay.com/browse/LPS-69445
[LPS-69473]: https://issues.liferay.com/browse/LPS-69473
[LPS-69501]: https://issues.liferay.com/browse/LPS-69501
[LPS-70282]: https://issues.liferay.com/browse/LPS-70282
[LPS-70336]: https://issues.liferay.com/browse/LPS-70336
[LPS-70353]: https://issues.liferay.com/browse/LPS-70353
[LPS-70362]: https://issues.liferay.com/browse/LPS-70362
[LPS-70515]: https://issues.liferay.com/browse/LPS-70515
[LPS-70677]: https://issues.liferay.com/browse/LPS-70677
[LPS-71724]: https://issues.liferay.com/browse/LPS-71724
[LPS-72252]: https://issues.liferay.com/browse/LPS-72252
[LPS-73056]: https://issues.liferay.com/browse/LPS-73056
[LPS-73156]: https://issues.liferay.com/browse/LPS-73156
[LPS-73248]: https://issues.liferay.com/browse/LPS-73248
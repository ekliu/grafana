+++
title = "What's New in Grafana v5.2"
description = "Feature & improvement highlights for Grafana v5.2"
keywords = ["grafana", "new", "documentation", "5.2"]
type = "docs"
[menu.docs]
name = "Version 5.2"
identifier = "v5.2"
parent = "whatsnew"
weight = -8
+++

# What's New in Grafana v5.2

Grafana v5.2 brings new features, many enhancements and bug fixes. This article will detail the major new features and enhancements.

* [Elasticsearch alerting]({{< relref "#elasticsearch-alerting" >}}) it's finally here!
* [Cross platform build support]({{< relref "#cross-platform-build-support" >}}) enables native builds of Grafana for many more platforms!
* [Improved Docker image]({{< relref "#improved-docker-image" >}}) with support for docker secrets
* [Security]({{< relref "#security" >}}) make your Grafana instance more secure
* [Prometheus]({{< relref "#prometheus" >}}) with alignment enhancements
* [InfluxDB]({{< relref "#influxdb" >}}) with support for a new function
* [Alerting]({{< relref "#alerting" >}}) with alert notification channel type for Discord
* [Dashboards & Panels]({{< relref "#dashboards-panels" >}}) with save & import enhancements

## Elasticsearch alerting

{{< docs-imagebox img="/img/docs/v52/elasticsearch_alerting.png" max-width="800px" class="docs-image--right" >}}

Grafana v5.2 ships with an updated Elasticsearch datasource with support for alerting. Alerting support for Elasticsearch has been one of
the most requested features by our community and now it's finally here. Please try it out and let us know what you think.

<div class="clearfix"></div>

## Cross platform build support

Grafana v5.2 brings an improved build pipeline with cross platform support. This enables native builds of Grafana for ARMv7 (x32), ARM64 (x64),
MacOS/Darwin (x64) and Windows (x64) in both stable and nightly builds.

We've been longing for native ARM build support for a long time. With the help from our amazing community this is now finally available.

## Improved Docker image

The Grafana docker image now includes support for Docker secrets which enables you to supply Grafana with configuration through files. More
information in the [Installing using Docker documentation](/installation/docker/#reading-secrets-from-files-support-for-docker-secrets).

## Security

{{< docs-imagebox img="/img/docs/v52/login_change_password.png" max-width="800px" class="docs-image--right" >}}

Starting from Grafana v5.2, when you login with the administrator account using the default password you'll be presented with a form to change the password.
By this we hope to encourage users to follow Grafana's best practices and change the default administrator password.

<div class="clearfix"></div>

## Prometheus

The Prometheus datasource now aligns the start/end of the query sent to Prometheus with the step, which ensures PromQL expressions with *rate*
functions get consistent results, and thus avoid graphs jumping around on reload.

## InfluxDB

The InfluxDB datasource now includes support for the *mode* function which allows to return the most frequent value in a list of field values.

## Alerting

By popular demand Grafana now includes support for an alert notification channel type for [Discord](https://discordapp.com/).

## Dashboards & Panels

### Modified time range and variables are no longer saved by default

{{< docs-imagebox img="/img/docs/v52/dashboard_save_modal.png" max-width="800px" class="docs-image--right" >}}

Starting from Grafana v5.2 a modified time range or variable are no longer saved by default. To save a modified
time range or variable you'll need to actively select that when saving a dashboard, see screenshot.
This should hopefully make it easier to have sane defaults of time and variables in dashboards and make it more explicit
when you actually want to overwrite those settings.

<div class="clearfix"></div>

### Import dashboard enhancements

{{< docs-imagebox img="/img/docs/v52/dashboard_import.png" max-width="800px" class="docs-image--right" >}}

Grafana v5.2 adds support for specifying an existing folder or create a new one when importing a dashboard, a long awaited feature since
Grafana v5.0 introduced support for dashboard folders and permissions. The import dashboard page have also got some general improvements
and should now make it more clear if a possible import will overwrite an existing dashboard, or not.

This release also adds some improvements for those users only having editor or admin permissions in certain folders. Now the links to
*Create Dashboard* and *Import Dashboard* is available in side navigation, dashboard search and manage dashboards/folder page for a
user that has editor role in an organization or edit permission in at least one folder.

<div class="clearfix"></div>

## Changelog

Checkout the [CHANGELOG.md](https://github.com/grafana/grafana/blob/master/CHANGELOG.md) file for a complete list
of new features, changes, and bug fixes.

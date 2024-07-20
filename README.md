# WordPress & WooCommerce Sniffs

Collection of PHP_CodeSniffer sniffs for WordPress & WooCommerce that exclude your own files.

## Installation

```php
composer require kallookoo/phpcs-rules
```

## Usage

When the project is related to WooCommerce set the standard with WooCommerce-Excl or set it with WordPress-Excl otherwise.

### Example of a configuration file

```xml
<?xml version="1.0"?>
<ruleset name="WordPress and WooCommerce Sniffs">
	<description>My project ruleset.</description>

	<!-- Rules -->

	<!-- Uncomment the required rule below -->
	<!-- <rule ref="WordPress-Excl"/> -->
	<!-- <rule ref="WooCommerce-Excl"/> -->

	<!-- Configs -->
	<config name="minimum_supported_wp_version" value="6.0"/>
	<config name="testVersion" value="8.0-"/>

	<rule ref="WordPress.WP.I18n">
		<properties>
			<!-- Replace the text-domain with the text domain in this project. -->
			<property name="text_domain" type="array" value="text-domain"/>
		</properties>
	</rule>
</ruleset>
```

virtualdev-module-puppet-zendserver
===================================

Puppet for installation of Zend Server CE. By default support for PHP 5.3 is enabled.

node default {

	include zendserverce

	zendserverce::vhost { 'example-site.com':
		server_name	=> 'example-site.com',
		serveraliases => [
			'www.example-site.com',
			'asset1.example-site.com',
			'asset2.example-site.com',
			'asset3.example-site.com',
			'asset4.example-site.com',
		],
	}

}
# Build

In <code>heroku run bash</code> you can build libraries on the environment.

	mkdir tmp
	cd tmp
	git clone https://github.com/php/php-src.git
	cd php-src
	git checkout php-5.3.10
	cd ext/mysqli
	/app/php/bin/phpize
	./configure --with-php-config=/app/php/bin/php-config
	make

# Download

Heroku will not allow the file to persist. To download the file I used
<code>base64 modules/mysqli.so</code> and then decoded the file back
to binary format locally.

# Info

Idea from https://github.com/yandod/phpinfo-heroku

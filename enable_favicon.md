favicon
=======
enable favicon for a manual install of localwiki

1. copied favicon.ico to /usr/share/localwiki/static<br/>
	$ rsync -avz -e ssh favicon.ico USERNAME@IPaddress:/usr/share/localwiki/static
2. copied favicon.ico to /usr/lib/pymodules/python2.7/sapling/themes/sapling/assets<br/>
	$ rsync -avz -e ssh favicon.ico USERNAME@IPaddress:/usr/lib/pymodules/python2.7/sapling/themes/sapling/assets

3. ssh'd into server and ran:<br/>
	$ localwiki-manage collectstatic
chose yes for overwrite

4. restarted apache<br/>
	$ /etc/init.d/apache2 restart

5. close and refresh browser a few times

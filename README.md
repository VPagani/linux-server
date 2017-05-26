**IP Address:** 104.207.147.234

**URL:** [http://catalog-nd.tk](http://catalog-nd.tk)

##### Software Installed
- Apache 2.4.18
- Python 2.7.12
- PostgreSQL 9.5

##### Summary Config
0. Update and upgrade all packages;
0. Create `student` and `grader` users and add `sudo` access;
0. Set up RSA keys for `student` and `grader` and disable password authentication;
0. Set up firewall rules with UFW allowing only SSH 2200, HTTP 80, NTP 123 incoming and any outgoing;
0. Change default SSH port;
0. Install `mod_wsgi`;
0. Configure `/etc/apache2/sites-available/flask.conf` and enabled with `a2ensite flask`;
0. Import Catalog app project to `/var/www/catalog`;
0. Adapt `catalog/catalog/models/__init_.py` to PostgreSQL;
0. Set up PostgreSQL database `catalog` and user `catalog`;
0. Sign in catalog app and populate database with `catalog/run.sh`;

##### Third-party Resources Used
- [http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/](http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/)
- [https://stackoverflow.com/questions/31298755/how-to-get-apache-to-serve-static-files-on-flask-webapp](https://stackoverflow.com/questions/31298755/how-to-get-apache-to-serve-static-files-on-flask-webapp)

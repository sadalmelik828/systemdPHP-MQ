# LISTENER ON SYSTEMD FOR PHP - IBM MQ SERIES

This program create and register a listener on systemd for integration between PHP and IBM MQ product.
It should be keep in mind that the extension [mqseries](https://pecl.php.net/package/mqseries) for PHP must be install before.

## Files Structure

- **environment** _Contains files with vars environment_
- **test** _Contains files php for testing_
- **units** _Contains files for each service/daemon listener to register on systemd_
- **conf\_check** _Shell Script that check config of service/daemon listener_
- **phpmqctl** _Shell Script that control the action start|stop of service/daemon listener_

## Instructions

1. Configure the paths, vars and your structure according to the system. 
2. Copy unit file to path `/etc/systemd/system` for register the new service/daemon.
3. Execute `sudo systemctl daemon-reload` for reload the services list.
4. Execute `sudo systemctl list-unit-files` for search your new service/daemon registered.
5. Execute `sudo systemctl start apptrs-notificaciones.service` for start the listener. Only if you have seen the service/daemon registered.
6. Execute `sudo systemctl status apptrs-notificaciones.service` for get more details about the status and logging of listener.
7. Execute `sudo systemctl stop apptrs-notificaciones.service` for stop the listener.
8. Execute `sudo systemctl enable apptrs-notificaciones` for register the listener to automatic start with OS. This command is optional according you need.


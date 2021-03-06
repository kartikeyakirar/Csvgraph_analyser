# Csvgraph_analyser
Analyse csv
##Feature
Csv graph analyser analyse data from enricher output csv formatted data of installed and clicked data with location(circle)
can be accesed through 
##### `http://172.16.0.77:3838/csvgraph/` {for Amlpl user only}


## Installing

At this time, Shiny Server can be run on Linux servers with explicit support for Ubuntu 12.04 or greater (64 bit) and CentOS/RHEL 5 (64 bit) or greater. If you are using one of these distributions, please download the pre-packaged installers from RStudio:

> [Download Shiny Server Installers](https://www.rstudio.com/products/shiny/shiny-server/). 

These installers will provide a majority of the prerequisite software and will provision all the necessary directories for you.

If you are not using one of the explicitly supported distributions, you can still use Shiny Server by building it from source, see the [instructions for building from source](https://github.com/rstudio/shiny-server/wiki/Building-Shiny-Server-from-Source).

## Configuration

Shiny Server will use the [default configuration](https://github.com/rstudio/shiny-server/blob/master/config/default.config) unless an alternate configuration is provided at `/etc/shiny-server/shiny-server.conf`. Using the default configuration, Shiny Server will look for Shiny apps in `/srv/shiny-server/` and host them on port 3838. If you plan to host your apps in this directory, you can either copy an app you've already developed to that location:

```
sudo cp -R ~/MY-APP /srv/shiny-server/
```

Or you can copy some or all of the examples provided with the Shiny package. (The location of the R library varies from system to system. You can use the command `R -e ".libPaths()" --quiet` to print the directory of the R library.) For instance, on Ubuntu, you could execute `cp -R /usr/local/lib/R/site-library/shiny/examples/* /srv/shiny-server/`.

Now start a web browser and point it to `http://<hostname>:3838/APP_NAME/`

**If the browser is not able to connect to the server, configure your server's firewall to allow inbound TCP connections on port 3838.**

To customize any of the above, or to explore the other ways Shiny Server can host Shiny apps, see the [Shiny Server Configuration Reference](https://rstudio.github.io/shiny-server/latest/#configuration-settings) for details on the various ways Shiny Server can be configured.

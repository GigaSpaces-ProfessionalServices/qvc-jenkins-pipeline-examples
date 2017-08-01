The XAP 12.1 REST API for administration is documented in the following link:

https://docs.gigaspaces.com/xap/12.1/admin/xap-manager-rest.html

The example scripts refer to jars from a small application which is contained in the file <b>rest-application-example.zip</b>. 

The deployable PU artifacts in this application are <b>shoppingcart-space.jar</b> and <b>shoppingcart-rest.war</b>. 

<b>shoppingcart-space.jar</b> contains the space data model and a remoting service component. <b>shoppingcart-rest.war</b> contains a web application which acts as a client of the remoting service.

The pipeline <b>xap_deploy_space_using_pu.groovy</b> creates the GSCs for the space and creates the space.

The pipeline <b>xap_deploy_app_using_pu.groovy</b> deploys the web application in the grid.

Couple of other example pipelines are included. The pipeline <b>xap_grid_up.groovy</b> shows creation of GSCs. The pipeline <b>xap_create_space.groovy</b> illustrates creation of an empty space.

The pipelines can be tested on a single machine by starting the standalone manager using the following command:

<pre>
./gs-agent.sh --manager-local
</pre>

Starting a manager is required to access the RESTful API.

REST calls can be tried out interactively using the web-based GUI available at http://localhost:8090.

Another important link is https://docs.gigaspaces.com/xap/12.1/admin/xap-manager.html.

Please note that it is important to have the proper setting for the _*XAP_MANAGER_SERVERS*_ environment variable in the <b>setenv-overrides.sh</b> file. 

GeoServer starter for OpenShift
===============================

How to run GeoServer on OpenShift:
----------------------------------

- Login to OpenShift
- Start creating new Tomcat 7 application
- Enter Source Code (Optional URL to a Git repository):
  https://github.com/kubaszostak/geoserver-openstack-starter.git
  on _Configure the application_ page.
- SSH to Your new application: 
```sh
rhc ssh -a [app-name]
```
- Copy geoserver_data folder: 
```sh
cp -a $OPENSHIFT_REPO_DIR/data/. $OPENSHIFT_DATA_DIR/
```
- Grant GeoServer access to data folder: 
```sh
chmod -R ugo+rw $OPENSHIFT_DATA_DIR/geoserver_data/
```
- Restart Your application on OpenShift
- Wait for application restarting...
- You can see log processing by typing
```sh
rhc tail <app_name>
```
- Wait a litte bit more...
- Login to Your application under /geoserver/web/ subdir

Live demo:
http://geoserver-ksz.rhcloud.com

---

Przeczytaj też: 
http://kubaszostak.blogspot.com/2014/04/openshift-darmowy-hosting-geoserver-wms.html

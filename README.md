# Couchapp Bootstrap Website
https://github.com/Smileupps/couchapp-bootstrap-website

## Purpose 

This Couchapp shows how to serve a static website, like the [Bootstrap website](http://getbootstrap.com), directly from CouchDB. This is a little bit more advanced than [Couchapp Hello World](https://github.com/Smileupps/couchapp-hello-world), because we created rewriting rules to reflect bootstrap website links to underlying resources (js, css, html files).

Here are the steps followed to package this couchapp:
1. We downloaded the **[Bootstrap Github Repository](https://github.com/twbs/bootstrap) as a zip file** to our local disk 
2. Using [Smileupps SmileOS](https://github.com/Smileupps/smileos) we created a new design document called *_design/bootstrap-website*
3. We uploaded our zip file to our ddoc *_attachments* field with the Upload/Edit JSON button
3. From our Smileupps control panel, we created a new domain bootstrap-smileupps.com pointing directly to our design document (path: /examples/_design/bootstrap-website/_rewrite) 
4. We created some rewriting rules within the ddoc *rewrites* field to properly forward our website requests to resources stored in *_attachments*.

## Install / Run

### Easy, fast install

This app is part of [Smileupps Ready to Run Examples](https://www.smileupps.com/wiki). This means installation is as simple as:

1. Installing [Free Smileupps CouchDB Hosting](https://www.smileupps.com/store/apps/couchdb) from Smileupps App Store
2. Checking your activation e-mail, which contains links to run it, access or edit its source code.

### Manual install

* **Prerequisite: Apache CouchDB**. You can download it from the [CouchDB official homepage](http://couchdb.apache.org)

1. Download this repository to your local disk
2. Upload this back to your own CouchDB instance, using a [CouchDB deployment tool](https://www.smileupps.com/wiki)
3. Choose a domain name to serve your app
4. Configure your DNS settings to point domain name to your CouchDB instance ip address. 
5. Forward incoming HTTP/S connections to CouchDB port or use a proxy to forward only requests to the above domain.
6. configure your CouchDB vhosts configuration to forward your domain to this app design document

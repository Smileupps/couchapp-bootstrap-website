# Couchapp Bootstrap Website: Another example on how to serve a static website from CouchDB
https://github.com/Smileupps/couchapp-bootstrap-website

## Purpose 

This Couchapp shows how to serve a static website, like the [Bootstrap website](http://getbootstrap.com), directly from CouchDB. This is a little bit more advanced than [Couchapp Hello World](https://github.com/Smileupps/couchapp-hello-world), because we created rewriting rules to reflect bootstrap website links to underlying resources (js, css, html files).

Here are the steps followed to package this couchapp:
1. We downloaded the **[Bootstrap Github Repository](https://github.com/twbs/bootstrap) as a zip file** to our local disk 
2. Using [Smileupps Couch OS](https://github.com/Smileupps/couchos) we created a new design document called *_design/bootstrap-website*
3. We uploaded our zip file to our ddoc *_attachments* field with the Upload/Edit JSON button
3. From our Smileupps control panel, we created a new domain bootstrap-smileupps.com pointing directly to our design document (path: /examples/_design/bootstrap-website/_rewrite) 
4. We created some rewriting rules within the ddoc *rewrites* field to properly forward our website requests to resources stored in *_attachments*.

## Install/ Run

This app is one of [Smileupps CouchDB Examples](https://www.smileupps.com/wiki) and is delivered as part of the [Smileupps CouchDB Hosting application](https://www.smileupps.com/store/apps/couchdb). After installation, you should receive an activation e-mail with URLs and credentials to run it.

You can otherwise also download this repository to your local disk, and upload it back to your own CouchDB instance, by using [Smileupps Couch OS](https://github.com/Smileupps/couchos) or a [CouchDB deployment tool](https://www.smileupps.com/wiki).

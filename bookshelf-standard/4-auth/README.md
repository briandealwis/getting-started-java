# Bookshelf App for Java on App Engine Standard Tutorial
## Auth

Contains the code for using Cloud Datastore and Cloud SQL v2.

This is part of a [Bookshelf tutorial](https://cloud.google.com/java/getting-started/tutorial-app).

Most users can get this running by updating the parameters in `pom.xml`. You'll
also need to [create a bucket][create-bucket] in Google Cloud Storage, referred
to below as `MY-BUCKET`.

### Running Locally

    mvn -Plocal clean appengine:devserver -Dbookshelf.bucket=MY-BUCKET

### Deploying to App Engine Standard

* Deploy your App

    mvn clean appengine:update -Dappengine.appId=<your-project-id> \
        -Dappengine.version=bookshelf \
        -Dbookshelf.bucket=MY-BUCKET

Visit it at http://bookshelf.<your-project-id>.appspot.com

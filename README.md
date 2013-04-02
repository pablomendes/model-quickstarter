Quickstarter for DBpedia Spotlight models
===================================================

You can use this tool for creating models of DBpedia Spotlight in your language.

This script requires Apache Hadoop and Apache Pig, for more information see [this guide](https://github.com/dbpedia-spotlight/dbpedia-spotlight/wiki/Internationalization-%28DB-backed-core%29).

If you have OpenNLP models, add them to your language folder and add the following line to run.sh (example for Dutch):

    ./index_db.sh -o nl wdir nl_NL nl/stopwords.list Dutch models/nl

This will create a DBpedia Spotlight model (for the DB-backend) in `models/nl`. If you do not have OpenNLP models, only add a stopwords file to your 
language folder and add the following to run.sh:


    ./index_db.sh wdir fr_FR fr/stopwords.list French models/fr


## Running on EC2

We also added a setup.sh file that we use to automate our setup when we are running this on EC2.

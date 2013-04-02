Quickstarter for DBpedia Spotlight models
===================================================

You can use this tool for creating models of DBpedia Spotlight in your language.

This script requires Apache Hadoop and Apache Pig, for more information see [this guide](https://github.com/dbpedia-spotlight/dbpedia-spotlight/wiki/Internationalization-%28DB-backed-core%29).

If you have OpenNLP models, add them to your language folder and add the following line to run.sh (example for Dutch):

    ./index_db.sh -o nl wdir nl_NL nl/stopwords.list Dutch models/nl

This will create a DBpedia Spotlight model (for the DB-backend) in `models/nl`. If you do not have OpenNLP models, only add a stopwords file to your 
language folder and add the following to run.sh:


    ./index_db.sh wdir fr_FR fr/stopwords.list French models/fr


## Running on Amazon EC2

We have made a couple of test runs on EC2 with a m1.large master instance (for English it might require more, for smaller languages, less)
and + 5-10 m1.large worker nodes. Start your instances as an Elastic Map Reduce Interactive Pig job.
We also added a setup.sh file that we use to automate our setup when we are running this on EC2.
Running setup.sh will install other useful things that do not come out of the box in those instances such as Maven3, and other useful tools like screen and elinks.

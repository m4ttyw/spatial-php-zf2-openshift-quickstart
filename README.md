# Parks in PHP with ZF2

## Set up gear

	rhc app create parks php-5.3 mongodb-2

## Load data

SSH into the gear and

	cd app-root/repo
	mongoimport -vvvv -h $OPENSHIFT_NOSQL_DB_HOST --type json -d $OPENSHIFT_APP_NAME -c parkpoints --file parks.json -u admin -p

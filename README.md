# Data Collector
Getting results in your collection is not hard. To get started, download and run the Data Collector tool in the system your applications live.

## install

> The data collector is a downloadable zip file that needs to be extracted and run on your target server where the applications you wish to migrate are located ie your application server machine. You should choose the correct data collector for your target server’s operating system.


Once downloaded, follow the steps below.

> **TIP:** The Data Collector is likely to consume a significant amount of resources while gathering data therefore, we recommend you run the tool in a pre-production environment.

1. Copy and place the file to your system in a directory where it has read-write-execute access.
   Then decompress the downloaded file:

```sh
gunzip -c transformationadvisor-AIX.tgz | tar xf -
```

2. Go to the Data Collector directory:

```sh
cd transformationadvisor*
```

> **TIP:** View command-line options that are available for the Data Collector run:
> ```sh
> ./bin/transformationadvisor --help
> ```

## Run tool



Choose one of the following accordingly.

1. Scan app 
```sh
./bin/transformationadvisor -w <WEBSPHERE_HOME_DIR> [--scan-node --ignore-missing-binary --ignore-missing-shared-library]
```

2. Scan app and configuration

```sh
./bin/transformationadvisor -w <WEBSPHERE_HOME_DIR> -p <PROFILE_NAME> [<WSADMIN_USER> <WSADMIN_PASSWORD> --scan-node --ignore-missing-binary --ignore-missing-shared-library]
```

3. Scan .ear or .war

```sh
./bin/transformationadvisor -o <WebSphere apps outside location of the .ear and/or .war files>
```

## View the data
The Data Collector will take some time to run. During this process, you can keep track of its progress by checking your command line.

If there is a connection between your system and your new collection, the Data Collector will send your application data for you.



# Resources

- [Using Transformation Advisor ](https://developer.ibm.com/recipes/tutorials/using-the-transformation-advisor-on-ibm-cloud-private/)
- WebSphere Application [Migration](https://developer.ibm.com/wasdev/docs/migration/), download WebSphere Application Migration Toolkit ([WAMT](https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Application_Server_Migration_Toolkit))
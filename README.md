Globalization Pipeline
======================

![Globalization Pipeline Logo](images/icon.png "Globalization Pipeline")


IBM Globalization Pipeline is a DevOps integrated application translation management service that you can use to rapidly translate and release cloud and mobile applications to your global customers. Access IBM Globalization Pipeline capabilities through its dashboard, RESTful API, or integrate it seamlessly into your application's Delivery Pipeline.

This repo contains common files and information for the
[IBM Globalization Pipeline](https://www.ng.bluemix.net/docs/#services/GlobalizationPipeline/index.html) service and related projects.

Quick Start Guide
-----------------
Below are some steps to help you quickly get started. For more detailed information about the service, please visit the official [Globalization Pipeline  documentation](https://console.ng.bluemix.net/docs/services/GlobalizationPipeline/index.html) page.

**Lets get started!**

### 1. Create a new Globalization Pipeline service instance
Head to the Bluemix catalog and find the Globalization Pipeline service, it should be under the DevOps category.

Note: if you see two catalog entries for Globalization Pipeline, ignore the Beta one since it will be removed soon.

![Bluemix Catalog](images/catalog.png "Globalization Pipeline")

Once you click the service icon, you should be taken to the Globalization Pipeline service page where you will find more information about the service. On this page:

1. Provide a name for your service instance
2. Connect to an application (optional)
3. Select a plan
4. Click Create

![Bluemix Catalog Entry](images/catalog-entry.png "Globalization Pipeline catalog entry")

### 2. Globalization Pipeline Dashboard
Click on the new service instance to go to the Globalization Pipeline Dashboard.

![Globalization Pipeline Dashboard](images/dashboard-overview.png "Globalization Pipeline Dashboard")

1. The *Getting Started* tab provides some general information about the service and some useful links.
2. The *Bundles* tab allows you to view your bundles and create new bundles.
3. The *API User* tab allows you to create new users with different levels of access to the service instance.
4. The *Machine Translation Configuration* tab can be used to configure additional Machine Translation engines from other providers.

### 3. New Bundle
Lets go ahead and create a new Bundle. Click the *New Bundle* button and then fill in the new Bundle's information:

![New Bundle](images/new-bundle.png "New Bundle")

The messages we want translated to the target languages are in `messages.json`:

```json
{
    "greet": "Hello there!",
    "weather": "It is snowing",
    "exit": "Goodbye"
}
```

Click Save and then select the new Bundle from the list to view the Bundle details.

![Bundle Details](images/bundle-details.png "Bundle Details")

You can now click on one of the target languages to view the messages translated in that language. For example, Japanese:

![Translated Messages](images/translated-messages.png "Translated Messages")

You can now download the translated messages by clicking the *DOWNLOAD* button. Or you can access the translated messages directly in your app by using one of the SDKs. To get started with the SDKs, head to the [next section below](#download).

### 4. Credentials
To see the credentials for the service instance, click *View Credentials*:

![New Instance](images/new-instance.png "New Instance")

![Credentials](images/creds.png "Credentials")

This information can be provided to the SDKs to access the service instance. Note however, that if the service instance is connected to an application on Blumix, the SDKs will automatically grab this information.

Caution! The default credentials shown above provide complete access to the service instance, including the ability to delete and modify bundles. When you are using the service in a production app, it is recommended that you create a new *Reader* account through the *API Users* tab. The Reader account can only read bundle data.

<!-- the download anchor is required for backwards compatibility  -->
SDKs<a name="download"></a>
---------------------------

There are a number of SDKs available for this service. Select one below for more details on how to use it.

* Python: [SDK](https://github.com/IBM-Bluemix/gp-python-client)
* Java: [SDK](https://github.com/IBM-Bluemix/gp-java-client) | [Tools](https://github.com/IBM-Bluemix/gp-java-tools)
* Angular: [SDK](https://github.com/IBM-Bluemix/gp-angular-client)
* Node.js: [SDK](https://github.com/IBM-Bluemix/gp-js-client) | [Sample](https://github.com/IBM-Bluemix/gp-nodejs-sample)
* Cordova: [SDK](https://github.com/IBM-Bluemix/gp-cordova-plugin)
* Ruby: [SDK](https://github.com/IBM-Bluemix/gp-ruby-client) | [Sample](https://github.com/IBM-Bluemix/gp-ruby-sample)
* Urban Code Deploy: [Plugin](https://github.com/IBM-Bluemix/gp-ucd-plugin)

Contributing
------------
see [CONTRIBUTING.md](CONTRIBUTING.md)

License
-------
Apache 2.0. See [LICENSE.txt](LICENSE.txt)

> Licensed under the Apache License, Version 2.0 (the "License");
> you may not use this file except in compliance with the License.
> You may obtain a copy of the License at
>
> http://www.apache.org/licenses/LICENSE-2.0
>
> Unless required by applicable law or agreed to in writing, software
> distributed under the License is distributed on an "AS IS" BASIS,
> WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
> See the License for the specific language governing permissions and
> limitations under the License.

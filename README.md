# DBS Project Playground
This markdown file documents each of the components within **DBS Project Playground**, detailing the configuration and deployment process, followed by illustrating their use cases and explaining each of their specific technical details.

# Configuration for Localhost
The ecosystem has been developed in multiple components. Namely, **Code Editor Playground**, **Machine Learning Model Builder** and **PayLah! Enhancement**.

**Live Code Editor:**
  Install the node packages in the root directory and client directory:

 1. `npm i`
 2. `cd client`
 3. `npm i`

Start the localhost:

    npm run dev
    
**Machine Learning Model Builder:**
  Run flask server:
  

    python flask_server.py

**DBS PayLah! Enhancement**

 1. APK file can be installed on lastest android version (sdk 28) with compatibility down to sdk version 24.
 2. The folder can be open and ran with Android Studio.

# Playground Code Editor
## Live Code Editor
The live code editor is designed to provide an in-house editing space, allowing developers to select pre-built templates, edit the code and publish on the spot. This feature accelerates the development process of application, allowing DBS to also control the environment which the development takes place in.

![Playground Code Editor](https://raw.githubusercontent.com/loichiilek/icons_for_test/master/code_editor.png)
 - **File directory** connects to the actual file system to allow developer to have a seamless development process despite being in a browser environment.
 - **Code editor** provides an autosave function to the ec2 instance ensuring code will not lost even if the browser is closed. 
- **Terminal** connects to the server, allowing running of scripts into an isolated environment.
- **Live preview** re-renders the code that is written within the code editor whenever it is saved.
## In-Built Database
The in-built database, ensures that DBS has control over the data that is collected by the application. It also provides an easy access to internal DBS data storage that developers can use, removing the need to use 3rd party data storage.

![In-Built Database](https://raw.githubusercontent.com/loichiilek/icons_for_test/master/database.png)
## Machine Learning Model Builder
The model builder provides an interface for developers to use DBS's data to train a model without having access to the data. This service provides an additional incentive for developers to choose DBS Playground to develop their applications.

## DBSUser API
Developers within the Playground environment is able to access the DBS user's information through API provided.
Following are a few examples to showcase some of the calls that can be made:

    const  name  =  await  dbsUser.getName();

    const  pastTransaction  =  await  dbsUser.getPastTransactions();

# Machine Learning Server


# DBS PayLah! Enhancement
## Android Implementation
The Android PayLah! showcases a possible implementation of an application that customers can use to access the plugins that the developers developed. It provides a secure login, and generates a cookie to authenticate a user's access to the developer's plugins through this mobile application.
![enter image description here](https://raw.githubusercontent.com/loichiilek/icons_for_test/master/android_food_me.png)
The user is also able to browse and download different plugins from the marketplace. The download will save the plugin data and information onto the user's PayLah! application and allow them to call the personalized application from here on.


![Plugins List and Store](https://raw.githubusercontent.com/loichiilek/icons_for_test/master/app_list_store.png)

The plugins can be download in the store, depicted on the right and displayed on the left in the application list.

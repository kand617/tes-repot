# Getting started

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

## How to Use

The following section explains how to use the GraphicsCardAPILib library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *GraphicsCardAPILib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

Clicking the ``` Add ``` button will open a dialog where you need to specify GraphicsCardAPILib in ``` Group Id ``` and GraphicsCardAPILib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=Graphics%20Card%20API-Java&workspaceName=GraphicsCardAPILib&projectName=GraphicsCardAPILib&rootNamespace=com.gogl.www)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *GraphicsCardAPILib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### 

API client can be initialized as following.

```java
// Initializing Object Mapper for Serialization and Deserialization purposes
public static ObjectMapper mapper = new ObjectMapper()
{
	private static final long serialVersionUID = -174113593500315394L;
	{
		configure(DeserializationFeature.FAIL_ON_UNKNOWN_PROPERTIES, false);
		setSerializationInclusion(JsonInclude.Include.NON_NULL);
	}
};


GraphicsCardAPILibClient client = new GraphicsCardAPILibClient();
```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [GTXCardsController](#gtx_cards_controller)

## <a name="gtx_cards_controller"></a>![Class: ](https://apidocs.io/img/class.png "com.gogl.www.controllers.GTXCardsController") GTXCardsController

### Get singleton instance

The singleton instance of the ``` GTXCardsController ``` class can be accessed from the API Client.

```java
GTXCardsController gTXCards = client.getGTXCards();
```

### <a name="get_gtx_async"></a>![Method: ](https://apidocs.io/img/method.png "com.gogl.www.controllers.GTXCardsController.getGtxAsync") getGtxAsync

> TODO: Add a method description


```java
void getGtxAsync(
        final String price,
        final APICallBack<GraphicsCard> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| price |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```java
String price = "price";
// Invoking the API call with sample inputs
gTXCards.getGtxAsync(price, new APICallBack<GraphicsCard>() {
    public void onSuccess(HttpContext context, GraphicsCard response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```


[Back to List of Controllers](#list_of_controllers)




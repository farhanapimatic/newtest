# Getting started

## How to Build


* In order to successfully build and run your SDK files, you are required to have the following setup in your system:
    * **Go**  (Visit [https://golang.org/doc/install](https://golang.org/doc/install) for more details on how to install Go)
    * **Java VM** Version 8 or later
    * **Eclipse 4.6 (Neon)** or later ([http://www.eclipse.org/neon/](http://www.eclipse.org/neon/))
    * **GoClipse** setup within above installed Eclipse (Follow the instructions at [this link](https://github.com/GoClipse/goclipse/blob/latest/documentation/Installation.md#instructions) to setup GoClipse)
* Ensure that ```GOPATH``` environment variable is set in the system variables. If not, set it to your workspace directory where you will be adding your Go projects.
* The generated code uses unirest-go http library. Therefore, you will need internet access to resolve this dependency. If Go is properly installed and configured, run the following command to pull the dependency:

```Go
go get github.com/apimatic/unirest-go
```

This will install unirest-go in the ```GOPATH``` you specified in the system variables.

Now follow the steps mentioned below to build your SDK:

1. Open eclipse in the Go language perspective and click on the ```Import``` option in ```File``` menu.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/go?step=import0)

2. Select ```General -> Existing Projects into Workspace``` option from the tree list.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/go?step=import1)

3. In ```Select root directory```, provide path to the unzipped archive for the generated code. Once the path is set and the Project becomes visible under ```Projects``` click ```Finish```

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/go?step=import2&workspaceFolder=CalculatorService-GoLang&projectName=calculatorservice_lib)

4. The Go library will be imported and its files will be visible in the Project Explorer

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/go?step=import3&projectName=calculatorservice_lib)

## How to Use

The following section explains how to use the CalculatorserviceLib library in a new project.

### 1. Add a new Test Project

Create a new project in Eclipse by ```File``` -> ```New``` -> ```Go Project```

![Add a new project in Eclipse](https://apidocs.io/illustration/go?step=createNewProject0)

Name the Project as ```Test``` and click ```Finish```

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/go?step=createNewProject1)

Create a new directory in the ```src``` directory of this project

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/go?step=createNewProject2&projectName=calculatorservice_lib)

Name it ```test.com```

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/go?step=createNewProject3&projectName=calculatorservice_lib)

Now create a new file inside ```src/test.com```

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/go?step=createNewProject4&projectName=calculatorservice_lib)

Name it ```testsdk.go```

![Create a new Maven Project - Step 5](https://apidocs.io/illustration/go?step=createNewProject5&projectName=calculatorservice_lib)

In this Go file, you can start adding code to initialize the client library. Sample code to initialize the client library and using its methods is given in the subsequent sections.

### 2. Configure the Test Project

You need to import your generated library in this project in order to make use of its functions. In order to import the library, you can add its path in the ```GOPATH``` for this project. Follow the below steps:

Right click on the project name and click on ```Properties```

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/go?step=testProject0&projectName=calculatorservice_lib)

Choose ```Go Compiler``` from the side menu. Check ```Use project specific settings``` and uncheck ```Use same value as the GOPATH environment variable.```. By default, the GOPATH value from the environment variables will be visible in ```Eclipse GOPATH```. Do not remove this as this points to the unirest dependency.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/go?step=testProject1)

Append the library path to this GOPATH

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/go?step=testProject2&workspaceFolder=CalculatorService-GoLang)

Once the path is appended, click on ```OK```

### 3. Build the Test Project

Right click on the project name and click on ```Build Project```

![Build Project](https://apidocs.io/illustration/go?step=buildProject&projectName=calculatorservice_lib)

### 4. Run the Test Project

If the build is successful, right click on your Go file and click on ```Run As``` -> ```Go Application```

![Run Project](https://apidocs.io/illustration/go?step=runProject&projectName=calculatorservice_lib)

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [defaultbinding_icalculator_pkg](#defaultbinding_icalculator_pkg)

## <a name="defaultbinding_icalculator_pkg"></a>![Class: ](https://apidocs.io/img/class.png ".defaultbinding_icalculator_pkg") defaultbinding_icalculator_pkg

### Get instance

Factory for the ``` DEFAULTBINDING_ICALCULATOR ``` interface can be accessed from the package defaultbinding_icalculator_pkg.

```go
defaultBindingICalculator := defaultbinding_icalculator_pkg.NewDEFAULTBINDING_ICALCULATOR()
```

### <a name="add"></a>![Method: ](https://apidocs.io/img/method.png ".defaultbinding_icalculator_pkg.Add") Add

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add a method description


```go
func (me *DEFAULTBINDINGICALCULATOR_IMPL) Add(body *models_pkg.ICalculatorAddInputMessage)(*models_pkg.ICalculatorAddOutputMessage,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.ICalculatorAddInputMessage

var result *models_pkg.ICalculatorAddOutputMessage
result,_ = defaultBindingICalculator.Add(body)

```


### <a name="create_subtract"></a>![Method: ](https://apidocs.io/img/method.png ".defaultbinding_icalculator_pkg.CreateSubtract") CreateSubtract

> *Tags:*  ``` Skips Authentication ``` 

> TODO: Add a method description


```go
func (me *DEFAULTBINDINGICALCULATOR_IMPL) CreateSubtract(body *models_pkg.ICalculatorSubtractInputMessage)(*models_pkg.ICalculatorSubtractOutputMessage,error)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| body |  ``` Required ```  | TODO: Add a parameter description |


#### Example Usage

```go
var body *models_pkg.ICalculatorSubtractInputMessage

var result *models_pkg.ICalculatorSubtractOutputMessage
result,_ = defaultBindingICalculator.CreateSubtract(body)

```


[Back to List of Controllers](#list_of_controllers)




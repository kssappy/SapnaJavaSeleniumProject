# SapnaJavaSeleniumProject

Project Overview:
This automation framework is designed for automating web applications using Selenium WebDriver, Java, TestNG, and Maven. It provides a robust structure for writing and executing automated tests across different browsers.

Setup Requirements:
Before automating browsers, ensure the following dependencies are correctly installed:

Java JDK (version 17).
Maven (version 3.1.2)
TestNG (version 7.8.0)
Apache POI (version 4.1.2) for handling Excel files
Extent Reports (version 2.41.2) to generate a customized Reports.

Overview
This BaseClass is designed to initialize and manage browser interactions for automated tests using Selenium WebDriver. It supports different browsers (Chrome, Firefox, Edge) and loads configuration details from a properties file. Additionally, it includes utilities for managing test data from an Excel file.

Key Components:
WebDriver Initialization: The class sets up the browser driver based on the configuration file.
Properties Handling: Configuration values like the browser type and application URL are loaded from an external config.properties file.

ExcelUtility: This utility is used to handle test data stored in Excel, though it is not fully implemented in the provided code.

Class: BaseClass
Variables:
driver: This is a WebDriver object that handles browser automation.
prop: A Properties object used to load and manage values from a configuration file.
excelTestData: An instance of ExcelUtility used to manage test data from an Excel file (currently initialized without a file path).
Constructor: BaseClass()
Initializes the prop object for loading properties.
Initializes the excelTestData object (though currently no file is passed to it).
Method: properties()
This method loads the configuration from the config.properties file located in the src/main/java/configPackage directory. These properties include browser type and application URL.

Purpose: Reads external configuration to make the code flexible for different environments.
Method: setUp()
Loads the properties file using the properties() method.

Retrieves the browser type from the properties file and initializes the respective WebDriver (Chrome, Firefox, Edge).

Maximizes the browser window.

Calls the getUrl() method to navigate to the application URL.

Closes the browser using the getClose() method after operations.


Method: getUrl()
This method retrieves the applicationURL from the properties file and directs the browser to that URL.

Method: getClose()
Closes the browser .if it was initialized.


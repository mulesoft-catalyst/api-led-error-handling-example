# Error Handling with API Led Connectivity approach - Example
This repository contains three applications that define a best practice to apply error handling when dealing with multiple Mule APIs

## Legacy Application
It's an application that will return an error or a not found error for specific customer ids. The idea behind this application is to mock a legacy system that will return different error messages or code without the standard HTTP Status.

## System Customer API
It's a system level API that will provide connectivity to the legacy system described before. Based on the error codes, it will return an HTTP Status. It can be 200, 404 or 500.

## Experience Customer API
It represents the API consumed by the user. It validates the Status of the HTTP Response manually and throws custom exceptions to return status 404 or 500.

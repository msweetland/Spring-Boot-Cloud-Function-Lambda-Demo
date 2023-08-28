# Spring Cloud Function API Demo Guide

Welcome to the demo guide for the Spring Cloud Function API developed with Spring Boot 3.1.3, Java 17, and Gradle. This document provides a step-by-step approach to run and showcase the function both in the AWS Lambda SAM environment and locally.

## Prerequisites
- Java 17 installed
- Gradle installed
- Install [AWS SAM CLI](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-install.html) (only if showcasing in a simulated AWS environment)
- Install [curl](https://curl.haxx.se/download.html) for testing the API endpoints

## Running Locally with AWS SAM
1. **Start the SAM Local API**: To showcase the API locally in a simulated AWS Lambda environment, use the AWS SAM CLI: `sam local start-api`. The API endpoint should be available at `http://127.0.0.1:3000/`.
2. **Showcase with curl**: Once your API is running, use the curl command to interact with your function. `curl -X POST http://127.0.0.1:3000/uppercase -d "hello world"`. The output should display the text transformed to uppercase.

## Running Locally without AWS SAM
1. **Start the Spring Application**: As the project uses Gradle, start the application with: `./gradlew bootRun`. The demo endpoint should now be available at `http://127.0.0.1:8080/`.
2. **Showcase with curl**: Use the curl command to interact: `curl -X POST http://127.0.0.1:8080/uppercase -d "please work"`. The output should again show the text transformed to uppercase.

## Final Notes
- Ensure that the port numbers (`3000` or `8080`) are correct as per your configurations.
- For a more user-friendly interaction experience during your demo, consider using tools like [Postman](https://www.postman.com/).

Enjoy!
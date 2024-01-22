# Travel Agency Management System

This project is a Travel Agency Management System implemented as a REST API using the Quarkus framework. It supports travel agencies in creating and managing travel programs, allows travelers to register for trips, provides a search functionality for finding trips, and offers statistical insights to travel agencies.
<!---## Features

- **Users Registration**: Travel agencies and Travelers can register to the service.

- **Travel Program Management**: Travel agencies can create travel programs, specifying details such as registration deadlines, departure/return dates, costs, deposits, and destinations to be visited during the trip. Each destination includes transport, accommodation, and attractions.

- **Boooking Prerequisites**: Interested travelers must register by the registration deadline and pay a deposit, with the total amount due by the date of departure.

- **Booking Requirements**: Each travel program has a minimum and maximum number of participants. If the minimum is not reached by the registration deadline, the trip is canceled, and deposits are refunded.

- **Traveler Registration**: Travelers can register to the service to access its features.

- **Trip Search**: Search for trips based on criteria such as destination, minimum days of stay, total trip duration, cost, and more.

- **Statistical Insights**: The service provides statistics to travel agencies,including average trip occupancy by destination for their programs and overall on the platform, and a list of destinations by popularity for specific periods.
!--->
## Requirements

- **Users Registration**: Travel agencies and Travelers must be able to register to the service.

- **Management of Travel Programs**: The service must allow travel agencies to create, edit, and delete travel programs. This includes the ability to set parameters like registration deadlines and costs.

- **Participation Management**: Travelers should be able to register for trips and check the status of their applications. The system must handle the registration process, including collecting advance payments.

- **Trip Search**: A search feature for finding trips based on various criteria. Travelers use this feature to discover suitable travel programs.

- **Statistics and Reports**: The service must generate statistics and reports for travel agencies. These reports could include data on occupancy, destination popularity, and other relevant metrics.


## Assumptions

- **Travel Agencies**: There is a demand from real travel agencies to use the service to manage their travel programs. The service will cater to multiple travel agencies.

- **Travel Agency Registration**: Travel agencies need to register with the service before they can use it.

- **Configuration of Travel Programs**: Travel agencies can create travel programs, specifying details such as registration deadlines, departure/return dates, costs, deposits, and destinations to be visited during the trip. Each destination includes transport, accommodation, and attractions.

- **Traveler Participation**: Travelers are expected to register for trips by the registration deadline. Advance payments are required from travelers.

- **Minimum and Maximum Number of Participations**: Each travel program has defined minimum and maximum participation limits. The system enforces these limits.

- **Trip Cancellation**: If the minimum number of registrations is not met, trips are canceled, travelers get notified via email and the deposits are returned to the travelers.

- **Travel Search**: Travelers use the service to search for trips based on various criteria, such as destination, date, and cost. This feature helps travelers find suitable travel programs.

- **Statistics**: The service provides statistical insights to travel agencies, including average trip occupancy per destination, a popularity list of destinations, and overall statistics for better decision-making.

## Domain Model Diagram
<br>

![TravelManagementModel.jpg](https://media.discordapp.net/attachments/1161636960616599663/1175055351989669989/TravelManagementModel.jpg?ex=6569d693&is=65576193&hm=a1396aec504ee42a99ab6e471e91069a49c89498904e9dd6ac4b56cd410bcbc6&=&width=1029&height=671)

<br>

## Build
The build of the software is done using the Maven 3 tool. The installation of Maven is relatively simple. After downloading Maven (e.g. version 3.5.0) and extracting the files to an appropriate directory e.g. **C:\Program Files\apache-maven-3.5.0** you should:

- Set the JAVA_HOME environment variable to point to the JDK installation directory
- Add the **C:\Program Files\apache-maven-3.5.0\bin** directory to the PATH environment variable.
- Set the M2_HOME environment variable. In our example it is the directory **C:\Program Files\apache-maven-3.5.0**.

In order to run the software build tasks from the command line, we use Maven via the **mvn** command after moving to the directory where the pom.xml file is located. A typical Maven run is:

**mvn [options] [target [target2 [target3] … ]]**

The generated files are created by Maven in the **/target** directory.

Typical tasks with Maven are:

- **mvn clean** cleaning the project. All files in the **/target** directory are deleted.
- **mvn compile** compile the source code. **.class** files are generated in the /**target/classes** directory.
- **mvn test-compile** compile the test code. The .class files are generated in the **/target/test-classes** directory.
- **mvn test** execution of tests with the JUnit framework.
- **mvn site** production on the project site which includes the project documentation.
- **mvn umlet:convert -Dumlet.targetDir=src/site/markdown/uml** produces png image files for all diagrams located at src/site/markdown/uml. It is recommended to call the command before submitting a new diagram version to the git repository (**git commit**). As a result the generated diagram image files accompany the source files so that it is easy to navigate the project documentation via github.

## Prerequisites

- [Quarkus](https://quarkus.io/)
- Java Development Kit (JDK)    
- Database (e.g., PostgreSQL, MySQL)
- Build Tool (e.g., Apache Maven)
- Dependencies (Quarkus extensions, databases, etc.)

## Installation and Usage

1. Clone the repository.

2. Configure your database settings in `src/main/resources/application.properties`.

3. Build the project using your preferred build tool:


## API Endpoints:
- **/api/travel-agencies**: Τερματικά σημεία για τη διαχείριση ταξιδιωτικών γραφείων.
- **/api/travel-programs**: Τερματικά σημεία για τη διαχείριση ταξιδιωτικών προγραμμάτων.
- **/api/travelers**: Τερματικά σημεία για τη διαχείριση ταξιδιωτών.
- **/api/trip-registrations**: Τερματικά σημεία για τη διαχείριση εγγραφών ταξιδιών.
- **/api/trip-search**: Τερματικά σημεία για αναζήτηση ταξιδιών.
- **/api/trip-statistics**: Τερματικά σημεία για πρόσβαση σε στατιστικά δεδομένα.

## Documentation

For the software documentation, Markdown markup was used to write the texts and the UMLet tool was used to construct the UML diagrams.



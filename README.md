# TutorBookings

## Description

This collaborative project is a web application that connects tutors and students. It is inspired by Riley's experience as a peer tutor and Microsoft Bookings' lack of recurring appointment scheduling, a feature strongly desired by students. The goal is to implement this feature to improve the user experience for scheduling tutoring. 

## Technologies

- HTML/CSS
- SQLite 
- C#/ASP.Net/Dapper

## Collaborators
**Riley @reddwryly**
- HTML/CSS
- Database schema design + implementation
- Scheduling webform
- Reccuring appointment logic

**Braeden @ThatRedBacon**
- HTML/CSS
- Admin Page webform
- Database implementation with admin page

## Running the Project 

make sure the following are installed before continuing: 
* Visual Studio + The ASP.NET and web development workload
* .NET Framework 4.7.2 Target framework 

### 1.) Clone the Repository 

* locally download the zip file
* Find **TutorBookings.slnx** in the root folder and right click to open with Visual Studio
* Allow Visual Studio to restore the required NuGet packages. These include Dapper, SQLite, and other dependencies listed in packages.config.

### 2.) Build the project from the UI or Terminal (Powershell)

UI: 
* In the top navigation bar find the **Build** 
* Click **Build Solution**

**OR** Terminal: 
* Open terminal from project directory
* copy/paste in the terminal: ```msbuild TutorBookings.slnx /p:Configuration=Debug```

### 3.) Start the Web Application from the UI or Terminal

UI: 
* Under the top navigation bar find and click the **Start Button** (green filled triangle)
* A webpage will open with an error (the default path is not configured)
* Append the populated URL with add /AboutTutoring 
	- When complete it should look something like: ```http://localhost:61133/AboutTutoring```

**OR** Terminal: 
* Open terminal from project directory
* copy/paste in the terminal run: ```& "${env:ProgramFiles(x86)}\IIS Express\iisexpress.exe" /path:"$PWD" /port:8080```
* In a new terminal window copy/paste to open: ```Start-Process "http://localhost:8080/AboutTutoring"```
	- **OR** copy/paste in your browser to open: ```http://localhost:8080/AboutTutoring```

Note: The terminal method uses port 8080 while Visual Studio in the UI method may use a different port

## Project Status: Completed

Left incomplete: 
- Scheduler reassigning a tutor when the chosen tutor is available for a recurring appointment

> Completed:
> * Baseline HTML/CSS
> * Database design/implementation
> * Database Connection
> * Apointment Scheduling Form
> * Recurring appointment logic
> * Manually-creat appointments by admin
> * Unique Appointment ID and Student Names

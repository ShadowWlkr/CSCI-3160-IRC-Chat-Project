# Lightweight Internet Relay Chat (IRC) Application Project

## Goal
The purpose of this project is to capstone the work performed in the operating system API and communication labs with a group project that incorporates skills learned in these labs. Teams of 4 or 5 students will produce, at a minimum, a lightweight internet relay chat (IRC) application, written in C, which employs a client-server architecture. In addition, the server will employ some programmatic scheme for managing multiple clients. Each team of students will present their work to the class during the last week of classes in a 10-15 minute presentation.

## Requirements
The IRC application shall consist of a client application and a server application. Clients shall connect to the server—there may be many clients connected to one server. At a minimum, the IRC server shall:
- Start by accepting a port number for the listening service via command line argument.
- Accept incoming client connections via POSIX (Berkeley) sockets for an indeterminate amount of time.
- Map a single task on the server to a single connected client in order to manage a client session.
- Receive messages from the client.
- Multicast received messages to other server tasks.
- Transmit messages from other clients to the connected client.

The server should complete all of these functionalities with high quality-of-service (i.e., low-latency message handling, high server availability, high server uptime, and clean implementation—no resource leaks). At a minimum, the IRC client shall:
- Start by accepting an IP address and a port number for the server’s listening service.
- Accept input messages from the user.
- Transmit messages to the server’s assigned session task.
- Receive and display messages from the server’s assigned session task.

A client may disconnect from the IRC service at any time by having the user input “quit” as a message. The client shall close the connection and exit; the server task, on detection of the closed connection, shall exit.

## Presentation
At a minimum, student teams shall prepare a 10-15 minute presentation that:
- Introduces the student team.
- Briefly describes what work on the IRC application the team completed.
- Demonstrate the IRC application.
- Perform a retrospective on the project’s development process.
- Reflect on Computer Systems, as a course.

## Exceeding Expectations
Think through ways to expand these basic requirements—for example, you could add multiple task handlers in the client: one task for receiving and displaying messages from the server and one task for accepting user input messages and transmitting those messages to the server. You could build your IRC client application with a graphical user interface—deploy your C client code as a library, then integrate that library in a managed language application/web application. You could create a better textual user interface (TUI)—add timestamps, display usernames, display emojis, and create multiple client panes. You could implement registration and authentication workflows on your server for when a client connects. You could further extend the account concept by having the server keep a history of prior conversations.

## Deliverables
Submit your IRC application source codes and presentation materials to the Dropbox by the last day of classes. In addition, present your IRC application as specified during the last week of classes.

## Grading
Project submissions that provide a functional client-server chat application that meets the requirements, but does not exceed requirements, along with a sufficient presentation, meets my expectations for the project. Project submissions that exceed the specified application requirements and/or excellent presentations will exceed my expectations, depending on the quality of the extensions (for the application) and/or excellence of the presentation.

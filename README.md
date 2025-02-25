# window-proxy-sever

=======

# Proxy Server GUI

## Overview

This project provides a Windows-based graphical user interface (GUI) for a proxy server. The application allows users to start and stop the proxy server, monitor incoming HTTP requests, and manage a blacklist of blocked domains.

## Features

- Start and stop the proxy server with buttons.
- Display HTTP request details, including method, host, and port.
- Maintain a blacklist of blocked domains.
- Allow users to add and remove entries from the blacklist.
- Provide real-time status updates on the proxy server.

## Dependencies

Ensure you have the following libraries installed:

- Windows API (`windows.h`)
- Winsock (`winsock2.h`, `ws2tcpip.h`)
- Standard C++ libraries (`string`, `vector`, `thread`, etc.)

## File Structure

- `gui.cpp`: Main GUI implementation.
- `prepare.h`: Helper functions for processing requests and handling the blacklist.
- `prepare.cpp`: Implements request parsing and blacklist checking.

## How to Compile and Run

1. Use a Windows environment with a compiler that supports WinAPI (e.g., MinGW, MSVC).
2. Compile the project using the following command:
   ```sh
   g++ src/gui.cpp src/prepare.cpp -o proxy_server -Iinclude -lws2_32 -mwindows
   ```
3. Run the executable:
   ```sh
   ./proxy_server
   ```

## Usage

1. Enter the desired port number.
2. Click **Start** to begin the proxy server.
3. HTTP requests will be displayed in the corresponding list boxes.
4. Use the **Blacklist** section to block specific domains.
5. Click **Stop** to shut down the proxy server.

## Notes

- Ensure port numbers are valid before starting the server.
- The proxy handles only HTTP connections.
- Blacklisted domains are blocked from being processed.

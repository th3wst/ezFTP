# ezFTP-client

A lightweight, GUI-based FTP file-sharing client and server application. This program allows you to securely transfer files over your local network using an easy-to-use interface.

## Features

- **Set Up Credentials**: Configure your FTP server with a username and password for secure access. Credentials are securely hashed and stored using bcrypt.
- **Start Server**: Launch a local FTP server with custom port options and secure file handling.
- **Stop Server**: Easily stop the FTP server when it's no longer needed.
- **File Upload**: Upload multiple files to the server using a graphical file selection dialog.
- **Secure File Handling**: Files are securely stored in the dedicated `uploaded_files` directory.
- **User Feedback**: Real-time status and progress updates for server actions and file uploads.
- **Port Configuration**: Customize the port number for the FTP server to fit your network requirements.

## How to Use

### Download and Run

1. Place the executable in a folder of your choice.
2. Double-click the executable to launch the application.

### Set Up Credentials

1. Click the **Set Up Credentials** button.
2. Enter a username and password for your FTP server.
3. Credentials are securely hashed and stored in a configuration file.

### Start the FTP Server

1. Click the **Start Server** button.
2. Enter the saved password to authenticate and start the server.
3. Optionally configure the port number (default is 21).
4. Once started, the server displays the IP address, port, and username for connections.

### Stop the FTP Server

1. Click the **Stop Server** button to safely terminate the server.

### Upload Files

1. Click the **Upload Files** button to select files from your computer.
2. Authenticate using your credentials and watch the real-time progress bar as files are uploaded.
3. Files are stored in the `uploaded_files` directory on the server.

## Notes

- The FTP server runs locally and is accessible only within your local network.
- Ensure your firewall settings allow traffic on the selected port to enable successful connections.
- Credentials are hashed with bcrypt for enhanced security.
- If you encounter issues, ensure the `ftp_credentials.cfg` file exists in the application's data directory.

## System Requirements

- **Python 3.7 or higher** (if running from source)
- **Required Libraries**:
  - `pyftpdlib`
  - `bcrypt`
  - `appdirs`

To install the required dependencies, run:

```bash
pip install pyftpdlib bcrypt appdirs
```

## Running from source
```bash
git clone https://github.com/th3wst/ezFTP-client.git
cd ezFTP-client
python ezFTP.py
```



# Logic World - Pelican Egg

A Pelican / Pelican egg for hosting dedicated Logic World servers. This egg allows you to easily deploy and manage Logic World game servers through the Pelican Panel interface.

## About Logic World

Logic World is a first-person sandbox simulation game that's all about digital logic. Play alone or with friends, invent new machines, build up layers of complexity, and experience the joy of circuits!

## Installation

1. **Import the Egg**
    - Download the egg configuration file
    - Import it into your Pelican Panel

2. **Create a New Server**
    - Select the Logic World egg
    - Choose your primary port allocation during installation
    - **Important**: If you change the port after installation, you must manually update it in the `config.jecs` file

3. **Configure Steam Authentication**
    1. Set the required variables:
        - Steam username
        - Steam password
    2. **Steam Mobile Authenticator**: Keep your Steam mobile authenticator app open during installation and server startup. You need to accept the login **at least twice** as we don't store Steam VDF config for security reasons.
    3. **Security Prompt**: When Steam shows security notifications, choose "Steam client", then "Other" for accepting.

4. **Happy Playing!**

### 3. Configure Steam Credentials

Set the following environment variables in your server configuration:

- `STEAM_USER`: Your Steam username
- `STEAM_PASS`: Your Steam password
- `SRCDS_APPID`: `1252670` (Logic World dedicated server App ID)

> **Note**: If you have Steam Guard enabled, you may need to use an app password or disable 2FA temporarily during installation and playing time. I recommend to buy a seperate game version for a dedicated server user (a new steam account)

## Configuration

### Server Configuration

The Logic World server can be configured through the `config.jecs` file which is automatically created during installation. The egg automatically configures the server port to match the port assigned by Pelican.

### Port Configuration

The server will automatically use the port assigned by Pelican Panel. The installation script modifies the `config.jecs` file to set the `DefaultPort` value accordingly.

## Troubleshooting

### Common Issues

1. **Steam Authentication Fails**
   - Ensure Steam credentials are correct
   - Disable Steam Guard temporarily if needed
   - Try using anonymous login (leave username/password empty)

2. **Server Won't Start**
   - Check server logs for error messages
   - Ensure sufficient disk space and memory

3. **Connection Issues**
   - Confirm the server port is properly configured
   - Check firewall settings
   - Verify the server is listening on the correct port

### Log Locations

Server logs are available through the Pelican Panel console interface.

## Links

- [Logic World on Steam](https://store.steampowered.com/app/1264090/)

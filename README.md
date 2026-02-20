# Keyboard Maestro Web Trigger

A simple webpage to remotely trigger a Keyboard Maestro macro via its built-in web server.

## Setup

1. Open **Keyboard Maestro** on your Mac.
2. Go to **Preferences → Web Server** and enable the web server.
3. Open `index.html` in a browser (or serve it locally).
4. Click **Run Macro** to trigger the "Test to display alert" macro.

### Accessing from another device

If you want to trigger the macro from a phone or another computer on the same network:

1. Find your Mac's local IP (System Settings → Wi-Fi → Details → IP Address).
2. Enter that IP in the **Host** field on the webpage.
3. Make sure port `4490` is accessible on your network.

## How it works

The page sends an HTTP request to the Keyboard Maestro web server:

```
http://<host>:4490/action.html?macro=Test+to+display+alert
```

This triggers any macro with a matching name.

# Blum auto play game

A script that will play mini game in Blum for you, using your tickets and collecting blum points

## Installation

1. **Install the `blum-auto-play` package:**

```bash
npm install blum-auto-play
```

3. **Create a `index.js` file and paste the code:**

```javascript
import { play } from "blum-auto-play";
const authToken = "Bearer <your_token>";
play(authToken);
```

4. **Add your Bearer token:**

   - Copy your Blum `Bearer token` and paste it in the `index.js` file.
  
## Receiving a Bearer token

1. **Install the [`Resource Override`](https://chromewebstore.google.com/detail/resource-override/pkoacgokdfckfpndoffpifphamojphii?utm_source=ext_app_menu) extension for Chrome**

2. **Set up Resource Override:**
   - Click the `Add Rule` button and select `Change Headers`.
   - In the `For` field, enter `*` (for convenience).
   - Click `Edit Headers` and select from the presets: `Enable CORS`, `Allow Frames` and `Allow Outside Content`.
   - Close the settings window.
3. **Get your Bearer token:**

   - Go to the web version of Telegram and open DevTools (usually F12 or Ctrl+Shift+I).
   - Launch Blum and go to the `Network` tab in DevTools.
   - Find your Bearer token in the request headers.

4. **Copy your Bearer token and paste it into the index.js file.**

![how to get Bearer token](./src/assets/token.jpg)

## Run the script:

```bash
   node index.js
```

## Functionality

- Starts a new game
- Collects a random number of points between 170 and 195
- Waits a random amount of time between 30 and 35 seconds
- Claims the points
- If an error occurs, waits 5 seconds and retries
- If the token is invalid, logs an error and exits
- If the number of tickets is 0, logs an error and exits

## Note:

Once you have received the Bearer token, be sure to disable the Resource Override extension to avoid problems with other sites.

![extension](./src/assets/resource.jpg)

# Happy mining!

---
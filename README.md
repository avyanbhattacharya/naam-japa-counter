# Touchless Japa Counter

A free, private, lightweight, no-ads web counter for naam japa. Choose the touchless timer or the large-button tap counter. Both modes track total naam and completed 108-count rounds locally in your browser.

## Why it works after an iPhone locks

iOS pauses browser JavaScript timers when the screen locks. This project does not treat `setInterval()` as the clock. It saves the start time and calculates the count from actual elapsed time:

```text
count = floor(elapsed milliseconds / 2000)
```

The display may freeze while the phone is locked, but it catches up to the correct count as soon as the page becomes active again.

## Features

- Start, pause, and reset controls
- Adjustable speed from 1 to 5 seconds per naam
- Completed rounds and current progress based on 108 naam per round
- Large-button Tap Japa Counter that adds one naam per tap
- Separate saved counts for Touchless and Tap modes
- Local browser storage with no account, ads, or external dependencies
- Accurate catch-up after the screen locks
- Saves the current session in the browser, even if the page reloads
- Mobile-friendly design with no dependencies or build process

## Run locally

Download the project and open `index.html` in a browser. Most features work directly from the file.

## Publish with GitHub Pages

1. Open the repository's **Settings**.
2. Select **Pages** under **Code and automation**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and `/ (root)`, then click **Save**.

GitHub will show the public URL after deployment completes.

## iPhone home-screen shortcut

Open the published URL in Safari, tap **Share**, then choose **Add to Home Screen**.

## Limitation

A web page cannot reliably chime, vibrate, or speak while iOS has suspended it in the background. A native iPhone app would be needed for reliable locked-screen alerts.

## License

MIT

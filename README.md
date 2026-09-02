# Naam Japa Counter

A simple, hands-free web counter for naam japa. After you press **Start**, the count increases by one every two seconds.

## Why it works after an iPhone locks

iOS pauses browser JavaScript timers when the screen locks. This project does not treat `setInterval()` as the clock. It saves the start time and calculates the count from actual elapsed time:

```text
count = floor(elapsed milliseconds / 2000)
```

The display may freeze while the phone is locked, but it catches up to the correct count as soon as the page becomes active again.

## Features

- Start, pause, and reset controls
- One naam every two seconds (30 per minute / 1,800 per hour)
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

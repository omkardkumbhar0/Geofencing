Geofencing with HTML, CSS & JavaScript (No Backend Needed)

This project is a simple browser-based geofencing system built only with HTML, CSS, and JavaScript.
It uses the Leaflet.js library (an open-source mapping library) and the Geolocation API to:

Show your current location on a map.

Allow you to add fences by clicking on the map (with approval popup).

Show a list of added fences on the right side.

Allow you to remove fences.

Notify you when you enter a fence (smart detection, not spammy).

🚀 Features

Show Current Location

Uses the browser’s built-in Geolocation API to get your current latitude & longitude.

Displays a blue marker on the map for your position.

Add Fences by Clicking

When you click anywhere on the map, a popup asks:
✅ "Do you want to add a fence here?"

If approved, a red circle fence is drawn at that location.

Remove Fences

Every fence is listed in the right-hand sidebar.

Each entry has a ❌ remove button.

When clicked, the fence disappears from both the map and the list.

Smart Notifications

When your current location enters any fence’s area, a notification appears at the bottom.

Notifications are rate-limited so you don’t get spammed.

🛠️ Tech Used

HTML5 → Structure

CSS3 → Styling (map & sidebar layout)

JavaScript (Vanilla) → Logic

Leaflet.js → Map rendering

Geolocation API → Get current device location

📂 File Structure
📁 geofence-app
│── index.html   # Single HTML file (includes CSS + JS)

📜 How It Works (Step by Step)

The app loads a Leaflet map centered on your current location.

You can click anywhere on the map → a confirmation popup appears.

If approved, a red circular fence (100m radius) is drawn.

The fence is also added to the sidebar list with a remove option.

The app tracks your live location →

If inside a fence, it shows a notification.

Notifications are limited to once per minute per fence to prevent spam.

▶️ Usage

Open index.html in your browser.

Allow location permissions when prompted.

Your location will show up on the map.

Click anywhere → approve popup → fence added.

Walk/drive into the fenced area → notification triggers.

⚠️ Notes

Works only if location permissions are allowed.

Notifications are basic JS alerts + HTML banners (no push notifications).

Radius is fixed at 100 meters (can be changed in code).

💻 Example Code Snippet (Inside index.html)
L.circle([lat, lng], { radius: 100, color: "red" }).addTo(map);


This creates a 100m geofence around the selected point.

✅ Next Improvements (Optional)

Save fences to LocalStorage so they persist after refresh.

Customize fence radius when adding.

Add browser notifications (Notification API).

Multi-user sync with a backend (e.g., Firebase).

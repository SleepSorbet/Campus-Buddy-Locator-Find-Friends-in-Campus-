# Campus Buddy Finder

## Project Overview
Campus Buddy Finder is a simple and impactful web application designed to help students locate and connect with friends within their campus using real-time location sharing on an interactive map.

---

## Core Features
1. **User Authentication**  
   - Secure sign-up and login using JWT (JSON Web Tokens) to protect user data.

2. **Friend Location Sharing**  
   - Users can share their real-time location with selected friends.
   - Display friend markers on a campus map for easy navigation.

3. **Location Request**  
   - "Where are you?" requests to prompt friends to share their current location.

4. **Privacy Controls**  
   - "Share" or "Hide" location toggle for enhanced privacy.

---

## Tech Stack
- **Frontend:** React (with Vite) and Leaflet.js or Google Maps API for map integration.
- **Backend:** Node.js and Express for server-side logic.
- **Database:** MongoDB for storing user profiles and friend connections.
- **Real-Time Updates:** Socket.IO for real-time communication.
- **Deployment:** Vercel (frontend), Render/Railway (backend)

---

## User Flow
1. **Sign Up / Log In:** Users create accounts or log in securely.
2. **Friend List:** Users can add and view their friends.
3. **Location Sharing:** Toggle location sharing to display real-time locations on the campus map.
4. **Find Friends:** View shared friend locations as markers on the campus map.
5. **Stop Sharing:** Users can stop location sharing at any time.

---

## Potential Extensions
1. **SOS Emergency Feature:** Allow users to send emergency alerts with their current location to selected contacts.
2. **Campus Event Locations:** Highlight key events and gathering points on the map.
3. **Group Meeting Points:** Create custom markers for group study or meetup locations.

---

## Implementation Plan
### **Phase 1: Setup and Authentication**
- Set up project structure with Vite for the frontend and Node.js for the backend.
- Implement JWT-based authentication.

### **Phase 2: Map Integration**
- Integrate Leaflet.js or Google Maps API for map rendering.
- Allow users to drop pins representing their real-time locations.

### **Phase 3: Real-Time Location Sharing**
- Set up Socket.IO for real-time friend location updates.
- Display friend markers on the map.

### **Phase 4: Privacy and Location Requests**
- Add "Share" and "Hide" location toggles.
- Implement location request functionality.

### **Phase 5: Deployment and Testing**
- Deploy the application and conduct extensive testing.

---

## Conclusion
Campus Buddy Finder is a lightweight yet impactful solution for fostering better connectivity among students. With its simple feature set and real-time location-sharing functionality, it provides a valuable tool for easy friend-finding within campus environments.


Contribution By Prasad Shaswat & Naina Chauhan

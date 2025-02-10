Below is the **Software Requirements Specification (SRS)** for the **Campus Buddy Finder** project, along with a suggested **folder and file structure** for organizing the codebase.

---

## **Software Requirements Specification (SRS)**

### **1. Introduction**
#### **1.1 Purpose**
The purpose of the **Campus Buddy Finder** is to provide students with a real-time location-sharing platform to easily locate and connect with friends on campus. The application will include features such as user authentication, real-time location sharing, privacy controls, and interactive map google integration.

#### **1.2 Scope**
The application will be a web-based platform accessible on both desktop and mobile devices. It will use modern technologies like React, Node.js, MongoDB, and Socket.IO to deliver a seamless user experience.

#### **1.3 Definitions**
- **JWT**: JSON Web Token for secure authentication.
- **Socket.IO**: A library for real-time, bidirectional communication.
- **Leaflet.js**: A JavaScript library for interactive maps.
- **Geospatial Indexing**: A technique to optimize location-based queries in MongoDB.

---

### **2. Overall Description**
#### **2.1 User Needs**
- Students need a way to locate friends on campus in real-time.
- Users require privacy controls to manage location sharing.
- The app should be intuitive, fast, and visually appealing.

#### **2.2 System Features**
1. **User Authentication**:
   - Secure sign-up and login using JWT.
2. **Real-Time Location Sharing**:
   - Share live location with friends.
   - Display friend locations on an interactive map.
3. **Privacy Controls**:
   - Toggle location sharing on or off.
4. **Location Requests**:
   - Send "Where are you?" requests to friends.
5. **Map Features**:
   - Search for friends.
   - Show estimated distance/time to reach a friend.
   - Zoom controls and "Focus on Friends" button.
6. **Smart Notifications**:
   - Notify users when friends are nearby.
7. **Event Integration**:
   - Display campus events on the map.
8. **SOS Feature**:
   - Send emergency alerts with location.

#### **2.3 Assumptions and Dependencies**
- Users have access to a modern web browser.
- The app will use third-party APIs (e.g., Google Maps or Leaflet.js) for map rendering.
- Real-time communication will depend on Socket.IO.

---

### **3. Functional Requirements**
#### **3.1 User Authentication**
- Users can sign up and log in securely using JWT.
- Passwords are hashed and stored securely in the database.

#### **3.2 Location Sharing**
- Users can share their real-time location with friends.
- Friends' locations are displayed as markers on the map.

#### **3.3 Privacy Controls**
- Users can toggle location sharing on or off.
- Location data is obfuscated for privacy.

#### **3.4 Location Requests**
- Users can send "Where are you?" requests to friends.
- Friends can accept or decline the request.

#### **3.5 Map Features**
- Users can search for friends on the map.
- The map shows estimated distance and time to reach a friend.
- Users can zoom in/out and focus on friends.

#### **3.6 Smart Notifications**
- Users receive notifications when friends are nearby.
- Notifications are customizable.

#### **3.7 Event Integration**
- Campus events are displayed on the map.
- Users can see which friends are attending the same events.

#### **3.8 SOS Feature**
- Users can send emergency alerts with their location to selected contacts.

---

### **4. Non-Functional Requirements**
#### **4.1 Performance**
- The app should handle up to 10,000 concurrent users.
- Location updates should be delivered in real-time (under 1 second).

#### **4.2 Security**
- Use HTTPS and secure WebSocket protocols (wss).
- Implement geospatial indexing for efficient location queries.

#### **4.3 Scalability**
- The app should be deployable on cloud platforms like Vercel and Render.

#### **4.4 Usability**
- The UI should be intuitive and visually appealing.
- The app should be accessible on both desktop and mobile devices.

---

### **5. System Architecture**
#### **5.1 Frontend**
- **React** with **Vite** for fast development.
- **Leaflet.js** or **Google Maps API** for map rendering.
- **Socket.IO Client** for real-time updates.

#### **5.2 Backend**
- **Node.js** with **Express** for server-side logic.
- **MongoDB** for database storage.
- **Socket.IO Server** for real-time communication.

#### **5.3 Database**
- **MongoDB** collections:
  - `users`: Stores user profiles and authentication data.
  - `friends`: Stores friend connections.
  - `locations`: Stores real-time location data.
  - `events`: Stores campus event data.

---

### **6. Folder and File Structure**
Below is the suggested folder and file structure for the project:

```
campus-buddy-finder/
├── backend/
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── locationController.js
│   │   ├── friendController.js
│   │   └── eventController.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Friend.js
│   │   ├── Location.js
│   │   └── Event.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── locationRoutes.js
│   │   ├── friendRoutes.js
│   │   └── eventRoutes.js
│   ├── utils/
│   │   ├── jwtUtils.js
│   │   ├── socketUtils.js
│   │   └── geospatialUtils.js
│   ├── server.js
│   └── config.js
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── Map.jsx
│   │   │   ├── FriendList.jsx
│   │   │   ├── AuthForm.jsx
│   │   │   ├── LocationToggle.jsx
│   │   │   └── SOSButton.jsx
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Login.jsx
│   │   │   └── Register.jsx
│   │   ├── utils/
│   │   │   ├── api.js
│   │   │   └── socket.js
│   │   ├── App.jsx
│   │   └── main.jsx
│   ├── styles/
│   │   ├── global.css
│   │   └── components.css
│   └── vite.config.js
├── README.md
└── package.json
```

---

### **7. Implementation Plan**
1. **Phase 1: Setup and Authentication**
   - Set up the project structure.
   - Implement JWT-based authentication.

2. **Phase 2: Map Integration**
   - Integrate Leaflet.js or Google Maps API.
   - Allow users to drop pins for their location.

3. **Phase 3: Real-Time Location Sharing**
   - Set up Socket.IO for real-time updates.
   - Display friend markers on the map.

4. **Phase 4: Privacy and Location Requests**
   - Add "Share" and "Hide" location toggles.
   - Implement location request functionality.

5. **Phase 5: Deployment and Testing**
   - Deploy the app using Vercel (frontend) and Render/Railway (backend).
   - Conduct extensive testing.

---

### **8. Conclusion**
The **Campus Buddy Finder** is a practical and innovative solution for students to connect and locate friends on campus. By incorporating real-time communication, privacy controls, and a game-like UI, the app offers a unique and engaging user experience. The proposed SRS and folder structure provide a clear roadmap for development and deployment.

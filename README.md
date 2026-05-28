# GateF8 — Backend

> A real-time social networking app for travelers — connect with people at the same airport, chat, and meet before your flight.

📱 **Live on App Store:** [Download GateF8](https://apps.apple.com/in/app/gatef8/id6760747063)

---

## What is GateF8?

GateF8 is a location-aware social app built for airports. Users check in with their departure details — airport, destination, date and time — and instantly connect with other travelers at the same airport. Once the departure time passes, the check-in expires automatically, but all connections and chat history remain.

There is also a global tab where all users can discover and connect with each other regardless of check-in status.

---

## My Role

I designed and built the **entire backend** from scratch — architecture, APIs, real-time systems, third-party integrations, and admin tooling.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | NestJS |
| Database | MongoDB |
| Real-time | WebSockets (Socket.io) |
| Auth | Twilio OTP · JWT · OAuth (Social Login) |
| Notifications | Push Notifications |
| Language | TypeScript |

---

## Key Features I Built

### Authentication System
- **Phone OTP login** via Twilio — send, verify, resecure
- **Email & password** login with JWT-based session management
- **Social login** (OAuth) — third-party provider integration
- Secure token refresh and session expiry logic

### Check-in System
- Users post a check-in with airport name, destination, departure date/time, and an optional message
- Check-ins are **auto-expired** after departure time passes
- Location-aware feed shows only users at the same airport
- Connections and chat history persist after check-in expires

### Real-time Chat
- **WebSocket-based** chat system built with Socket.io
- Connection request flow — send request with optional message → accept → chat unlocked
- Chat rooms scoped per connection pair

### Push Notifications
- Real-time alerts for connection requests, messages, and check-in activity

### Global Discovery Tab
- Secondary feed where all users appear regardless of check-in status
- Same connection request and chat flow applies

### Admin Panel
- Backend APIs for admin operations — user management, content moderation, analytics

---

## Architecture Highlights

- Modular NestJS architecture with clean separation of concerns
- MongoDB schema design optimized for real-time social queries
- Scalable WebSocket gateway with room-based event handling
- Middleware-level auth guards across all protected routes
- Automated check-in expiry using scheduled jobs

---

> *Code is proprietary and not publicly available. Available to discuss architecture, design decisions, and implementation details in interviews.*

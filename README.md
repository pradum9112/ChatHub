# 💬 ChatHub — Real-Time MERN Chat Application

**ChatHub** ek full-stack real-time messaging application hai jo modern web technologies ka upayog karke seamless, secure aur instant communication provide karti hai. Isme **Socket.IO** ka use karke real-time chat, **JWT** authentication aur **MongoDB** me encrypted data storage diya gaya hai.

---

## 🚀 Work Flow Architecture

```text
  ┌────────────────┐         HTTP Requests (REST API)        ┌────────────────┐
  │                ├────────────────────────────────────────►│                │
  │   React.js     │  (Login, Register, Fetch Chats/Users)   │   Node.js &    │
  │   Frontend     │◄────────────────────────────────────────┤   Express.js   │
  │   (Chakra UI)  │        JSON Data / JWT Tokens           │    Backend     │
  │                │                                         │                │
  └───────┬────────┘                                         └───────┬────────┘
          │                                                          │
          │ WebSockets (Socket.io)                                   │ Mongoose ORM
          │ Real-Time Events (Send/Receive Msg, Typing)             │
          ▼                                                          ▼
  ┌────────────────┐                                         ┌────────────────┐
  │ Socket.io Server│                                        │    MongoDB     │
  │ (Real-Time Engine)                                       │    Database    │
  └────────────────┘                                         └───────┬────────┘
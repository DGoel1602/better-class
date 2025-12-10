# Better Class

Better Class is a reverse-Kahoot classroom app where students ask questions and teachers answer. Students can post anonymously or publicly. Teachers moderate questions in a separate environment. The app includes moderation controls, text-to-speech (TTS), banning, authentication, threaded replies, and custom room creation and deletion.

## Key features

- Reverse-Kahoot style: students ask questions, teachers answer
- Anonymous or public questions
- Teacher moderation environment
- Moderation tools: approve/reject questions, delete, ban users
- Text-to-Speech (TTS) for questions and replies
- Authentication with profile pictures
- Threaded replies to messages
- Custom room creation and deletion
- Real-time updates via Socket.IO

## Tech stack

- Client: React + TypeScript (Create React App)
- Server: Node + TypeScript + Express
- Real-time: Socket.IO
- Authentication: Clerk
- Validation: zod
- Forms: react-hook-form
- UI primitives: ShadCN

## Repo layout

- client/ — React front-end
- server/ — TypeScript Node backend

## Getting started

Prerequisites:
- Node.js (LTS recommended)
- npm

Install dependencies:
```bash
# from repo root
cd client
npm install

# in a separate terminal
cd ../server
npm install
```

Build & production:
```bash
# build client
cd client
npm run build

# build server
cd server
npm run build

# start server from built output
cd server
npm start
```

Typical ports:
- Frontend: http://localhost:3000
- Backend: http://localhost:4000

## How it works (high level)

1. Teachers create a room and share the room code or link.
2. Students join the room and submit questions, choosing anonymous or public posting.
3. Questions are delivered to teachers for moderation in a dedicated UI.
4. Teachers approve to publish, reject/delete content, or ban users.
5. Approved questions are visible in the class and can be read with TTS.
6. Real-time synchronization uses Socket.IO.

## Security & privacy

- Ensure anonymous posting does not store or expose metadata that could identify users.
- Track banned users server-side to enforce bans across reconnects.
- Validate and sanitize user-submitted content on the server.

## Contribution

To contribute:
1. Open an issue describing the change.
2. Create a feature/ or fix/ branch.
3. Make changes and ensure TypeScript compiles.
4. Open a Pull Request describing the change and include screenshots where helpful.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Dhruv Goel

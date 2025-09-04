# 🛡️ WackyFlip-Clans

**Social System for Teams, Guilds, and Player Communities**

`WackyFlip-Clans` powers the **community-driven social features** of the [Wacky Flip](https://wackyflip.com) universe. Players can **create, join, and manage clans** (a.k.a. teams or guilds), participate in **group missions**, and climb **clan leaderboards** together. This system encourages teamwork, friendly rivalry, and long-term player engagement.

---

## ✨ Features

| Feature                           | Description                                                                        |
| --------------------------------- | ---------------------------------------------------------------------------------- |
| 🏰 **Clan Creation & Management** | Players can start clans, customize names, emblems, and descriptions                |
| 👥 **Membership System**          | Join, leave, or invite friends to a clan                                           |
| 🗨️ **Clan Chat & Emotes**        | In-clan communication tools for coordination and fun                               |
| 🎯 **Clan Missions**              | Cooperative objectives that reward all members upon completion                     |
| 🏆 **Clan Leaderboards**          | Rankings based on activity, wins, or total points                                  |
| 🎁 **Shared Rewards**             | Distribute clan achievements as coins, gems, or exclusive items                    |
| 🌍 **Cross-Platform Support**     | Clans are synced across web and mobile platforms                                   |
| 🧩 **Integrations**               | Works with `WackyFlip-Social`, `WackyFlip-Challenges`, and `WackyFlip-Tournaments` |

---

## 🛠 Tech Stack

* **Backend:** Node.js + Express / NestJS
* **Database:** PostgreSQL (clan data, memberships, leaderboards)
* **Frontend:** React components for clan profiles, rosters, and chat
* **WebSockets:** Real-time clan chat and notifications
* **Integrations:**

  * `WackyFlip-Social` → friends list & invites
  * `WackyFlip-Challenges` → clan-based missions
  * `WackyFlip-Tournaments` → team-based tournaments

---

## 📁 Repository Structure

```
WackyFlip-Clans/
├── backend/
│   ├── models/
│   │   ├── Clan.ts
│   │   ├── Member.ts
│   │   └── Mission.ts
│   ├── routes/
│   │   ├── createClan.ts
│   │   ├── joinClan.ts
│   │   ├── clanLeaderboard.ts
│   │   └── clanChat.ts
│   └── services/
│       └── rewardDistributor.ts
├── frontend/
│   ├── components/
│   │   ├── ClanProfile.tsx
│   │   ├── ClanChat.tsx
│   │   └── ClanLeaderboard.tsx
│   └── hooks/
└── README.md
```

---

## 🚀 Getting Started

1. Clone the repo:

```bash
git clone https://github.com/wackyflipgame/WackyFlip-Clans.git
cd WackyFlip-Clans
npm install
```

2. Configure environment variables in `.env`:

```
DATABASE_URL=your-database-uri
AUTH_SERVICE_KEY=your-auth-service-key
```

3. Run development server:

```bash
npm run dev
```

---

## 🔄 Example Usage

```ts
// Create a new clan
POST /api/clans/create
{
  "name": "FlipMasters",
  "emblem": "🔥",
  "description": "Best flippers in town!"
}

// Response
{
  "id": "clan_abc123",
  "name": "FlipMasters",
  "members": 1,
  "rank": 0
}
```

---

## 📬 Contribution Guidelines

* Ensure **secure clan ownership transfer** if the leader leaves
* Add **anti-spam tools** for clan chat moderation
* Balance **rewards** for solo vs. clan play
* Write **unit tests** for mission progress & leaderboard updates

---

## 🔗 Related Repositories

* [`WackyFlip-Social`](https://github.com/wackyflipgame/WackyFlip-Social) – Friends, chat, and player interactions
* [`WackyFlip-Challenges`](https://github.com/wackyflipgame/WackyFlip-Challenges) – Clan missions and objectives
* [`WackyFlip-Tournaments`](https://github.com/wackyflipgame/WackyFlip-Tournaments) – Clan-based competitions

---

## 📜 License

MIT © 2025 Wacky Flip Studios

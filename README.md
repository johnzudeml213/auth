# 🔐 HunchClient Authentication Repository

This repository contains the HWID whitelist for HunchClient.

## ⚠️ Private Repository
This repository should be **private** to protect user HWIDs.

## 📝 Whitelist Format

```json
{
  "version": "1.0",
  "updated": 1736946000000,
  "users": [
    {
      "hwid": "user_hwid_hash",
      "username": "PlayerName",
      "tier": "premium",
      "expiry": 0,
      "banned": false,
      "banReason": "",
      "metadata": {}
    }
  ]
}
```

## 🔧 User Tiers

- `developer` - Full access, no expiry
- `premium` - Premium features
- `basic` - Basic access

## 📊 Fields

- `hwid` - SHA-256 hashed hardware ID
- `username` - Display name
- `tier` - User tier (developer/premium/basic)
- `expiry` - Unix timestamp (0 = never expires)
- `banned` - Ban status
- `banReason` - Reason for ban (if applicable)
- `metadata` - Additional user data

## 🚀 Usage

The HunchClient automatically fetches this whitelist on startup and validates users based on their HWID.

## 🔒 Security

- All HWIDs are SHA-256 hashed with salt
- Repository should remain private
- Access via GitHub API with Personal Access Token
- Rate limit: 5000 requests/hour with authentication

---

**HunchClient Authentication System v1.0**
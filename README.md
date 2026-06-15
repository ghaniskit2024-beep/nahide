# আল-কুরআন ও তাফসীর

একটি বাংলা কুরআন, তাফসীর, হাদীস ও ইসলামিক শিক্ষা ওয়েবসাইট।

## 🔧 GitHub Pages-এ Deploy করার নিয়ম

### ১. Firebase Setup (বাধ্যতামূলক)

Firebase ছাড়া লগিন/সেভ ফিচার কাজ করবে না।

1. [Firebase Console](https://console.firebase.google.com/) এ যান
2. নতুন Project তৈরি করুন
3. **Project Settings → Your Apps → Web App** থেকে Config কপি করুন
4. GitHub Repository → **Settings → Secrets and variables → Actions** এ যান
5. নিচের Secrets গুলো Add করুন:

| Secret Name | মান |
|---|---|
| `VITE_FIREBASE_API_KEY` | Firebase API Key |
| `VITE_FIREBASE_AUTH_DOMAIN` | Firebase Auth Domain |
| `VITE_FIREBASE_PROJECT_ID` | Firebase Project ID |
| `VITE_FIREBASE_STORAGE_BUCKET` | Firebase Storage Bucket |
| `VITE_FIREBASE_MESSAGING_SENDER_ID` | Messaging Sender ID |
| `VITE_FIREBASE_APP_ID` | Firebase App ID |
| `VITE_FIREBASE_MEASUREMENT_ID` | Measurement ID |

### ২. GitHub Pages Enable করুন

1. Repository → **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **gh-pages** / `/ (root)`

### ৩. Firebase Authentication Enable করুন

Firebase Console → Authentication → Sign-in method → **Google** Enable করুন

এবং Authorized domains এ আপনার GitHub Pages URL যোগ করুন:
`yourusername.github.io`

### ৪. Firestore Rules

Firebase Console → Firestore Database → Rules এ `firestore.rules` ফাইলের content paste করুন।

## 🚀 Local Development

```bash
# .env.example থেকে .env তৈরি করুন
cp .env.example .env
# .env ফাইলে আপনার Firebase config বসান

npm install
npm run dev
```

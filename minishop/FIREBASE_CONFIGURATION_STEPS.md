# 🔥 Firebase Project Configuration Steps

## 🎯 What You Need to Do Now

Since you've created a new Firebase project, follow these steps to get SMS authentication working:

### Step 1: Enable Authentication
1. Go to your Firebase Console: https://console.firebase.google.com/
2. Select your newly created project
3. Click on "Authentication" in the left sidebar
4. Click on "Get started" if it's your first time
5. Go to the "Sign-in method" tab
6. Find "Phone" in the list and click on it
7. Toggle the "Enable" switch
8. Click "Save"

### Step 2: Upgrade to Blaze Plan (Required for SMS)
⚠️ **IMPORTANT**: SMS authentication requires the Blaze (pay-as-you-go) plan

1. In Firebase Console, click the gear icon → "Project settings"
2. Go to "Usage and billing" tab
3. Click "Modify plan"
4. Select "Blaze" plan
5. Add your payment method (credit/debit card)
6. Confirm the upgrade

**Cost**: SMS in India costs approximately ₹0.65 per message. First 10,000 verifications per month are FREE.

### Step 3: Register Your Web App
1. In Firebase Console, go to Project Overview
2. Click the web icon (`</>`) to add a web app
3. Give it a nickname like "ecommerce-web"
4. Click "Register app"
5. **COPY the configuration object** - you'll need it next!

### Step 4: Get Your Firebase Configuration
After registering your web app, you'll see something like this:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyC...",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project-id",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abcdef"
};
```

**Copy this entire configuration object!**

### Step 5: Update Your App Configuration
Once you have your Firebase configuration, I'll help you update the app with your actual Firebase credentials.

### Step 6: Add Development Domain (IMPORTANT)
🚨 **CRITICAL**: You must add your development server domain to Firebase authorized domains

1. In Firebase Console, go to "Authentication" → "Settings" tab
2. Scroll down to "Authorized domains" section
3. Click "Add domain"
4. Add: `localhost:5173` (this is Vite's default development port)
5. Click "Done"

**Without this step, Google login will fail with "auth/unauthorized-domain" error!**

---

## 📋 Quick Checklist

- [ ] Firebase project created
- [ ] Authentication enabled
- [ ] Phone sign-in method enabled
- [ ] Upgraded to Blaze plan
- [ ] Web app registered
- [ ] Firebase configuration copied

## 🔄 Next Steps

Once you complete these steps and have your Firebase configuration, paste it here and I'll update your app to use your actual Firebase project!

## 💡 Need Help?

If you encounter any issues:
1. Make sure you're signed in to the correct Google account
2. Check that billing is properly set up for SMS
3. Verify that the phone sign-in method is enabled
4. Ensure your web app is registered

Let me know when you have your Firebase configuration ready!
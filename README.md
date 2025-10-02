# 🤖 Facebook PageBot Setup Tutorial

Complete guide to creating and deploying your Facebook Messenger bot

## 📋 Prerequisites

- A Facebook account
- A GitHub account with your bot project
- A hosting platform account (Render or Railway)

---

## Step 1: Initial Facebook Setup

1. Open your web browser and log in to your Facebook account
2. Create a Facebook Page (if you don't have one already)
3. Navigate to [developers.facebook.com/apps](https://developers.facebook.com/apps)

---

## Step 2: Create a Facebook App

1. Click on **"Create App"**
2. Select **"Business"** as the app type
3. Fill in the required details:
   - App Display Name
   - Contact Email
4. Click **"Create App"**

---

## Step 3: Add Messenger and Generate Access Token

1. In your app dashboard, click **"Add Product"**
2. Find **"Messenger"** and click **"Set Up"**
3. Scroll to the **"Access Tokens"** section
4. Click **"Add or Remove Pages"** and connect your Facebook Page
5. Click **"Generate Token"** and copy the Page Access Token

> **⚠️ Important:** Save this token securely. You'll need it in the next step!

---

## Step 4: Configure Your GitHub Project and Deploy

1. Go to your GitHub project repository
2. Open `token.txt` and paste your Page Access Token
3. Commit and push the changes
4. Deploy your project to **Render** or **Railway**:
   - **Render:** Get the live link (e.g., `https://your-app.onrender.com`)
   - **Railway:** Get the public domain URL

> **💡 Note:** Make sure your deployment is successful and the app is running before proceeding!

---

## Step 5: Set Up Webhooks

1. Go back to your Facebook app dashboard
2. Navigate to **Messenger API Settings** → **Webhooks**
3. Click **"Add Callback URL"** or **"Setup Webhooks"**
4. Enter the following:
   - **Callback URL:** `https://your-deployment-url.com/webhook`
   - **Verify Token:** `pagebot`
5. Subscribe to these fields:
   - `messages`
   - `messaging_optins`
   - `messaging_postbacks`
6. Click **"Verify and Save"**
7. Add your page subscription to complete the webhook setup

---

## Step 6: Configure Privacy Policy (Required for Public App)

1. Go to [freeprivacypolicy.com/free-privacy-policy-generator](https://www.freeprivacypolicy.com/free-privacy-policy-generator/)
2. Generate your free privacy policy
3. Copy the privacy policy URL
4. In your Facebook app dashboard, go to **App Settings** → **Basic**
5. Scroll to **"Privacy Policy URL"** and paste your privacy policy link
6. Save the changes

---

## Step 7: Make Your App Live

1. In your app dashboard, look for the toggle to make your app **"Live"**
2. Switch your app from "Development" mode to "Live" mode
3. After making it live, generate a **new Page Access Token**
4. Update your `token.txt` with the new token
5. Redeploy your project on Render or Railway

---

## Step 8: Test Your Messenger Bot

1. Go to your Facebook Page
2. Send a message to your page (e.g., type "help" to see available commands)
3. Check if the bot responds correctly

> **✅ Success!** If your bot responds, congratulations! Your Messenger bot is now live and working!

---

## 📌 Important Notes

- Once your app is live, anyone can message your page and interact with the bot
- Keep your Page Access Token secure and never share it publicly

---

## 🎉 Credits

- Tutorial created by ChatGPT, Blackbox AI, and Adrian
- Modified by Kohi

**Note:** You are free to modify and customize this project as you wish!
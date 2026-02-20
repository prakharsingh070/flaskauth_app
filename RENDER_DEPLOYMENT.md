# Render Deployment Guide for FlaskAuthApp

## Prerequisites
1. ✅ GitHub repository: https://github.com/prakharsingh070/flaskauth_app.git
2. ✅ Render account (free): https://render.com

## Step-by-Step Deployment Instructions

### 1. Login to Render
- Go to [https://render.com](https://render.com)
- Click "Sign up for free" or "Sign In"
- Connect with your GitHub account

### 2. Create New Web Service
1. Click **"New"** button in Render dashboard
2. Select **"Web Service"**
3. Choose **"Connect a repository"**
4. Find and select your repository: `prakharsingh070/flaskauth_app`
5. Click **"Connect"**

### 3. Configure Deployment Settings
Fill in these settings in the Render configuration:

**Basic Settings:**
- **Name**: `flaskauth-app` (or any name you prefer)
- **Region**: US East (Ohio) or closest to you
- **Branch**: `main`
- **Runtime**: `Python 3`

**Build Settings:**
- **Build Command**: `./build.sh`
- **Start Command**: `gunicorn app:app`

**Advanced Settings:**
- **Instance Type**: `Free` (for assignment purposes)

### 4. Environment Variables (Optional but Recommended)
Click **"Advanced"** and add environment variables:

- **SECRET_KEY**: Click "Generate" to create a secure secret key
- **PYTHON_VERSION**: `3.11.0` (or latest Python version)

### 5. Deploy
1. Click **"Create Web Service"**
2. Render will automatically:
   - Clone your GitHub repository
   - Install dependencies from `requirements.txt`
   - Start your Flask app with Gunicorn
   - Provide you with a live URL

### 6. Monitor Deployment
- Watch the **Logs** tab to see deployment progress
- Look for "Deploy successful" message
- Your app URL will be: `https://flaskauth-app.onrender.com`

## Expected Deployment Process
```
==> Building...
    Running build command './build.sh'...
    Installing dependencies from requirements.txt...
    Flask==3.0.0
    Flask-SQLAlchemy==3.1.1
    bcrypt==4.1.2
    gunicorn==21.2.0
    
==> Build successful!

==> Deploying...
    Starting with command: gunicorn app:app
    App is now live at: https://your-app-name.onrender.com
```

## Troubleshooting

### Common Issues:
1. **Build fails**: Check that `requirements.txt` has correct package versions
2. **App won't start**: Verify `gunicorn app:app` command is correct
3. **Database errors**: SQLite should work automatically with Render

### Testing Your Deployed App:
1. Visit your Render URL
2. Test registration with empty fields - should show error messages
3. Test valid registration - should redirect to login
4. Test login functionality

## Verification Steps
After successful deployment:
- ✅ App loads at Render URL
- ✅ Registration form validation works (empty fields show errors)
- ✅ User can register with valid data
- ✅ User can login successfully
- ✅ Dashboard shows user information

## Assignment Requirements Met:
- ✅ **Task 1**: Registration validation bug fixed
- ✅ **Task 2**: Code pushed to GitHub
- ✅ **Task 3**: App deployed on Render
- ✅ **Task 4**: Ready for Google Form submission

## Your Deployment URLs:
- **GitHub Repository**: https://github.com/prakharsingh070/flaskauth_app.git
- **Render Deployed URL**: [Will be provided after deployment]
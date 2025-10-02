<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Facebook Messenger Bot Setup Tutorial</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .container {
            background: white;
            border-radius: 12px;
            padding: 40px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
        }
        h1 {
            color: #1877f2;
            text-align: center;
            margin-bottom: 10px;
        }
        h2 {
            color: #333;
            border-bottom: 3px solid #1877f2;
            padding-bottom: 10px;
            margin-top: 30px;
        }
        h3 {
            color: #555;
            margin-top: 25px;
        }
        .step {
            background: #f8f9fa;
            border-left: 4px solid #1877f2;
            padding: 20px;
            margin: 20px 0;
            border-radius: 6px;
        }
        .step-number {
            background: #1877f2;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: bold;
            display: inline-block;
            margin-bottom: 10px;
        }
        ul {
            padding-left: 25px;
        }
        li {
            margin: 10px 0;
        }
        code {
            background: #e9ecef;
            padding: 3px 8px;
            border-radius: 4px;
            font-family: 'Courier New', monospace;
            color: #d63384;
        }
        .note {
            background: #fff3cd;
            border-left: 4px solid #ffc107;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }
        .important {
            background: #f8d7da;
            border-left: 4px solid #dc3545;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }
        .success {
            background: #d1e7dd;
            border-left: 4px solid #198754;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }
        a {
            color: #1877f2;
            text-decoration: none;
            font-weight: 500;
        }
        a:hover {
            text-decoration: underline;
        }
        .credits {
            background: #e7f3ff;
            border-radius: 6px;
            padding: 20px;
            margin-top: 30px;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🤖 Facebook Messenger Bot Setup Tutorial</h1>
        <p style="text-align: center; color: #666;">Complete guide to creating and deploying your Facebook Messenger bot</p>

        <h2>📋 Prerequisites</h2>
        <ul>
            <li>A Facebook account</li>
            <li>A GitHub account with your bot project</li>
            <li>A hosting platform account (Render or Railway)</li>
        </ul>

        <div class="step">
            <span class="step-number">Step 1</span>
            <h3>Initial Facebook Setup</h3>
            <ul>
                <li>Open your web browser and log in to your Facebook account</li>
                <li>Create a Facebook Page (if you don't have one already)</li>
                <li>Navigate to <a href="https://developers.facebook.com/apps" target="_blank">developers.facebook.com/apps</a></li>
            </ul>
        </div>

        <div class="step">
            <span class="step-number">Step 2</span>
            <h3>Create a Facebook App</h3>
            <ul>
                <li>Click on <strong>"Create App"</strong></li>
                <li>Select <strong>"Business"</strong> as the app type</li>
                <li>Fill in the required details:
                    <ul>
                        <li>App Display Name</li>
                        <li>Contact Email</li>
                    </ul>
                </li>
                <li>Click <strong>"Create App"</strong></li>
            </ul>
        </div>

        <div class="step">
            <span class="step-number">Step 3</span>
            <h3>Add Messenger and Generate Access Token</h3>
            <ul>
                <li>In your app dashboard, click <strong>"Add Product"</strong></li>
                <li>Find <strong>"Messenger"</strong> and click <strong>"Set Up"</strong></li>
                <li>Scroll to the <strong>"Access Tokens"</strong> section</li>
                <li>Click <strong>"Add or Remove Pages"</strong> and connect your Facebook Page</li>
                <li>Click <strong>"Generate Token"</strong> and copy the Page Access Token</li>
            </ul>
            <div class="important">
                <strong>⚠️ Important:</strong> Save this token securely. You'll need it in the next step!
            </div>
        </div>

        <div class="step">
            <span class="step-number">Step 4</span>
            <h3>Configure Your GitHub Project and Deploy</h3>
            <ul>
                <li>Go to your GitHub project repository</li>
                <li>Open <code>token.txt</code> and paste your Page Access Token</li>
                <li>Commit and push the changes</li>
                <li>Deploy your project to <strong>Render</strong> or <strong>Railway</strong>:
                    <ul>
                        <li><strong>Render:</strong> Get the live link (e.g., <code>https://your-app.onrender.com</code>)</li>
                        <li><strong>Railway:</strong> Get the public domain URL</li>
                    </ul>
                </li>
            </ul>
            <div class="note">
                <strong>💡 Note:</strong> Make sure your deployment is successful and the app is running before proceeding!
            </div>
        </div>

        <div class="step">
            <span class="step-number">Step 5</span>
            <h3>Set Up Webhooks</h3>
            <ul>
                <li>Go back to your Facebook app dashboard</li>
                <li>Navigate to <strong>Messenger API Settings</strong> → <strong>Webhooks</strong></li>
                <li>Click <strong>"Add Callback URL"</strong> or <strong>"Setup Webhooks"</strong></li>
                <li>Enter the following:
                    <ul>
                        <li><strong>Callback URL:</strong> <code>https://your-deployment-url.com/webhook</code></li>
                        <li><strong>Verify Token:</strong> <code>pagebot</code></li>
                    </ul>
                </li>
                <li>Subscribe to these fields:
                    <ul>
                        <li><code>messages</code></li>
                        <li><code>messaging_optins</code></li>
                        <li><code>messaging_postbacks</code></li>
                    </ul>
                </li>
                <li>Click <strong>"Verify and Save"</strong></li>
                <li>Add your page subscription to complete the webhook setup</li>
            </ul>
        </div>

        <div class="step">
            <span class="step-number">Step 6</span>
            <h3>Configure Privacy Policy (Required for Public App)</h3>
            <ul>
                <li>Go to <a href="https://www.freeprivacypolicy.com/free-privacy-policy-generator/" target="_blank">freeprivacypolicy.com/free-privacy-policy-generator</a></li>
                <li>Generate your free privacy policy</li>
                <li>Copy the privacy policy URL</li>
                <li>In your Facebook app dashboard, go to <strong>App Settings</strong> → <strong>Basic</strong></li>
                <li>Scroll to <strong>"Privacy Policy URL"</strong> and paste your privacy policy link</li>
                <li>Save the changes</li>
            </ul>
        </div>

        <div class="step">
            <span class="step-number">Step 7</span>
            <h3>Make Your App Live</h3>
            <ul>
                <li>In your app dashboard, look for the toggle to make your app <strong>"Live"</strong></li>
                <li>Switch your app from "Development" mode to "Live" mode</li>
                <li>After making it live, generate a <strong>new Page Access Token</strong></li>
                <li>Update your <code>token.txt</code> with the new token</li>
                <li>Redeploy your project on Render or Railway</li>
            </ul>
        </div>

        <div class="step">
            <span class="step-number">Step 8</span>
            <h3>Test Your Messenger Bot</h3>
            <ul>
                <li>Go to your Facebook Page</li>
                <li>Send a message to your page (e.g., type "help" to see available commands)</li>
                <li>Check if the bot responds correctly</li>
            </ul>
            <div class="success">
                <strong>✅ Success!</strong> If your bot responds, congratulations! Your Messenger bot is now live and working!
            </div>
        </div>

        <div class="note">
            <h3>📌 Important Notes</h3>
            <ul>
                <li>Once your app is live, anyone can message your page and interact with the bot</li>
                <li>Keep your Page Access Token secure and never share it publicly</li>
            </ul>
        </div>

        <div class="credits">
            <h3>🎉 Credits</h3>
            <ul>
                <li>Tutorial created by ChatGPT, Blackbox AI, and Adrian</li>
                <li>Modified by Kohi</li>
            </ul>
            <p style="margin-top: 15px;"><strong>Note:</strong> You are free to modify and customize this project as you wish!</p>
        </div>
    </div>
</body>
</html>
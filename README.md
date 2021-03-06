# Twilio Sendgrid use Node to Send Email via API

https://app.sendgrid.com/guide/integrate/langs/nodejs

https://github.com/coding-to-music/twilio-sendgrid-node-send-email

## How to send email using Node.js

### Make sure you have the prerequisites
Our library requires Node.js version 0.10, 0.12, or 4.

## Create an API key
This allows your application to authenticate to our API and send mail. You can enable or disable additional permissions on the API keys page.

My First API Key Name
 
## Create an environment variable
Update your development environment with your SENDGRID_API_KEY. Run the following in your shell:

```java
echo "export SENDGRID_API_KEY='YOUR_API_KEY'" > sendgrid.env
echo "sendgrid.env" >> .gitignore
source ./sendgrid.env```

Output
```java
```

## Install the package
The following recommended installation requires npm. If you are unfamiliar with npm, see the npm docs. Npm comes installed with Node.js since node version 0.8.x, therefore you likely already have it:

```java
npm install --save @sendgrid/mail
```

Output
```java
```

## Send your first email
The following is the minimum needed code to send an email:

```java
// using Twilio SendGrid's v3 Node.js Library
// https://github.com/sendgrid/sendgrid-nodejs
javascript
const sgMail = require('@sendgrid/mail')
sgMail.setApiKey(process.env.SENDGRID_API_KEY)
const msg = {
  to: 'test@example.com', // Change to your recipient
  from: 'test@example.com', // Change to your verified sender
  subject: 'Sending with SendGrid is Fun',
  text: 'and easy to do anywhere, even with Node.js',
  html: '<strong>and easy to do anywhere, even with Node.js</strong>',
}
sgMail
  .send(msg)
  .then(() => {
    console.log('Email sent')
  })
  .catch((error) => {
    console.error(error)
  })
  ```

Output
```java
```

Implement and run the code above. If that runs without error, click “Next” and we’ll check to see if your email came through SendGrid.
# LambdaLayers
Firebase Admin - AWS Lambda Layer

Firebase Admin Version in Layer: 10.2.0

Use Case: If you are trying to create a AWS Lambda function to access your Firebase resources via Firebase Admin

To Use: 
1. Goto your AWS Lambda console. Under "Additional Resources", click on Layers.
2. Create a new Layer. Select "Upload a .zip file" (use the firebaseadmin.zip file in this repo). 
3. To attach this layer to your lambda function, goto your Function Overview, click on Layers->Add a layer. 
4. Select the layer you created in Step #2.
5. That's it! 

Once you have attached the layer to your lambda function, you would be to 'require' it. Similar to the following

const { initializeApp, applicationDefault, cert } = require('firebase-admin/app');
const { getFirestore } = require('firebase-admin/firestore');

Check the Firebase docs for more details -> https://firebase.google.com/docs/admin/setup

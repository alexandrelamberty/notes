# Deploy multiple projects on Firebase Hosting

.firebaserc

```json
{
  "projects": {
    "dev": "myapp-staging", // alias "dev" to the project "myapp-staging"
    "prod": "myapp-prod" // alias "prod" to the project "myapp-prod"
  },
  "targets": {
    "myapp-staging": {
      // project ID
      "hosting": {
        "target_1": [
          // user-defined identifier for the Hosting site, call it whatever you'd like
          "myapp-staging-adminpanel" // name of the Hosting site as listed in your Firebase project
        ],
        "target_2": ["myapp-staging-catalog"]
      }
    }
  }
}
```

firebase.json

```json
{
  "hosting": [
    {
      "target": "target_1",
      "public": "build",
      "ignore": ["firebase.json", "**/.*", "**/node_modules/**"]
    },
    {
      "target": "target_2",
      "public": "test",
      "ignore": ["firebase.json", "**/.*", "**/node_modules/**"]
    }
  ]
}
```

The [target] is defined in the firebase.json

The [site] is the name of one of your hosting site in firebase.

```bash
firebase target:apply hosting [target] [site]
```

You can check your ressource targets

```bash
firebase target
```

```bash
firebase use dev
firebase deploy --only hosting:adminpanel

firebase use prod
firebase deploy --only hosting:adminpanel
```

https://fireship.io/lessons/deploy-multiple-sites-to-firebase-hosting/

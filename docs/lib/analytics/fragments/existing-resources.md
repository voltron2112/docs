Using existing Amazon Pinpoint resources is not supported.  Instead, add a new resource to your Amplify project:

```bash
amplify add analytics
```

Existing data will need to be migrated manually from the existing Pinpoint resource to the new one.

Note that before you can add an AWS resource to your application, the application must have the Amplify libraries installed. If you need to perform this step, see [Install Amplify Libraries](~/lib/project-setup/create-application.md#n2-install-amplify-libraries). 
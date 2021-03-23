Using an existing AWS AppSync API is not supported.  Instead, add a new API to your Amplify project:

```bash
amplify add api
```

Existing data will need to be migrated manually from the existing AppSync API resource to the new one.  If your existing AppSync API is backed by a DynamoDB data source, you can change your new API's Data Source to point to the existing DynamoDB table.  Before doing this though, ensure that your schema for both the new API and the existing API are identical, and that conflict detection is configured the same way for both APIs, otherwise the new API will return schema validation errors.

Visit the [AppSync console](https://console.aws.amazon.com/appsync/), select your new API, select "Data Sources", and then for each table, select the DynamoDB table resource used by the existing API.

Note that before you can add an AWS resource to your application, the application must have the Amplify libraries installed. If you need to perform this step, see [Install Amplify Libraries](~/lib/project-setup/create-application.md#n2-install-amplify-libraries). 
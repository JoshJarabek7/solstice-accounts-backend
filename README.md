Early Works for Solstice Account Backend Service

Since we are going to be an Apple Exclusive app, we will exclusively use Sign In with Apple ID to simplify things, and we can take advantage of MongoDB Realm to keep data local to the device, keep their data in-sync, and offload a lot of risk to MongoDB, rather than accessing it on our servers.

## Planning

Features/Services:
    - Users should not be able to see accounts they've blocked and users who have them blocked shouldn't be able to see them
    - Authentication with Apple Sign-In JWT
    - User Deactivation
    - User Deletion
    - Retrieval of User's Data when requested
    - Banning Users
    - Reporting of Users
    - Suspension
    - Notifications
    - User Search by handle
    - Background Checks and ID Verification

Determine what can and cannot be done on the device with MongoDB Realm.
We should strive to keep most data and compute local to the user's device.
Only try to collect the minimal amount of data required to make the application work.
Keep other backend services to a minimal in terms of their MongoDB classes.
This will keep the bson ID for that user, which can be passed to the other services.
Separate Account from Profile to keep PII to a minimum.
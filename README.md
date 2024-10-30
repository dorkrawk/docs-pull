# docs-pull

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/dorkrawk/docs-pull.git
   cd docs-pull
   ```

2. Install the required gems:
   ```
   bundle install
   ```

3. Set up Google API credentials:
   - Go to the [Google Cloud Console](https://console.cloud.google.com/).
   - Create a new project or select an existing project.
   - Enable the Google Docs API and Google Drive API for the project.
   - Create OAuth 2.0 credentials and download the JSON file.
   - Save the JSON file as `credentials.json` in the root directory of the repository.

## Running the Application

1. Run the Ruby script to pull the contents of a Google Doc:
   ```
   ruby google_doc_pull.rb
   ```

2. Follow the instructions to authorize your Google account. The credentials will be stored to avoid re-authorization after the first time.

## Notes

- The application uses the `googleauth` gem for OAuth2 authorization and the `google_drive` gem to pull the contents of a Google Doc.
- Make sure to keep your `credentials.json` file secure and do not share it with others.

## credentials.json

The `credentials.json` file should look like this:

```json
{
  "installed": {
    "client_id": "YOUR_CLIENT_ID",
    "project_id": "YOUR_PROJECT_ID",
    "auth_uri": "https://accounts.google.com/o/oauth2/auth",
    "token_uri": "https://oauth2.googleapis.com/token",
    "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
    "client_secret": "YOUR_CLIENT_SECRET",
    "redirect_uris": [
      "urn:ietf:wg:oauth:2.0:oob",
      "http://localhost"
    ]
  }
}
```

# Notion-Api-Insomnia
Insomia workspace with Notion APIs

Ported from Notion's [official postman collection](https://www.postman.com/notionhq/).

Added a dummy request to retrieve OAuth token for Notion's 
[public integretions](https://developers.notion.com/docs/authorization#authorizing-public-integrations).

Added the environment:
```JSON
{
  "notion_api_version": "2021-08-16",
  "database_id": "",
  "user_id": "",
  "block_id": "",
  "page_id": "",
  "bearer_prefix": "Bearer",
  "access_token": "{% token 'req_b4f6a2fe7b41494fa2d57131513342b5', true, false, false %}",
  "client_id": "",
  "oauth_secret": "",
  "oauth_redirect_uri": ""
}
```

The variable `access_token` uses the Insomia plugin [insomnia-plugin-accesstoken](https://insomnia.rest/plugins/insomnia-plugin-accesstoken) to reference the OAuth access token.
Every other request then uses bearer authentication with this var as the token. You can just set it to your token if you don't need public integration.

The varables ending in _id are notions uuid.

Will probably add documentation in the future.

Pull requests and issues are welcome!

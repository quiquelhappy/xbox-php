# Xbox PHP API Wrapper (oAuth-based)
### Azure project setup
 1. Create an azure oAuth project, [here](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade)
	 a Name it whatever you want
	 b For the supported account types, choose 'Accounts in any organizational directory (Any Azure AD directory - Multitenant) and personal Microsoft accounts (e.g. Skype, Xbox)'
	 c Set a redirect URI such as http://localhost:300/authorize/
2. Goto **Dashboard → App → Certificates & secrets** and under `Client secrets` click on `+ New client secret`
	a Enter  `Description`, eg:  `Example Secret Key`
	b For  `Expires`  choose  `Never`

Congrats! Now you just have to copy the **client-id** (available on your [project description](https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade)), and your **client-secret**, available on the secret you just created (click on the copy button). Please, store these values safely, and [do not share client-secret with anyone](https://www.codementor.io/@ccornutt/keeping-credentials-secure-in-php-kvcbrk55z)!

### Client installation
`composer require <to-do>`

### Client usage

    $client = new quiquelhappy\xbox\Client($clientId,$clientSecret);

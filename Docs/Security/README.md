# Ukey1 for Developers - Security

We've designed and built Ukey1 platform specifically with the need to meet strict GDPR requirements. Not only for our needs but also for our clients - web developers, webmasters, startup founders as well as for managers of blue fishes. That's why we honor following principles:

- privacy by design and by default
- data protection by design and by default
- security by design and by default

Even with limited budget we are able to provide the highly available and auto-scalable low-cost service with the best security measures possible.

## Data location

Our databases are currently located in three locations - London in United Kingdom, Frankfurt in Germany and Dallas in United States. With the respect to GDPR, we store data about European citizens exclusively in European data centers, data of citizens of other countries are stored in Dallas.

## Measures

We take security and data protection seriously. We follow security guidelines and recommendations and actively looking for possible threats.

Here's our statement...

Our domain is protected with [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions) and it has [HSTS](https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security) enabled. It means we use secure [HTTPS](https://en.wikipedia.org/wiki/HTTPS) communication only. We also protect our service against [DDoS](https://en.wikipedia.org/wiki/Denial-of-service_attack) attacks using Cloudflare. Availability of our systems is also monitored every minute using IBM's monitoring service.

Because we are paranoid, we follow strict password policy. No password, access or encryption key is in the code and no one has direct access to databases. It also means that no developer can use a copy of live database. There are also other threats like [injections](https://www.owasp.org/index.php/Injection_Flaws), [session hijacking](https://www.owasp.org/index.php/Session_hijacking_attack), [CSRF](https://en.wikipedia.org/wiki/Cross-site_request_forgery), [timing attacks](https://en.wikipedia.org/wiki/Timing_attack) and more. We know and we are prepared.

For the case an attacker breaks into our databases, users' passwords are hashed with cryptographically strong salt and all valuable data including personal identification data like emails, names, IP addresses and images, or access credentials of apps, are encrypted.

And we cannot forget to audit logs. We log every operation. Even each access to every single personal data field.

## Additional security settings for your app communicating with API

We provide 4 additional security measures to enhance protection of the authentication process. All settings are available in our developer dashboard, for each app in the section *API keys*. **We generally recommend to activate as much protection as possible.**

### Domain protection

Whether you send API requests on client-side (via ajax) or server-side, there is a Domain Protection available in our dashboard. This protection is strongly recommended.

For client-side requests, this protection serves as a firewall for cross-origin requests. Because your App ID is publicly visible for client-side requests, a potential attacker could act on your behalf on any other domain name. When you enable this protection, our servers will allow requests only from specified domains. Learn more about [CORS](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing).

If you use server-side requests, you can still use this protection as another level of protection. When enabled, `X-Origin` header with the correct value must be used within each server-side request.

### Server-only protection

Generally, server-to-server requests are more secure than client-side requests because you can use enhanced security measures - e.g. the request signed by your secret key, IP whitelisting etc. If you are not going to use client-side requests, we recommend you to activate the server-only protection.

### IP protection

IP whitelisting is useful for server-to-server connections but it can be used also for client-side requests, if the target app should stay accessible privately only from few places. You're able to set unlimited list of IP addresses or subnet masks.

### Return URL protection

For each case of connection, you should enable protection of your return URLs. Return URL is the URL which is used for redirecting user back from our gateway to your website. If your return URLs are random, you can still use this protection. For example `https://example.org/callback/` will allow `https://example.org/callback/` as well as `https://example.org/callback/abcdefgh/?tracking=123456` but not `https://example.org/invalid`.

-----

[Home](../../README.md) | [How it works](../HowItWorks/README.md) | [Permissions](../Permissions/README.md) | [Security](../Security/README.md) | [FAQ](../FAQ/README.md)

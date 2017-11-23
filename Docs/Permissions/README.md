# Ukey1 for Developers - Permissions

Ukey1 works differently - you have to ask for permissions for each data field you want to get. This gives users full control over their personal data. It may look like a lot of clicks but the truth is that your users will appreciate it. We've prepared our authorization screen to be as simple as possible and we're going to implement adaptive features to simplify the process.

## Minimization

One of the assumptions of [GDPR](https://ico.org.uk/for-organisations/guide-to-the-general-data-protection-regulation-gdpr/) is data minimization. It means you should ask users only for data you really need to minimize the chance of data leak.

## Mandatory fields

By default, all data fields are optional, so users may not to grant access for you. Actually, they have to confirm every single field they want to share with you. This is called a "positive opt-in". Basically, we assume you need consent from your users. And thanks to this authorization scheme you have a proof of such consent.

Let's recall four basic lawful basics:

- Consent of the data subject (positive opt-in)
- Processing is necessary for the performance of a contract with the data subject or to take steps to enter into a contract
- Processing is necessary for compliance with a legal obligation
- Necessary for the purposes of legitimate interests pursued by the controller or a third party, except where such interests are overridden by the interests, rights or freedoms of the data subject

In some cases you need (or want) to use another legal basis. In fact, sometimes you have to use another legal basis. If you're not sure, just keep in touch and we'll be glad to help you. In such cases there are mandatory fields available. When applicable, you can append an exclamation mark `!` to the field code. This will cause that user has to share such field with your app.

Please note and be sure that if you want to use mandatory fields, your privacy policy includes information about legal basis you use. It should be included anyway.

## Data fields

Here is the full list of available fields...

| Description                       | Field code  | Can be mandatory  | Mandatory code |
| --------------------------------- | ----------- | ----------------- | -------------- |
| First name                        | `firstname` | *yes*             | `firstname!`   |
| Surname                           | `surname`   | *yes*             | `surname!`     |
| Email                             | `email`     | *premium feature* | `email!`       |
| Profile image                     | `image`     | *premium feature* | `image!`       |
| Country code (ISO 3166-1 alpha-2) | `country`   | *yes*             | `country!`     |
| Language code (ISO 639-1)         | `language`  | *yes*             | `language!`    |

-----

[Home](../../README.md) | [How it works](../HowItWorks/README.md) | [Permissions](../Permissions/README.md) | [Security](../Security/README.md) | [FAQ](../FAQ/README.md)

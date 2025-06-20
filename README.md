# profile-editor
Bootstrap v5 Member Profile Editor

## Background

There are two workflows:
* new member creating their profile
* existing member updating their profile

For new members, there are 4 scenarios:
* user is the participant and is under-age (under 18)
* user is the participant and is of age (18 or over)
* user is the participant's parent/guardian while the participant is under-age (under 18)
* user is the participant's parent/guardian while the participant is of age (18 or over)

(We don't care about the edge cases where the participant is being impersonated or proxied.)

## Design References

We'll use Badminton Canada's Tournament Software portal as the primary source, since we want to:
* provide a one-stop registration system that mimics BCAN's portal
* use BCAN's port as a potential import source

As a secondary sources, we'll reference The Locker (managed by Coaching Association of Canada)
and PCNS (Pickleball Canada National System).

| Data | BCAN | Locker | PCNS |
| ---- | ---- | ------ | ---- |
| Photo | Yes (8 MB) | No | Yes |
| Title | Yes | No | No |
| Gender (Identity) | Male/Female | Man/Woman/Non-Binary/Two-Spirit/Prefer not to answer | Male/Female/Gender Diverse |
| Nationality | Country of your passport | | |
| Street Address | 3 lines | 1 line | 2 lines |
| Contact | Phone/Phone 2/Phone (mobile)/Fax/Fax 2/Website | Phone | Phone/Alternate Phone/Emergency Contact Name+Phone |
| Email Subscriptions | Receive newletter/marketing messages/performance updates checkboxes | Email consent (Yes/No) | |
| Aboriginal ancestry | None/First nations/Metis/Inuit/Ancestry but non status | Indigenous Peoples checkbox | |
| Language | | English/French/Bilingual/Other | |
| Demographics | | Candian Armed Forces/RCMP/People with a Disability | Member with a disability (Yes/No/Prefer not to answer) |
| NCCP Number | Yes | Implied | |
| Sport-Specific | BWF Member ID/National ID/BON Member ID | | Region |
| Mobile Form | No | Manual Switch | Auto-Detect |

## Country Codes

* [GeoNames Country Codes](https://www.geonames.org/countries/)
* [MaxMind GeoIP Countries](https://dev.maxmind.com/geoip/docs/databases/city-and-country/)
  * [Legacy GeoIP](https://dev.maxmind.com/geoip/docs/web-services/legacy/) describes A1 (Anonymous Proxy), A2 (Satellite PRovider), EU (IP block used by multiple European countries), and AP (IP block used by multiple Asia/Pacific region countries)
* [National Olympic Committees (NOC)](https://www.olympics.com/en/news/paris-2024-olympics-full-list-ioc-national-olympic-committee-codes)
  * Wikipedia's [IOC Country Codes](https://en.wikipedia.org/wiki/List_of_IOC_country_codes) contains historical usage
* Wikipedia's [Telephone Country Codes](https://en.wikipedia.org/wiki/List_of_telephone_country_codes)

## Latest Mock-Up

![Start Page!](/screenshots/1-start.png)

![Agreement!](/screenshots/2a-agreement.png)

![Parental Consent!](/screenshots/2b-parental-consent.png)

![Import Profile!](/screenshots/3a-import-profile.png)

![Profile Editor!](/screenshots/3b-profile-editor.png)

![Offcanvas Pronouns!](/screenshots/3c-offcanvas-pronouns.png)

![Offcanvas Voluntary Disclosure!](/screenshots/3d-offcanvas-voluntary.png)

![Payment!](/screenshots/4a-payment.png)

![Thank You!](/screenshots/4b-thankyou.png)

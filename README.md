Canadian Postal Code & Political Constituencies Dataset
========================================================

This project is a lightweight web crawler and dataset that maps every postal code in Canada to its political constituency information and member of parliament. This dataset is proudly used by [Democracy Bot](https://www.democracybot.ca/), a non-profit that allows Canadians to quickly send letters to their member of parliament through text messages.

This project was created to increase accessibility and transparency regarding political data in Canada, and in response to general demand (https://open.canada.ca/en/suggested-datasets/postal-codes-and-federal-ridings for example). Outside of politics the database is also useful as it holds all the general Canadian postal code information in one place.

-----

## Dataset Overview

The database contains 844 216 entries in total. 9960 of the postal codes do not have political information (only postal_code, province, county, and place). In these instances additional address information was required to map the information to a constituency or the location is extremely remote and has no available political information.

The dataset is accurate with the elections Canada website, as of December 2023

-----

## Relation Schema

| Attribute | Data Properties | Description |
| ----- |:-----| ------------|
| postal_code | varchar(7) | Postal code being mapped to voting constituency |
| MP | varchar(255) | The member of parliament representing given postal code |
| MP_email | varchar(255) | Member of parliament email contact |
| constituency | varchar(255) | the name of the voting constituency |
| province | varchar(32) | province where constituency is located |
| county | varchar(255) | name of the county associated with constituency |
| place | varchar(255) | general region identifier i.e. "Hunter River" or "Stratford" |
| constituency_population | int | Population of voting constituency |
| constituency_registered_voters | int | Number of registered voters in constituency |
| constituency_polling_divisions | int | Number of polling divisions, each division has a voting station |
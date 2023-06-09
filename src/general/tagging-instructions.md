# Tagging Instructions

# Introduction

[BTCMap.org](https://btcmap.org) uses an open source dataset provided by [OpenStreetMap](https://www.openstreetmap.org). If you are serious about supporting bitcoin adoption in your area, you should consider opening an OSM account and contributing to our mission to enable Bitcoiners to easily find places to spend sats anywhere on the planet.

# Copyright

https://www.openstreetmap.org/copyright

> OSM contributors are reminded never to add data from any copyrighted sources (e.g. Google Maps or printed maps) without explicit permission from the copyright holders.

# Noobs 🙂

If you only want to add a few places and you aren't planning to maintain them, there is a [simple form](https://btcmap.org/add-location) you can fill and our community will add your data to the OSM database. Our resources are limited so please consider learning how to add and edit data on OSM yourself if you have time.

If you want to verify information on an existing location there is also a [simple form](https://btcmap.org/verify-location) to do that.

You can learn more about OSM tagging in the [Beginners Guide](https://wiki.openstreetmap.org/wiki/Beginners%27_guide). We have also made a [walkthrough video](https://rumble.com/v1ldybp-how-to-create-an-entry-on-openstreetmap..html).

You can also slide into the [BTC Map Discord](https://discord.gg/wPqva83uzq) if you have any questions. You'll be editing like a Shadowy Supertagger in no time!

# Shadowy Supertaggers 🥷

Earn [badges](https://btcmap.org/badges), [sats](lightning-tips.html) and recognition on BTC Map for your contributions. Your efforts will be featured on our [Activity Feed](https://btcmap.org/activity), [Leaderboard](https://btcmap.org/leaderboard) and you will get your very own [Tagger Profile](https://btcmap.org/tagger/16971158) too!

Once you have an OpenStreetMap account, you can use the [OSM iD web app](https://learnosm.org/en/beginner/id-editor/#the-id-editor) to edit the maps directly on [OpenStreetMap.org](https://www.openstreetmap.org/edit).

A video tutorial can be found [here](https://rumble.com/v1ldybp-how-to-create-an-entry-on-openstreetmap..html).

## Contributing

Add new or update existing locations directly as you see fit or help with the backlog of submissions from the Noob Form at one of the links below:

- [New locations ready for Shadowy Supertaggers](https://github.com/teambtcmap/btcmap-data/issues?q=is%3Aissue+is%3Aopen+sort%3Acreated-asc+label%3Alocation-submission+-label%3Aassigned+no%3Aassignee) 🆕

- [Verified locations ready for Shadowy Supertaggers](https://github.com/teambtcmap/btcmap-data/issues?q=is%3Aopen+is%3Aissue+label%3A%22verify-submission%22+-label%3Aassigned+no%3Aassignee) 📍

If you're a serious tagger, please consider joining the [Shadowy Supertagger Team](https://github.com/orgs/teambtcmap/teams/shadowy-supertaggers) on GitHub so you can manage issues. We also have a Supertagger [Discord](https://discord.gg/f88bzkDA4u) channel.

Please use the following guidance when editing locations:

### Physical Verification and Local Knowledge

Our main goal is to provide the public with an accurate data-set and locals know best. Please try to prioritize locations with close physical proximity to you. Make sure that you're relying on the most accurate data, such as:

- On-site survey.
- Direct phone/email ([e.g.](verifying-locations.html))/social media survey.
- Various online sources (be careful about [copyright](tagging-instructions.html#copyright)), not all online data is free to use! The official website of the merchant is usually the best online source.

Relying on a form submission without any additional checks is discouraged. An extra step of due diligence should be taken to ensure we are adding accurate data to OpenStreetMap and being good stewards of the database.

### Double-check Coordinates

If taking on issues submitted from the Add Location form, you can and should make adjustments to the exact pin location IF you notice it is incorrect. The person submitting the location will not be a mapping expert and that it ok - this is where the extra validation by the Supertagger can help improve the data accuracy. Any submissions with completely invalid locations (like in the middle of the ocean) can be closed as not-planned with the reason provided in a comment.

### Source of Data

Each submission will contain information about the source of the data so that taggers will know if it was completed by the business owner, a customer, or by another method. Some submissions may also include contact information which can be used to follow-up if further information is required.

## Tagging Guidance

### Points, not Ways

Please tag _points_ and not _ways_. If ways already exist, do not create any additional points and tag the existing ways instead. More information on element types can be found [here](https://wiki.openstreetmap.org/wiki/Elements).

### Required Tags

`currency:XBT=yes` - This denotes the bitcoin _currency_ **is** generally accepted, but doesn't specify the supported _payment types_.

`currency:XBT=no` - This denotes the bitcoin _currency_ **is not** generally accepted.

### Strongly recommended tags

The following tags drive the behavior of our apps and so please be as specific as you can when tagging.

`payment:onchain=yes` - Denotes that on-chain payments _are_ accepted.

`payment:onchain=no` - Denotes that on-chain payments _are not_ accepted.

`payment:lightning=yes` - This denotes that Lightning payments _are_ accepted.

`payment:lightning=no` - This denotes that Lightning payments _are not_ accepted.

`payment:lightning_contactless=yes` - This denotes that NFC Lightning payments _are_ accepted.

`payment:lightning_contactless=no` - This denotes that NFC Lightning payments _are not_ accepted.

#### Verified tags - [more information](map-legend.html#verified)

`survey:date=yyyy-mm-dd` - Use this tag when the location has been physically verified in person by you. Please use the correct ISO date format as shown.

`check_date=yyyy-mm-dd` - Use this tag when the location has been verified with local knowledge or extrapolation. Please use the correct ISO date format as shown.

`check_date:currency:XBT=yyyy-mm-dd` - You can reduce the scope of the information checked by using this tag. For example, if you had only checked the bitcoin tags. Please use the correct ISO date format as shown.

You should verify all the present tags (if possible) when you are adding bitcoin tags to an existing location.

### Legacy Tags

`payment:bitcoin=yes` - This is a [very popular legacy tag](https://taginfo.openstreetmap.org/tags/payment:bitcoin=yes#overview) implying both `currency:XBT=yes` and `payment:onchain=yes`. You should remove the `payment:bitcoin=yes` tag when adding the `currency:XBT=yes` tag.

We still search for these legacy tags for general display in the apps, but we won't be specific on the payment types supported. You should really remove them when updating with the current tagging rules.

Here is the [full list](https://data.btcmap.org/legacy-nodes.html) of the legacy places and you are encouraged to verify them. Clicking on any place in that list will open the [OSM iD editor](https://learnosm.org/en/beginner/id-editor/#the-id-editor). If the place still exists, modify it using the guidance above. If the place doesn't exist, you can remove it from OSM. In a case when a place still exists but no longer accepts bitcoins, simply remove the `payment:bitcoin=yes` tag.

### Other OpenStreetMap tags

OpenStreetMaps is an incredibly flexible platform with tags for a variety of different features.

Here are some useful links that may be useful for your location:

- [Opening Hours](https://wiki.openstreetmap.org/wiki/Key:opening_hours)
- [Food / Cuisine](https://wiki.openstreetmap.org/wiki/Key:cuisine)

It is easy to look up all the available tags and their use-cases in the OSM [Wiki](https://wiki.openstreetmap.org/wiki/Main_Page).

### Changeset Comments

Every edit on OpenStreetMap has the option to add a changeset comment. This is an important way for other OSM contributors to get a quick idea of what the edit contained. You can include a short description of your changes in this field.

Additionally, another OSM contributor may ask a question for clarification about one of your edits. You should receive an e-mail notification when this happens. Please make an effort to respond to any non-frivolous and respectful questions.

Please include the `#btcmap` hashtag in your changeset comments so that the activity is associated with our initiative.

## Completing Issues

After you have added or edited a location on OpenStreetMap and before closing the GH Issue as complete, it is good practice to leave a comment listing any additional steps you took to verify the accuracy of the data. Please also paste a link to the changeset on OSM so others can reference it and provide additional comments if necessary.

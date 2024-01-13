[https://apify.com/epctex/kickstarter-scraper?fpr=yhdrb](https://apify.com/epctex/kickstarter-scraper?fpr=yhdrb)

# Kickstarter Scraper
The ultimate and most all-encompassing Kickstarter tool you'll ever discover. With powerful search features, you can instantly locate and access any live project on Kickstarter.com. Search by location, project status, funding progress, and more. User-friendly, cost-effective, and without limitations.

Since the official Kickstarter API does not provide structured output of search results, you can get list of Kickstarter projects with this Kickstarter Scraper.

## Why scrape Kickstarter?
The [Kickstarter](https://www.kickstarter.com/) website is brimming with crowdfunding initiatives that are making a multitude of small-scale impacts on the world. Here's what you can achieve using the information about them:

- Monitor both active and upcoming [Kickstarter](https://www.kickstarter.com/) projects in your region or locality.
- Analyze which projects have a high likelihood of garnering support and estimate their potential for success.
- Enhance your crowdfunding campaign with real-time data.
- Track projects within the same category across the entire country.
- Validate your [Kickstarter](https://www.kickstarter.com/) investment analysis with the most recent data.
- Maintain records of past successful projects in your area.
- Continuously scout for leads on [Kickstarter](https://www.kickstarter.com/) by monitoring projects regularly.

## Features
- Exceptional speed and efficiency. Fetch Kickstarter Projects at a rate of **2400 items** per operation within just **3 minutes**.
- Explore projects using **any keyword**.
- Access data from the latest projects across any category, from **any city**, complete with **sorting** choices and **filters**. Unparalleled versatility.
- Search and extract data based on **funding goals**, **pledges**, **raised**, and more...
- **Custom dataset** feature. Assign names to your Kickstarter datasets for easy organization and monitoring of numerous runs.

## Bugs, fixes, updates, and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/epctex/kickstarter-scraper/issues).

## Input Parameters
- `query`: (Optional) (String) Keyword you want to search on Kickstarter.
- `startUrls`: (Optional) (Array) List of Kickstarter URLs. Project detail, search withy any sort or filter, Project Developer and Category URLs are supported.
- `category`: (Optional) (String) Kickstarter category you want to search your keywords in.
- `location`: (Optional) (String) Location of the Projects that will be retrieved.
- `status`: (Optional) (String) Status of the Projects that will be retrieved.
- `goal`: (Optional) (String) Goal of the Projects that will be retrieved.
- `pledged`: (Optional) (String) Amount of pledged for the Projects that will be retrieved.
- `raised`: (Optional) (String) Raised amount of the Projects that will be retrieved.
- `sort`: (Optional) (String) Sorting for the list.
- `maxResults`: (Optional) (Number) You can limit scraped items. This should be useful when you search through the big lists or search results.
- `proxyConfig`: (Required) (Proxy Object) Proxy configuration.
- `datasetName`: (Optional) (String) This is the custom dataset name that you want to save your rows into.
- `customMapFunction`: (Optional) (String) Function that takes each object's handle as an argument and returns the object with executing the function.

This solution requires the use of **Proxy servers**, either your own proxy servers or you can use [Apify Proxy](https://www.apify.com/docs/proxy).

### Tip

When you want to scrape over a specific list URL, just copy and paste the link as one of the **startUrl**.

If you would like to scrape only the first page of a list then put the link for the page and have the `endPage` as 1.

With the last approach that is explained above you can also fetch any interval of pages. If you provide the 5th page of a list and define the `endPage` parameter as 6 then you'll have the 5th and 6th pages only.

### Compute Unit Consumption

The actor is optimized to run blazing fast and scrape as many items as possible. Therefore, it forefronts all the detailed requests. If the actor doesn't block very often it'll scrape 100 listings in 2 minutes with ~0.03-0.05 compute units.

### Kickstarter Scraper Input example

```json
{
    "startUrls": [

    ],
    "includeReviews": false,
    "proxy": {
        "useApifyProxy": true
    },
    "endPage": 5,
    "maxItems": 100
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with a failure state and output an explanation of what is wrong.

## Kickstarter Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any language (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Kickstarter actor.

## Output
```json
{
	"url": "https://www.kickstarter.com/projects/1460250988/darkest-dungeon-by-red-hook-studios",
	"id": 1637457328,
	"photo": {
		"key": "assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg",
		"full": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=560&h=315&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=6da6937c57f82cb8ecadf3ee7585c4bf",
		"ed": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=352&h=198&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=0df2a471df5389efb646d4ab2802c488",
		"med": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=272&h=153&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=318772ec256642058bd1000164b7c029",
		"little": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=208&h=117&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=1ac714777905d3ae2852e1d3933d8edd",
		"small": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=160&h=90&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=d68eb4dbd06a41c11290e280439f334f",
		"thumb": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=48&h=27&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=f194adaa46ffe0ed8d5f8ba08a16b3cd",
		"1024x576": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=1024&h=576&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=e8624ff5e9dc61f08835e40aa634b793",
		"1536x864": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=1552&h=873&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=78034df38c3cc1928f2c8e3073cf6dc4"
	},
	"name": "Darkest Dungeon by Red Hook Studios",
	"blurb": "Darkest Dungeon is a challenging gothic roguelike RPG about the psychological stresses of adventuring. Descend at your peril!",
	"goal": 75000,
	"pledged": 313337.29,
	"state": "successful",
	"slug": "darkest-dungeon-by-red-hook-studios",
	"disable_communication": false,
	"country": "US",
	"country_displayable_name": "the United States",
	"currency": "USD",
	"currency_symbol": "$",
	"currency_trailing_code": true,
	"deadline": 1394780340,
	"state_changed_at": 1394780340,
	"created_at": 1387566705,
	"launched_at": 1392049183,
	"staff_pick": true,
	"is_starrable": false,
	"backers_count": 9639,
	"static_usd_rate": 1,
	"usd_pledged": "313337.29",
	"converted_pledged_amount": 313337,
	"fx_rate": 1,
	"usd_exchange_rate": 1,
	"current_currency": "USD",
	"usd_type": "domestic",
	"creator": {
		"id": 1460250988,
		"name": "Tyler Sigman",
		"is_registered": null,
		"is_email_verified": null,
		"chosen_currency": null,
		"is_superbacker": null,
		"avatar": {
			"thumb": "https://ksr-ugc.imgix.net/assets/006/967/403/ec78c1d4027518b1e9c4a26e987a3681_original.png?ixlib=rb-4.1.0&w=40&h=40&fit=crop&v=1461424629&auto=format&frame=1&q=92&s=707dbe0f4fb467810e50fef15dda3e9c",
			"small": "https://ksr-ugc.imgix.net/assets/006/967/403/ec78c1d4027518b1e9c4a26e987a3681_original.png?ixlib=rb-4.1.0&w=80&h=80&fit=crop&v=1461424629&auto=format&frame=1&q=92&s=77c3aeb6b149c3b8f91f33cff8f6e4d2",
			"medium": "https://ksr-ugc.imgix.net/assets/006/967/403/ec78c1d4027518b1e9c4a26e987a3681_original.png?ixlib=rb-4.1.0&w=160&h=160&fit=crop&v=1461424629&auto=format&frame=1&q=92&s=70723d292890977f2f3fc604e695f1a8"
		},
		"urls": {
			"web": {
				"user": "https://www.kickstarter.com/profile/1460250988"
			},
			"api": {
				"user": "https://api.kickstarter.com/v1/users/1460250988?signature=1701877526.25fd04f389ab206bd58132e8c7b24e2c2207b36b"
			}
		}
	},
	"location": {
		"id": 9807,
		"name": "Vancouver",
		"slug": "vancouver-ca",
		"short_name": "Vancouver, Canada",
		"displayable_name": "Vancouver, Canada",
		"localized_name": "Vancouver",
		"country": "CA",
		"state": "BC",
		"type": "Town",
		"is_root": false,
		"expanded_country": "Canada",
		"urls": {
			"web": {
				"discover": "https://www.kickstarter.com/discover/places/vancouver-ca",
				"location": "https://www.kickstarter.com/locations/vancouver-ca"
			},
			"api": {
				"nearby_projects": "https://api.kickstarter.com/v1/discover?signature=1701835626.29f1203a9fd242ae1642e87326f87c274abd94a8&woe_id=9807"
			}
		}
	},
	"category": {
		"id": 35,
		"name": "Video Games",
		"analytics_name": "Video Games",
		"slug": "games/video games",
		"position": 7,
		"parent_id": 12,
		"parent_name": "Games",
		"color": 51627,
		"urls": {
			"web": {
				"discover": "http://www.kickstarter.com/discover/categories/games/video%20games"
			}
		}
	},
	"video": {
		"id": 341397,
		"status": "successful",
		"hls": null,
		"high": "https://v2.kickstarter.com/1701781589-O7K1EUa334JswxxLwE2K3tSxkjciwfkbDWHfsszUFFs%3D/projects/803257/video-341397-h264_high.mp4",
		"base": "https://v2.kickstarter.com/1701781589-O7K1EUa334JswxxLwE2K3tSxkjciwfkbDWHfsszUFFs%3D/projects/803257/video-341397-h264_base.mp4",
		"width": 640,
		"height": 350,
		"frame": "https://d15chbti7ht62o.cloudfront.net/projects/803257/video-341397-h264_high.jpg?2014"
	},
	"profile": {
		"id": 821784,
		"project_id": 821784,
		"state": "active",
		"state_changed_at": 1426460821,
		"name": "Darkest Dungeon by Red Hook Studios",
		"blurb": "Darkest Dungeon is a challenging gothic roguelike RPG about the psychological stresses of adventuring. Descend at your peril!",
		"background_color": "",
		"text_color": "",
		"link_background_color": "",
		"link_text_color": "",
		"link_text": "Buy now!",
		"link_url": "http://store.steampowered.com/app/262060/",
		"show_feature_image": false,
		"background_image_opacity": 0.8,
		"should_show_feature_image_section": true,
		"feature_image_attributes": {
			"image_urls": {
				"default": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=1552&h=873&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=78034df38c3cc1928f2c8e3073cf6dc4",
				"baseball_card": "https://ksr-ugc.imgix.net/assets/011/625/166/31cd062c4f7bf199c14723ea78e338f9_original.jpg?ixlib=rb-4.1.0&crop=faces&w=560&h=315&fit=crop&v=1463685688&auto=format&frame=1&q=92&s=6da6937c57f82cb8ecadf3ee7585c4bf"
			}
		}
	},
	"spotlight": true,
	"urls": {
		"web": {
			"project": "https://www.kickstarter.com/projects/1460250988/darkest-dungeon-by-red-hook-studios",
			"rewards": "https://www.kickstarter.com/projects/1460250988/darkest-dungeon-by-red-hook-studios/rewards",
			"project_short": "http://kck.st/1gmsiey",
			"updates": "https://www.kickstarter.com/projects/1460250988/darkest-dungeon-by-red-hook-studios/posts"
		},
		"api": {
			"project": "https://api.kickstarter.com/v1/projects/1637457328?signature=1701877526.b349e69d1787a234c0f0017940a47942f5db2d85",
			"comments": "https://api.kickstarter.com/v1/projects/1637457328/comments?signature=1701877526.532b17d386bb2d28fa87ad09c4c13dcfcb749745",
			"updates": "https://api.kickstarter.com/v1/projects/1637457328/updates?signature=1701877526.5fc5e473f9fa34c33a347aa7e576eaabf7a83145"
		}
	},
	"updated_at": 1555423491,
	"successful_at": 1394780340,
	"comments_count": 7432,
	"updates_count": 52,
	"tags": [
		"Monsters",
		"RPGs"
	],
	"rewards": [
		{
			"id": 0,
			"description": "No Reward",
			"minimum": 1,
			"reward": "No Reward",
			"converted_minimum": 1
		},
		{
			"id": 2357683,
			"minimum": 15,
			"converted_minimum": 15,
			"reward": "NOMAD\\n\\nTHE GAME\\n\\nDigital downloadable copy of Darkest Dungeon on Steam when it releases. (PC / Mac) ● (Approximately €11 / £9)",
			"description": "NOMAD\\n\\nTHE GAME\\n\\nDigital downloadable copy of Darkest Dungeon on Steam when it releases. (PC / Mac) ● (Approximately €11 / £9)",
			"title_for_backing_tier": "$15 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 3186,
			"updated_at": 1700592473,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2357683?signature=1701877526.66d91fe5ed4036f247354f1dc8fbb24f57a876f2"
				}
			}
		},
		{
			"id": 2264018,
			"minimum": 20,
			"converted_minimum": 20,
			"reward": "WANDERER\\n\\nTHE GAME + EARLY ACCESS + DEVELOPMENT POLLS\\n\\nGet EARLY ACCESS to the game when it goes live on Steam later this year. You will be amongst the first to play the game and access new features and content right as they are implemented! ● Plus, you will see concept art and be given the chance to take part in polls during development to help choose some character classes, monsters, and environments that will get put into the game. ● (Approximately €15 / £12)",
			"description": "WANDERER\\n\\nTHE GAME + EARLY ACCESS + DEVELOPMENT POLLS\\n\\nGet EARLY ACCESS to the game when it goes live on Steam later this year. You will be amongst the first to play the game and access new features and content right as they are implemented! ● Plus, you will see concept art and be given the chance to take part in polls during development to help choose some character classes, monsters, and environments that will get put into the game. ● (Approximately €15 / £12)",
			"title_for_backing_tier": "$20 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 2526,
			"updated_at": 1698083502,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264018?signature=1701877526.899be1da6133f574b4fd714d2c1a9aa6589fba50"
				}
			}
		},
		{
			"id": 2264043,
			"minimum": 29,
			"converted_minimum": 29,
			"reward": "SEEKER\\n\\n+PDF ADVENTURING MANUAL + DIGITAL ESTATE MAP + EXCLUSIVE WALLPAPER PACK + CREDIT\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Really excited about Darkest Dungeon? Back us at this level and you will be handsomely rewarded with a PDF Adventuring Manual filled with lore, tips, and sketches to assist you in planning your quests. ● Also, get a digital map of your inherited Estate, complete with scrawled hints which will help you in your early adventurers. ● You'll also get an exclusive BACKERS ONLY digital wallpaper pack to adorn your favorite computer(s) ● Finally, in recognition of your pledging at this level and helping Darkest Dungeon get made, you'll receive a \"Founders\" CREDIT in the game! ● (Approximately €21 / £18)",
			"description": "SEEKER\\n\\n+PDF ADVENTURING MANUAL + DIGITAL ESTATE MAP + EXCLUSIVE WALLPAPER PACK + CREDIT\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Really excited about Darkest Dungeon? Back us at this level and you will be handsomely rewarded with a PDF Adventuring Manual filled with lore, tips, and sketches to assist you in planning your quests. ● Also, get a digital map of your inherited Estate, complete with scrawled hints which will help you in your early adventurers. ● You'll also get an exclusive BACKERS ONLY digital wallpaper pack to adorn your favorite computer(s) ● Finally, in recognition of your pledging at this level and helping Darkest Dungeon get made, you'll receive a \"Founders\" CREDIT in the game! ● (Approximately €21 / £18)",
			"title_for_backing_tier": "$29 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 932,
			"updated_at": 1700945905,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264043?signature=1701877526.e0abf856d8ecc44aa7db6902095199a67d9c34f8"
				}
			}
		},
		{
			"id": 2264071,
			"minimum": 49,
			"converted_minimum": 49,
			"reward": "ADVENTURER\\n\\nDELUXE DIGITAL EDITION: EXCLUSIVE CHARACTER CLASS + PDF ART BOOK + ORIGINAL SOUNDTRACK BY STUART CHATWOOD + ADVENTURER CREDIT\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Exclusive playable Backers Only character class which will be voted upon by backers (you!) after the campaign closes. ● Feast your eyes upon a digital ART BOOK containing extensive concept work and finished illustrations from Darkest Dungeons' artists! ● Treat your ears to a digital downloadable copy of the Darkest Dungeon Original Soundtrack by Stuart Chatwood. Stuart has composed music for 8 Prince of Persia games on top of his work in a platinum-selling rock band. ● AND, for helping us at this deluxe level, earn eternal recognition with an ADVENTURER credit in the game! ● (Approximately €36 / £29)",
			"description": "ADVENTURER\\n\\nDELUXE DIGITAL EDITION: EXCLUSIVE CHARACTER CLASS + PDF ART BOOK + ORIGINAL SOUNDTRACK BY STUART CHATWOOD + ADVENTURER CREDIT\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Exclusive playable Backers Only character class which will be voted upon by backers (you!) after the campaign closes. ● Feast your eyes upon a digital ART BOOK containing extensive concept work and finished illustrations from Darkest Dungeons' artists! ● Treat your ears to a digital downloadable copy of the Darkest Dungeon Original Soundtrack by Stuart Chatwood. Stuart has composed music for 8 Prince of Persia games on top of his work in a platinum-selling rock band. ● AND, for helping us at this deluxe level, earn eternal recognition with an ADVENTURER credit in the game! ● (Approximately €36 / £29)",
			"title_for_backing_tier": "$49 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 1551,
			"updated_at": 1700594500,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264071?signature=1701877526.a21dbd63697ec84f5e9f48f604c13a4909ef5524"
				}
			}
		},
		{
			"id": 2266427,
			"minimum": 74,
			"converted_minimum": 74,
			"reward": "ARTIST\\n\\n+PRINTED ART BOOK (DISCOUNTED)\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Beautiful printed copy of the Darkest Dungeon Art Book to handle and gaze at. Save $ versus Adding On separately. ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €69 / £57 including shipping.)",
			"description": "ARTIST\\n\\n+PRINTED ART BOOK (DISCOUNTED)\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Beautiful printed copy of the Darkest Dungeon Art Book to handle and gaze at. Save $ versus Adding On separately. ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €69 / £57 including shipping.)",
			"title_for_backing_tier": "$74 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 184,
			"updated_at": 1668799093,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2266427?signature=1701877526.c69c101ed34e2de5179d187e1d1e3b602df4d337"
				}
			}
		},
		{
			"id": 2273192,
			"minimum": 95,
			"converted_minimum": 95,
			"reward": "DIGITAL PATRON\\n\\nALL DIGITAL! (NO PHYSICAL ITEMS) GREAT FOR INTERNATIONAL SUPPORTERS!\\n\\nWant the most Darkest Dungeon you can get, including Personalizing a Hero and Designing an Item, but don't want to deal with physical items and shipping costs? Back us at this level and get some  of the rewards from higher tiers. ● INCLUDES ALL REWARDS FROM ADVENTURER TIER (DIGITAL DELUXE EDITION) ● Plus PDF DIORAMA (print your own diorama!) ● Plus PERSONALIZE A HERO (see \"Patron\" tier) ● Plus DESIGN AN IN GAME EQUIPPABLE ITEM (see \"Grand Patron\" tier) ● And get listed as a \"PATRON\" in the credits! ● (Approximately €69 / £57 - no shipping required.)",
			"description": "DIGITAL PATRON\\n\\nALL DIGITAL! (NO PHYSICAL ITEMS) GREAT FOR INTERNATIONAL SUPPORTERS!\\n\\nWant the most Darkest Dungeon you can get, including Personalizing a Hero and Designing an Item, but don't want to deal with physical items and shipping costs? Back us at this level and get some  of the rewards from higher tiers. ● INCLUDES ALL REWARDS FROM ADVENTURER TIER (DIGITAL DELUXE EDITION) ● Plus PDF DIORAMA (print your own diorama!) ● Plus PERSONALIZE A HERO (see \"Patron\" tier) ● Plus DESIGN AN IN GAME EQUIPPABLE ITEM (see \"Grand Patron\" tier) ● And get listed as a \"PATRON\" in the credits! ● (Approximately €69 / £57 - no shipping required.)",
			"title_for_backing_tier": "$95 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 212,
			"updated_at": 1686842249,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2273192?signature=1701877526.b6a2e533ad978e5d93fc8f3084eb6f3f0e8d20fd"
				}
			}
		},
		{
			"id": 2264149,
			"minimum": 99,
			"converted_minimum": 99,
			"reward": "PATRON\\n\\n+PAPER DIORAMA + PERSONALIZE A HERO + PATRON CREDIT\\n\\nINCLUDES ALL [ARTIST] REWARDS (Digital Deluxe Pack + Printed Art Book) PLUS: ● Make your own Darkest Dungeon diorama! You get a set of character, hallway, and monster sheets. Just cut and assemble for a desktop dungeon delving display! ● PLUS, get involved in game creation by personalizing a recruitable hero for the game. After the campaign, we'll send you a survey where you can select a name (subject to style approval to fit the game), character class, and some starting traits. This character can show up as a recruit in town, for any players to hire. ● Get listed as a PATRON in the credits and know you were a huge part of making DD happen. ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €87/ £73 including shipping.)",
			"description": "PATRON\\n\\n+PAPER DIORAMA + PERSONALIZE A HERO + PATRON CREDIT\\n\\nINCLUDES ALL [ARTIST] REWARDS (Digital Deluxe Pack + Printed Art Book) PLUS: ● Make your own Darkest Dungeon diorama! You get a set of character, hallway, and monster sheets. Just cut and assemble for a desktop dungeon delving display! ● PLUS, get involved in game creation by personalizing a recruitable hero for the game. After the campaign, we'll send you a survey where you can select a name (subject to style approval to fit the game), character class, and some starting traits. This character can show up as a recruit in town, for any players to hire. ● Get listed as a PATRON in the credits and know you were a huge part of making DD happen. ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €87/ £73 including shipping.)",
			"title_for_backing_tier": "$99 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 94,
			"updated_at": 1668818956,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264149?signature=1701877526.5d4757e07e798f95344047a86f667f85ebbf39c1"
				}
			}
		},
		{
			"id": 2264150,
			"minimum": 149,
			"converted_minimum": 149,
			"reward": "GRAND PATRON\\n\\n+SIGNED ART PRINT + DESIGN AN IN-GAME EQUPPABLE ITEM\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Get a beautiful signed numbered limited edition 18\" x 24\" print by Darkest Dungeon artist Chris Bourassa. ● Design an in-game item that is equippable by heroes: during development, we will send you a survey where you can assemble an item by choosing a form, giving it powers, and naming it (subject to thematic approval). Your item becomes loot in the game! ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €123 / £103 including shipping.)",
			"description": "GRAND PATRON\\n\\n+SIGNED ART PRINT + DESIGN AN IN-GAME EQUPPABLE ITEM\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Get a beautiful signed numbered limited edition 18\" x 24\" print by Darkest Dungeon artist Chris Bourassa. ● Design an in-game item that is equippable by heroes: during development, we will send you a survey where you can assemble an item by choosing a form, giving it powers, and naming it (subject to thematic approval). Your item becomes loot in the game! ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €123 / £103 including shipping.)",
			"title_for_backing_tier": "$149 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"available": true,
			"backers_count": 107,
			"updated_at": 1681506672,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264150?signature=1701877526.cd4d58b5d963440062d8e8999fef460d7ecf8f73"
				}
			}
		},
		{
			"id": 2273152,
			"minimum": 2500,
			"converted_minimum": 2500,
			"reward": "BARON\\n\\n+DESIGN A MONSTER!\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Work with our design team to design a monster that will appear in the game! We'll collaborate to pick a monster type, name, and combat abilities. ● Then, receive a print of the monster, signed by the dev team. ● And you'll be credited under \"ADDITIONAL MONSTER DESIGN\" in the credits! ● Worldwide shipping included. ● (Approximately €1825 / £1500)",
			"description": "BARON\\n\\n+DESIGN A MONSTER!\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Work with our design team to design a monster that will appear in the game! We'll collaborate to pick a monster type, name, and combat abilities. ● Then, receive a print of the monster, signed by the dev team. ● And you'll be credited under \"ADDITIONAL MONSTER DESIGN\" in the credits! ● Worldwide shipping included. ● (Approximately €1825 / £1500)",
			"limit": 5,
			"title_for_backing_tier": "$2,500 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 4,
			"available": true,
			"backers_count": 1,
			"updated_at": 1486113694,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2273152?signature=1701877526.1fbb39b80f9f68fc30331a1ea7c196ff4be3ae61"
				}
			}
		},
		{
			"id": 2273172,
			"minimum": 24,
			"converted_minimum": 24,
			"reward": "EARLY BIRD - SEEKER\\n\\nYou get all rewards of the $29 tier below! You save $$ by jumping in early! ● (Approximately €18 / £15)",
			"description": "EARLY BIRD - SEEKER\\n\\nYou get all rewards of the $29 tier below! You save $$ by jumping in early! ● (Approximately €18 / £15)",
			"limit": 250,
			"title_for_backing_tier": "$24 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 250,
			"updated_at": 1647967050,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2273172?signature=1701877526.5ff1856c4080c78aeac214d4962a3530e15aa666"
				}
			}
		},
		{
			"id": 2273178,
			"minimum": 40,
			"converted_minimum": 40,
			"reward": "EARLY BIRD - ADVENTURER\\n\\nAll rewards of the $49 tier below. Save $$ by jumping in early! (Approximately €29 / £24)",
			"description": "EARLY BIRD - ADVENTURER\\n\\nAll rewards of the $49 tier below. Save $$ by jumping in early! (Approximately €29 / £24)",
			"limit": 225,
			"title_for_backing_tier": "$40 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 225,
			"updated_at": 1690714840,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2273178?signature=1701877526.a430f6a7a1a94cc8751501689ba5d8535e4c5be6"
				}
			}
		},
		{
			"id": 2367081,
			"minimum": 44,
			"converted_minimum": 44,
			"reward": "EARLY BIRD ROUND 2 - ADVENTURER\\n\\nDue to overwhelming demand, we'd decided to open some more Early Bird slots for ADVENTURER. This includes all rewards of the $49 tier below. Save $$ by jumping in early! (Approximately €32 / £27)",
			"description": "EARLY BIRD ROUND 2 - ADVENTURER\\n\\nDue to overwhelming demand, we'd decided to open some more Early Bird slots for ADVENTURER. This includes all rewards of the $49 tier below. Save $$ by jumping in early! (Approximately €32 / £27)",
			"limit": 250,
			"title_for_backing_tier": "$44 reward",
			"shipping_enabled": false,
			"shipping_type": "no_shipping",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 250,
			"updated_at": 1701700729,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2367081?signature=1701877526.d4e6a591d08e581a5a5ab0d59c6de5dfe356bdf4"
				}
			}
		},
		{
			"id": 2264151,
			"minimum": 249,
			"converted_minimum": 249,
			"reward": "HEIR\\n\\n+YOUR FACE DRAWN IN THE DARKEST DUNGEON STYLE + THE DARKEST DUNGEON NARRATOR READS A LINE FOR YOU!\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Get your face drawn in the Darkest Dungeon style similar to what you see under the TEAM section...a great avatar for Twitter, Facebook, etc.! ● ALSO, the velvet-voiced baritone Narrator of Darkest Dungeon, Wayne June, will read a line of your choice for you and you will get the digital recording to use as you wish. (Lines are subject to decency/political restrictions--we'll work with you to make sure it's acceptable.) ● Get credited as a HEIR in the game WITH YOUR AVATAR PICTURE shown! ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €196 / £164 including shipping)",
			"description": "HEIR\\n\\n+YOUR FACE DRAWN IN THE DARKEST DUNGEON STYLE + THE DARKEST DUNGEON NARRATOR READS A LINE FOR YOU!\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Get your face drawn in the Darkest Dungeon style similar to what you see under the TEAM section...a great avatar for Twitter, Facebook, etc.! ● ALSO, the velvet-voiced baritone Narrator of Darkest Dungeon, Wayne June, will read a line of your choice for you and you will get the digital recording to use as you wish. (Lines are subject to decency/political restrictions--we'll work with you to make sure it's acceptable.) ● Get credited as a HEIR in the game WITH YOUR AVATAR PICTURE shown! ● Shipping to US and Canada included. Please add $20 for other countries. ● (Approximately €196 / £164 including shipping)",
			"limit": 20,
			"title_for_backing_tier": "$249 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 20,
			"updated_at": 1600883089,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264151?signature=1701877526.dc9d926fb2e86786fe919573d8ae18d23094c66f"
				}
			}
		},
		{
			"id": 2264169,
			"minimum": 499,
			"converted_minimum": 499,
			"reward": "NOBLE HEIR\\n\\n+JOURNAL OF YOUR EXPEDITION AND DOOM\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Be immortalized in Darkest Dungeon! We will work with you to come up with a simple story about your fictional adventure down into the dungeons in which you met an untimely end. While adventuring, players can happen across journal pages which tell of your fate. ● Finally, be listed as \"NOBLE HEIR\" in the credits. ● Worldwide shipping included. ● (Approximately €364 / £299)",
			"description": "NOBLE HEIR\\n\\n+JOURNAL OF YOUR EXPEDITION AND DOOM\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Be immortalized in Darkest Dungeon! We will work with you to come up with a simple story about your fictional adventure down into the dungeons in which you met an untimely end. While adventuring, players can happen across journal pages which tell of your fate. ● Finally, be listed as \"NOBLE HEIR\" in the credits. ● Worldwide shipping included. ● (Approximately €364 / £299)",
			"limit": 5,
			"title_for_backing_tier": "$499 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 5,
			"updated_at": 1533051734,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264169?signature=1701877526.e64424cc6dbef6ebf78fdddec2da36a176fac962"
				}
			}
		},
		{
			"id": 2264168,
			"minimum": 999,
			"converted_minimum": 999,
			"reward": "HEIR APPARENT\\n\\n+EXCLUSIVE 1 of 1 SIGNED CLASS DRAWING\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Work with Darkest Dungeon artist Chris Bourassa to select your favorite hero class and discuss a pose. Chris will paint this pose and we will print a SINGLE COPY ONLY of this print, sign it, and ship it to you. ● You will also get the digital wallpaper version to share as you decide. ● Finally, be listed as \"HEIR APPARENT\" in the credits. ● Worldwide shipping included. ● (Approximately €729 / £599)",
			"description": "HEIR APPARENT\\n\\n+EXCLUSIVE 1 of 1 SIGNED CLASS DRAWING\\n\\nINCLUDES ALL PREVIOUS REWARDS ● Work with Darkest Dungeon artist Chris Bourassa to select your favorite hero class and discuss a pose. Chris will paint this pose and we will print a SINGLE COPY ONLY of this print, sign it, and ship it to you. ● You will also get the digital wallpaper version to share as you decide. ● Finally, be listed as \"HEIR APPARENT\" in the credits. ● Worldwide shipping included. ● (Approximately €729 / £599)",
			"limit": 5,
			"title_for_backing_tier": "$999 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 5,
			"updated_at": 1486163259,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2264168?signature=1701877526.f9dcc571d434576f6081c9c8a778efaa32be5de4"
				}
			}
		},
		{
			"id": 2281998,
			"minimum": 5000,
			"converted_minimum": 5000,
			"reward": "LORD\\n\\n+DESIGN A CHARACTER CLASS\\n\\nINCLUDES ALL PREVIOUS REWARDS ● You will have an effect in shaping the game for every player. Work with our design and art team to create and design a character class that players can recruit and use in their party. We'll collaborate to create the visual and gameplay elements of the class, including combat abilities, camping abilities, and weapons and armor. ● Receive credit in the game as \"ADDITIONAL CLASS DESIGN.\" ● We'll also give you a signed 1/1 print of the class. ● Worldwide shipping included. ● (Approximately €3650 / £3000)",
			"description": "LORD\\n\\n+DESIGN A CHARACTER CLASS\\n\\nINCLUDES ALL PREVIOUS REWARDS ● You will have an effect in shaping the game for every player. Work with our design and art team to create and design a character class that players can recruit and use in their party. We'll collaborate to create the visual and gameplay elements of the class, including combat abilities, camping abilities, and weapons and armor. ● Receive credit in the game as \"ADDITIONAL CLASS DESIGN.\" ● We'll also give you a signed 1/1 print of the class. ● Worldwide shipping included. ● (Approximately €3650 / £3000)",
			"limit": 1,
			"title_for_backing_tier": "$5,000 reward",
			"shipping_enabled": true,
			"shipping_preference": "unrestricted",
			"shipping_summary": "Anywhere in the world",
			"shipping_type": "anywhere",
			"estimated_delivery_on": 1420070400,
			"has_addons": false,
			"reward_type": "base",
			"project_id": 1637457328,
			"remaining": 0,
			"available": false,
			"backers_count": 1,
			"updated_at": 1486112509,
			"rewards_items": [],
			"urls": {
				"api": {
					"reward": "https://api.kickstarter.com/v1/projects/1637457328/rewards/2281998?signature=1701877526.877f82629611dc36416d05c2915cd74f77d058cf"
				}
			}
		}
	],
	"add_ons": [],
	"items": [],
	"prelaunch_activated": false,
	"display_prelaunch": false,
	"available_card_types": [
		"VISA",
		"MASTERCARD",
		"AMEX",
		"DISCOVER",
		"JCB",
		"DINERS",
		"UNION_PAY"
	],
	"supports_addons": false,
	"addons_pledge_url": "https://www.kickstarter.com/projects/1460250988/darkest-dungeon-by-red-hook-studios/pledge/new?clicked_reward=false"
}
```

## Contact
Please visit us through [epctex.com](https://epctex.com) to see all the products that are available for you. If you are looking for any custom integration or so, please reach out to us through the chat box in [epctex.com](https://epctex.com). In need of support? [devops@epctex.com](mailto:devops@epctex.com) is at your service.

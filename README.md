# Exporting Google/Meta Ads Data (Prototype)

This script was built to export Meta/Google Ads data to Google Sheets on a recurring basis for use in a dashboard.

In order to bypass limits around the amount of data that can be processed by the Facebook Marketing API and [Google App Script's
6 minute runtime maximum](https://developers.google.com/apps-script/guides/services/quotas), the script makes [asynchronous requests](https://developers.facebook.com/docs/marketing-api/asyncrequests/) to the Facebook Marketing API.

## How Facebook Helps Advertisers Target You

If you use Facebook, it probably comes as no surprise that Facebook collects a lot of information about you. This includes information you’ve shared about yourself as well as information about your activity on Facebook and other websites — things like check-ins, searches, and status updates.

What you may not know is that even when you haven’t shared interests, Facebook makes guesses about your views and preferences based on your activity. This is also used to target you, but it’s not as easy for you to see this. When you use Ad Analysis for Facebook, you can see what Facebook knows about you and how that affects the advertising you see. You can also compare a wide range of targets shared as a public data set by thousands of other Facebook users.

## Peek Outside Your Filter Bubble

Seeing how and why you’re targeted for advertising is one way to examine how Facebook shapes the content you’re likely to see and how that might influence your opinions and beliefs. But what about the advertising you don’t see?

Facebook maintains its own Ad Archive, which offers Facebook users a simple keyword search tool to view ads related to politics or issues of national importance.

The Ad Archive is useful if you know what you are looking for, but may not help you if you are trying to answer questions like “Who is spending the most money on political ads in my state?” or “If I am a Millennial, do I see different ads than Baby Boomers?” With Ad Analysis for Facebook, you can view top advertisers; filter advertisers by state, gender, and age; and link to advertisers’ ads in the Facebook Ad Archive.

## Setup

You'll first want to create a [Facebook App](https://developers.facebook.com/apps/) and add the Marketing API product to it.

You can then get a short-lived user access token through the [Graph API Explorer](https://developers.facebook.com/tools/explorer/).

If you're going to be using this script on an ongoing basis, I recommend you exchange your short-lived token for a long-lived one using [this method](https://developers.facebook.com/docs/facebook-login/access-tokens/refreshing#exchanging-short-lived-tokens-for-long-lived-tokens).

Once you've entered your credentials as well as all parameters, you'll want to make sure that [request-facebook-report.js](https://github.com/fredericharnois/facebook-ads-reporting-google-apps-script/blob/master/request-facebook-report.js) is scheduled to run before [get-facebook-report.js](https://github.com/fredericharnois/facebook-ads-reporting-google-apps-script/blob/master/get-facebook-report.js).

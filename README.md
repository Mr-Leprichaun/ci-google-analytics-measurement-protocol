## ci-google-analytics-measurement-protocol
#Google Analytics Measurement Protocol Library for CodeIgniter


This library allows you to send custom events and pageviews to Google Analytics Goals with a single function call.

Installation:

1. Put `Google_analytics.php` into your `application/libraries` folder
2. [Optional] Change `$this->user_agent = 'CI-GA-MP/1.0 '.site_url();` to any other user-agent you'd like your site to be

Usage:

1. Load the library
  1. in `system/config/autoload.php`, add `'google_analytics'` to the `$autoload['libraries']` array, or
  2. in the file that you'd like to use this class, add `$this->load->library('google_analytics');`
2. Call the function to either send an 'event' or a 'pageview' to Google Analytics:

For an event:
```PHP
$this->google_analytics->send_google_analytics_event('UA-XXXXXXXX-X', '{CATEGORY}', '{ACTION}', '[{LABEL}]', '[{VALUE}]');
```
LABEL and VALUE are optional
    
For a pageview
```PHP
$this->google_analytics->send_google_analytics_pageview('UA-XXXXXXXX-X', '{HOST}', '{PATH}', '{TITLE}');
```    
All parameters are required

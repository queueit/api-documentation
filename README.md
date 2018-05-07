DisplayName: 
The name of the event

RedirectUrl: 
This is the default target URL to redirect to after leaving the queue. Required valid URL

Description: 
Description of the event

TimeZone: 
Time zone of the event. Required name of time zone from available options found here: http://support.microsoft.com/kb/973627

TimeZonePostfix: 
Text to be displayed after a time value (e.g. event start time)

PreQueueStartTime: 
Pre queue start time of the event. Required date string expressed in either Unix Time (ex. \/Date(1310669017000)\/) or ISO-8601 (ex. 2015-01-06T19:34:58.8082444Z) format

EventStartTime: 
Queue start time of the event. Required date string expressed in either Unix Time (ex. \/Date(1310669017000)\/) or ISO-8601 (ex. 2015-01-06T19:34:58.8082444Z) format

EventEndTime: 
End time of the event. Required date string expressed in either Unix Time (ex. \/Date(1310669017000)\/) or ISO-8601 (ex. 2015-01-06T19:34:58.8082444Z) format

EventCulture: 
Culture/language of the event. Optional name of language culture from available options found here: http://msdn.microsoft.com/en-us/library/ee825488%28v=cs.20%29.aspx. If not specified default value will be en-US

MaxNoOfRedirectsPrQueueId: 
The maximum allowed number of redirects pr. queue number/id. Required number between 1 and 20 (both included)

QueueNumberValidityInMinutes: 
The validity/lifetime minutes of any queue number issued. Required number between 5 and 60 (both included)

AfterEventLogic: 
The post queue setting, e.g. what happens when the event is over/ended. Required enum value from one of the following: KeepUsersOnAfterEventPage | RedirectUsersToSpecialPage | RedirectUsersToTargetPage

AfterEventRedirectPage: 
If AfterEventLogic is set to RedirectUsersToSpecialPage you need to specify the URL of this page. Optional valid Absolute URL

AfterEventEndUserRedirectsEnabled: 
Whether or not end users should be allowed to complete their queue journey even after event end time occurs. Optional True or False value

UseSSL: 
SSL/HTTPS security setting of the event. Required enum value from one of the following: False | True | Auto

JavaScriptSupportEnabled: 
Optional True or False value, whether or not javascript client support should be enabled. If not specified False will be used. To enable SimpleLink behavior, set this to False and 'KnowUserSecurity' to 'None'

TargetUrlSupportEnabled: 
Whether or not target URL parameter should be supported. Optional True or False value

SafetyNetMode: 
Safetynet setting for the event. Required enum value from one of the following: Disabled | ProtectionAndQueueSequence | RelaxedProtectionAndQueueSequence | OutputThroughput. Compared to our Go-platform, 'Disabled' equals 'Always - queue mode', 'ProtectionAndQueueSequence' equals 'SafetyNet (Burst protection), only visible above threshhold', 'RelaxedProtectionAndQueueSequence' equals 'SafetyNet (Normal), only visible above threshhold', and 'OutputThroughput' equals 'SafetyNet (Mixed-Mode)'

KnowUserSecurity: 
Known user security setting if you are using known user implementation e.g. not enqueing via javascript. Required enum value from one of the following: None | Simple | HMACSHA256 | SimpleWithTimestamp | MD5Hash | KnownUserV3. Compared to our Go-platform, 'Simple' equals 'Simple hash value', 'HMACSHA256' equals 'Hash-based Message Authentication Code', 'SimpleWithTimestamp' equals 'Simple hash value based on timestamp', 'MD5Hash' equals 'QueueIT Security (MD5 hash value)', and 'KnownUserV3' equals 'QueueIT Security V3'. To enable SimpleLink behavior, set this to 'None' and 'JavaScriptSupportEnabled' to False

KnowUserSecretKey: 
Optional event specific secret key for known user security. If not specified the default known user secret key will be used

CustomLayout: 
Required name of your own custom layout or one of our default layouts being 'Default layout by Queue-it', 'Christmas Layout by Queue-it', or 'Ticket Layout by Queue-it'. Optional text with a max length of 256 characters

TargetUrlValidationRegex: 
The pattern is used for regular expression validation of the target URL parameter. Optional regular expression pattern

DomainAlias: 
Optional event specific domain alias (CNAME). If not specified the default (q.queue-it.net) will be used

AllowedCustomLayouts: 
Optional list of names of the event specific layouts allowed. Optional string array of maximum 30 elements

BrowserCultureEnabled: 
Whether or not language should be detected from browser settings. Optional True or False value

IdleQueueLogic: 
The idle setting, e.g. what happens before pre queue start. Required enum value from one of the following: UseBeforePage | RedirectUsersToSpecialPage | RedirectUsersToTargetPage

IdleQueueRedirectPage: 
If IdleQueueLogic is set to RedirectUsersToSpecialPage you need to specify the URL of this page. Optional valid Absolute URL

CaptchaType: 
Whether or not captcha fraud protection should be enabled. Required enum value from one of the following: None | Recaptcha | RecaptchaInvisible | BotDetect

IsTest: 
Whether or not this is a test event. Optional True or False value

RequireKey: 
Fraud protection setting if you require user input as a part of your queue flow. Required enum value from one of the following: NoKey | RequireKey | RequireUniqueKey. Can be combined with captcha, where captcha will be displayed first.

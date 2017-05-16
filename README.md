# API [![Build Status](https://api.travis-ci.org/PagePortrait/API.svg?branch=master)](http://travis-ci.org/PagePortrait/API)

### Common

**Parameters**
```
url - String. The webpage URL.
key - String. The request authentication key.
jsonp - String. Optional callback function name.
```


### Alexa API

**URL**
```
https://api.pageportrait.com/v1/alexa
```

**Response**
```javascript
{
  "country": {"name": "Ukraine", "rank": "22867"},
  "global": {"rank": "3084726", "delta": "-6547191"}
}
```


### Audience API

**URL**
```
https://api.pageportrait.com/v1/audience
```

**Response**
```javascript
{
  "demographics": {
    "gender": {"male": 89, "female": 0},
    "education": {"college": 0, "no-college": 0, "graduate-school": 69, "some-college": 0},
    "location": {"home": 32, "school": 0, "work": 66}
  },
  "engagement": {
    "search-visits": {"value": "11.10", "delta": "-17"},
    "pageviews": {"value": "4.40", "delta": "30"},
    "bounce-rate": {"value": "32.90", "delta": "-13"},
    "time-on-site": {"value": "7:55", "delta": "62"}
  }
}
```


### AWIS API (Alexa Web Information Service)

**URL**
```
https://api.pageportrait.com/v1/awis
```

**Response**
```javascript
{
  "engagement": {"pageviews": {"value": 1.01, "delta": -1.94}},
  "links": "18796",
  "country": {"rank": 4912.0, "name": "VN"},
  "global": {"delta": -10865.0, "rank": 8336.0},
  "geo": [["IN", 2.6, 9628.0, 2.6], ["UA", 2.3, 1188.0, 2.3], ["DE", 3.3, 5763.0, 3.3]],
  "speed": {"percentile": "88", "loadtime": "750"}
}
```


### Content API (Proxy)

**URL**
```
https://api.pageportrait.com/v1/content
```

**Response**
```javascript
{
  "content": "<!DOCTYPE html><html>...</html>",
  "status": 200,
  "headers": { ... }
}
```


### Google API

**URL**
```
https://api.pageportrait.com/v1/google
```

**Response**
```javascript
{
  "pagerank": "6",
  "safebrowsing": "ok",
  "mobile": {
    "screenshot": {
      "width": 375,
      "page_rect": {"width": 375, "top": 0, "height": 667, "left": 0},
      "data": "BASE64",
      "mime_type": "image/jpeg",
      "height": 667
    },
    "ruleGroups": {
      "USABILITY": {"score": 100, "pass": true}
    }
  },
  "pagespeed": {
    "screenshot": {
      "width": 320,
      "page_rect": {"width": 1024, "top": 0, "height": 768, "left": 0},
      "data": "BASE64",
      "mime_type": "image/jpeg",
      "height": 240
    },
    "title": "\u042f\u043d\u0434\u0435\u043a\u0441",
    "ruleGroups": {
      "SPEED": {"score": 87}
    },
    "version": {"major": 1, "minor": 15},
    "responseCode": 200,
    "pageStats": {
      "otherResponseBytes": "2373",
      "totalRequestBytes": "2736",
      "numberCssResources": 1,
      "javascriptResponseBytes": "328534",
      "cssResponseBytes": "30633",
      "imageResponseBytes": "8316",
      "numberResources": 16,
      "numberHosts": 6,
      "numberStaticResources": 8,
      "htmlResponseBytes": "11002",
      "numberJsResources": 5
    }
  }
}
```


### Http Data API

**URL**
```
https://api.pageportrait.com/v1/httpdata
```

**Response**
```javascript
{
  "accept-ranges": "bytes",
  "content-length": "2038",
  "content-language": "en-US",
  "content-encoding": "gzip",
  "content-type": "text/html; charset=UTF-8",
  "cache-control": "max-age=86400, public",
  "cache-public": true,
  "server": "Apache/2.2.22 (Debian)",
  "server-name": "Apache",
  "server-version": "2.2.22",
  "server-signature": true,
  "vary": "Accept-Encoding",
  "connection": "close",
  "date": "Wed, 03 Feb 2016 21:13:26 GMT"
}
```


### Http Headers API

**URL**
```
https://api.pageportrait.com/v1/headers
```

**Response**
```javascript
{
  "Location": "https://www.dtm.io/",
  "Date": "Tue, 16 May 2017 20:29:24 GMT",
  "Content-Type": "text/html; charset=iso-8859-1",
  "Server": "Apache"
}
```


### Meta Tags API

**URL**
```
https://api.pageportrait.com/v1/metatags
```

**Response**
```javascript
{
  "og:image": "http://pageportrait.com/images/logo-600x455.png",
  "description": "What does your page mean in a digital world? Discover your digital page portrait.",
  "twitter:card": "summary",
  "url": "http://pageportrait.com",
  "image": "http://pageportrait.com/images/logo-120x90.png",
  "og:description": "What does your page mean in a digital world? Discover your digital page portrait.",
  "og:title": "Instant Digital Page Portrait",
  "twitter:site": "@vpodk",
  "twitter:url": "http://pageportrait.com",
  "content-type": "text/html; charset=utf-8",
  "viewport": "user-scalable=no, initial-scale=1.0, maximum-scale=1.0, width=device-width"
}
```

**Notes**

Depreacated. Please use [Page Data API](https://github.com/PagePortrait/API/blob/master/README.md#page-data-api) instaed.



### Moz Data API

**URL**
```
https://api.pageportrait.com/v1/mozdata
```

**Response**
```javascript
{
  "domain-authority": 10.025181014176077,
  "links": 0,
  "page-authority": 1
}
```


### Page Data API

**URL**
```
https://api.pageportrait.com/v1/pagedata
```

**Response**
```javascript
{
  "emails": {"hr@dtm.io": 2},
  "content-length": 40819,
  "media-queries": {
    "screen and (max-width:774px)": 3,
    "screen and (min-width:1445px)": 1
  },
  "code-ratio": 4.916827947769422,
  "description": "From Concept To Reality",
  "headings": {
    "h1": ["Accelerate"],
    "h2": ["Datamart Services", "Datamart Partners", "Find Out More"]
  },
  "doctype": "DOCTYPE html",
  "frames": {"framesets": 0, "iframes": 0},
  "title": "Datamart - Accelerate Innovations",
  "trackers": {"Google Analytics (Universal)": 1},
  "embeds": {"total": 0, "applets": 0, "flash": 0},
  "deprecated": {},
  "images": {"unfriendly": 0, "vector": 7, "noalt": 0, "total": 20, "external": 0},
  "styles": {"inline": 1, "total": 1},
  "scripts": {"inline": 2, "total": 3},
  "text-length": 2007,
  "frameworks": {},
  "meta": {
    "name": ["Datamart - Accelerate Innovations"],
    "twitter:card": ["summary_large_image"],
    "viewport": ["user-scalable=no, initial-scale=1.0, maximum-scale=1.0, width=device-width"],
    "description": ["From Concept To Reality"],
    "og:title": ["Datamart - Accelerate Innovations"],
    "og:description": ["From Concept To Reality"],
    "og:type": ["website"],
    "fb:app_id": ["344116085973021"],
    "datepublished": ["2016-09-05"]
  },
  "links": {
    "data": {
      "/solutions/": {"counter": 1, "follow": "follow", "type": "Internal", "anchor": "Learn More"},
      "mailto:hr@dtm.io": {"counter": 1, "follow": "follow", "type": "CTA", "anchor": ""},
      "https://twitter.com": {"counter": 1, "follow": "follow", "type": "External", "anchor": "Follow"},
      "/company/contact/": {"counter": 1, "follow": "follow", "type": "Internal", "anchor": "Contacts"},
      "/open-source/": {"counter": 1, "follow": "follow", "type": "Internal", "anchor": "Open Source"},
      "tel:+14157997500": {"counter": 1, "follow": "follow", "type": "CTA", "anchor": ""},
      "https://www.dtm.io": {"counter": 1, "follow": "follow", "type": "Internal", "anchor": ""},
      "/": {"counter": 1, "follow": "follow", "type": "Internal", "anchor": "Datamart Home"}
    },
    "unfriendly": 0, "nofollow": 0, "total": 25, "friendly": 25, "external": 4, "underscored": 0
  }
}
```


### Social API

**URL**
```
https://api.pageportrait.com/v1/social
```

**Response**
```javascript
{
  "facebook": {"comment": 0, "total": 4, "likes": 0, "shares": 4},
  "gplusone": {"count": 0},
  "linkedin": {"shares": 4}
}
```


### Web Files API

**URL**
```
https://api.pageportrait.com/v1/webfiles
```

**Response**
```javascript
{"favicon.ico": 200, "sitemap.xml": 404, "robots.txt": 200}
```


### Whois Data API

**URL**
```
https://api.pageportrait.com/v1/whois
```

**Response**
```javascript
{
  "status": "clienttransferprohibited",
  "updated": "25-jan-2016",
  "created": "16-apr-2015",
  "ip": "184.73.223.98",
  "registrar": "google inc.",
  "expired": "16-apr-2017"
}
```

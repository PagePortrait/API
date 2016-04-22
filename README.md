# API [![Build Status](https://api.travis-ci.org/PagePortrait/API.svg?branch=master)](http://travis-ci.org/PagePortrait/API)

**Social API:** 
https://api.pageportrait.com/v1/social?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
  "facebook": {"comment": 0, "total": 4, "likes": 0, "shares": 4},
  "gplusone": {"count": 0},
  "linkedin": {"shares": 4}
});
```

**Whois Data API:**  
https://api.pageportrait.com/v1/whois?url=http://www.pageportrait.com&jsonp=cb
```javascript
cb({
  "status": "clienttransferprohibited",
  "updated": "25-jan-2016",
  "created": "16-apr-2015",
  "ip": "184.73.223.98",
  "registrar": "google inc.",
  "expired": "16-apr-2017"
});
```

**Moz Data API:**
https://api.pageportrait.com/v1/mozdata?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
  "domain-authority": 10.025181014176077,
  "links": 0,
  "page-authority": 1
});
```
*Example of Moz data report:* https://moz.com/researchtools/ose/links?site=scalr.com  
*Response fields references:* https://moz.com/help/guides/moz-api/mozscape/api-reference/url-metrics



**Page Data API:**
https://api.pageportrait.com/v1/pagedata?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
  "headings": {
    "h2": ["Testimonials", "Contacts"],
    "h3": ["Case studies", "Choose your Scalr"],
    "h4": ["The Policy driven Cloud Management Platform"],
    "h5": ["Enterprise edition", "Community Edition", "Follow us"],
    "h6": ["Scalr", "Resources", "Head office"]
  }
});
```

**Http Data API:**
https://api.pageportrait.com/v1/httpdata?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
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
 });
```

**Meta Tags API:**
https://api.pageportrait.com/v1/metatags?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
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
});
```

**Web Files API:**
https://api.pageportrait.com/v1/webfiles?url=http://pageportrait.com&jsonp=cb
```javascript
cb({"favicon.ico": 200, "sitemap.xml": 404, "robots.txt": 200});
```

**Audience API:**
https://api.pageportrait.com/v1/audience?url=http://ya.ru&jsonp=cb
```javascript
cb({
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
});
```

**Google API:**
https://api.pageportrait.com/v1/google?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
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
});
```

**Alexa API:**
https://api.pageportrait.com/v1/alexa?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
  "country": {"name": "Ukraine", "rank": "22867"},
  "global": {"rank": "3084726", "delta": "-6547191"}
});
```

**Content API (Proxy):**
https://api.pageportrait.com/v1/content?url=http://pageportrait.com&jsonp=cb
```javascript
cb({
  "content": "<!DOCTYPE html><html>...</html>",
  "status": 200,
  "headers": {
    "content-encoding": "gzip",
    "expires": "Wed, 03 Feb 2016 13:29:45 GMT",
    "server": "nginx",
    "last-modified": "Wed, 03 Feb 2016 13:29:45 GMT",
    "connection": "close",
    "cache-control": "no-cache,no-store,max-age=0,must-revalidate",
    "date": "Wed, 03 Feb 2016 13:29:45 GMT",
    "content-type": "text/html; charset=UTF-8",
    "x-frame-options": "DENY",
    ...
  }
});
```

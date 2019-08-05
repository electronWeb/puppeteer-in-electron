<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [connect][1]
    -   [Parameters][2]
-   [getPage][3]
    -   [Parameters][4]

## connect

Connects puppeteer to the electron app. Must be called at startup before the electron app is ready.

### Parameters

-   `app` **App** The app imported from electron.
-   `puppeteer` **puppeteer** The imported puppeteer namespace.
-   `port` **[number][5]** Port to host the DevTools websocket connection. If none is given, we will pick an open port. (optional, default `0`)

Returns **[Promise][6]&lt;Browser>** An object containing the puppeteer browser, the port, and json received from DevTools.

## getPage

Given a BrowserWindow, find the corresponding puppeteer Page. It is undefined if external operations
occur on the page whilst we are attempting to find it. A url/file must be loaded on the window for it to be found.
If no url is loaded, the parameter 'allowBlankNavigate' allows us to load "about:blank" first.

### Parameters

-   `browser` **Browser** The puppeteer browser instance obtained from calling |connect|.
-   `window` **BrowserWindow** The browser window for which we want to find the corresponding puppeteer Page.
-   `allowBlankNavigate` **[boolean][7]** If no url is loaded, allow us to load "about:blank" so that we may find the Page. (optional, default `true`)

Returns **[Promise][6]&lt;Page>** The page that corresponds with the BrowserWindow.

[1]: #connect

[2]: #parameters

[3]: #getpage

[4]: #parameters-1

[5]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[6]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise

[7]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean
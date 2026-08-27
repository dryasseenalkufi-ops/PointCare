<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link href="https://media.base44.com/images/public/6a89a08b639d60fe6fff8383/8e1c452ec_logo.jpg" rel="icon" type="image/svg+xml" />
    <meta content="width=device-width, initial-scale=1.0" name="viewport" />
    <link href="/manifest.json" rel="manifest" />
    <title>
      Base44 APP
    </title>
    <script crossorigin="" src="/assets/index-EIGBkepD.js" type="module">
    </script>
    <link crossorigin="" href="/assets/index-zMXdP_Da.css" rel="stylesheet" />
    <script type="module">
      if (window.self === window.top) {
  let lastPath = &#34;&#34;;
  function getPageNameFromPath(path) {
    const segments = path.split(&#34;/&#34;).filter(Boolean);
    return segments[0] || null;
  }
  function trackPageView() {
    const path = window.location.pathname;
    if (path === lastPath) return;
    lastPath = path;
    const pageName = getPageNameFromPath(path) || &#34;home&#34;;
    const appId = &#34;6a89a08b639d60fe6fff8383&#34;;
    if (!appId) return;
    fetch(`/api/app-logs/${appId}/log-user-in-app/${pageName}`, {
      method: &#34;POST&#34;,
    }).catch(() =&gt; {});
  }
  const originalPushState = history.pushState.bind(history);
  history.pushState = function (...args) {
    originalPushState(...args);
    trackPageView();
  };
  const originalReplaceState = history.replaceState.bind(history);
  history.replaceState = function (...args) {
    originalReplaceState(...args);
    trackPageView();
  };
  window.addEventListener(&#34;popstate&#34;, trackPageView);
  trackPageView();
}
    </script>
    <meta content="yes" name="mobile-web-app-capable" />
    <meta content="black" name="apple-mobile-web-app-status-bar-style" />
    <meta content="Stator " name="apple-mobile-web-app-title" />
    <script async="true" data-app-id="6a89a08b639d60fe6fff8383" data-platform-url="https://app.base44.com" src="/static/js/badge.js">
    </script>
  </head>
  <body>
    <div id="root">
    </div>
  </body>
</html>

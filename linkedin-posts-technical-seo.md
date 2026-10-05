# 100 LinkedIn Posts: Crawling and Advanced Technical SEO

Every post is between 1,500 and 2,000 characters, follows a "What is / How to / Why it matters for rankings" structure, and ends with a CTA to the 4-Day Advanced Technical SEO Workshop Series.

Copy everything between the heading and the `---` line.

---

## Post 1: What is crawling?

What is crawling, and why does every ranking start here?

Before Google can rank a page, it has to find it and download it. That first step is called crawling.

Here's how it works:

Step 1: Google discovers a URL through links on other pages or through your XML sitemap.

Step 2: The URL is added to a crawl queue.

Step 3: Googlebot checks your robots.txt to see if it's allowed to fetch the URL.

Step 4: If allowed, Googlebot sends an HTTP request and downloads the page.

Step 5: Links in the page are extracted and added back to the queue.

Explained simply:

Think of Google as a librarian who can only catalogue the books delivered to the library. Crawling is the delivery. Google doesn't 'see' the web live; it works from copies its crawlers have downloaded. If a page is never fetched, or the fetch fails, Google simply has no copy to evaluate, however good the content is.

Common mistake to avoid:

Publishing a page and assuming Google will find it. Orphan pages with no internal links and no sitemap entry can go undiscovered for months.

Why it matters for rankings:

→ A page that isn't crawled can't be indexed.
→ A page that isn't indexed can't rank.
→ Crawl problems silently cap your organic growth.

Fix crawling first. Everything else builds on it.

Source: https://developers.google.com/search/docs/fundamentals/how-search-works

🎓 Want to master crawling hands-on? Join our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #SEO #Googlebot #Crawling

---

## Post 2: What is Googlebot?

What is Googlebot?

Googlebot is the generic name for Google Search's web crawler. It comes in two types:

→ Googlebot Smartphone: simulates a user on a mobile device
→ Googlebot Desktop: simulates a user on a desktop

How to see Googlebot on your site:

Step 1: Open your server access logs.

Step 2: Filter by the user agent containing "Googlebot".

Step 3: Verify the requests are real using a reverse DNS lookup (fake Googlebots are common).

Step 4: Check which pages it visits most, and which it never visits.

Explained simply:

Googlebot isn't one machine. It's a large distributed system making requests from many IP addresses at once. It decides what to fetch based on how important your URLs look, how often they change, and how much load your server can take. Every request it makes is a decision about how to use limited crawling capacity.

Common mistake to avoid:

Blocking or rate limiting 'Googlebot' based only on the user-agent string. Fake bots are blocked, but so is the real one if you never verify by DNS.

Why it matters for rankings:

Googlebot is your only route into Google's index. If it spends its time on junk URLs, your money pages get crawled less often, and updates take longer to show in search.

Source: https://developers.google.com/search/docs/crawling-indexing/googlebot

🎓 Learn log analysis and crawler verification live in our 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Googlebot #SEO

---

## Post 3: What is mobile-first indexing?

What is mobile-first indexing?

Google uses the mobile version of your content, crawled with Googlebot Smartphone, for indexing and ranking.

If your mobile page shows less content than your desktop page, Google indexes less.

How to make your site mobile-first ready:

Step 1: Serve the same primary content on mobile and desktop.

Step 2: Keep the same structured data on both versions.

Step 3: Keep the same title, meta description and robots meta tags.

Step 4: Make sure images and videos on mobile are crawlable, with the same alt text.

Step 5: Check your logs. Most Googlebot requests should come from Googlebot Smartphone.

Explained simply:

Before mobile-first indexing, Google mainly looked at desktop pages. Now the smartphone crawler's view is the version that counts for indexing and ranking. Desktop still matters to your users, but for Google the mobile HTML is the source of truth. Content, links and markup that exist only on desktop are effectively invisible.

Common mistake to avoid:

Using a 'lighter' mobile template that drops reviews, FAQs, breadcrumbs or internal links to save space. Those are often the very signals that help a page rank.

Why it matters for rankings:

Whatever is missing on mobile is effectively missing from Google. Hidden tabs, trimmed text or removed schema on mobile can cost you rankings you earned on desktop.

Source: https://developers.google.com/search/docs/crawling-indexing/mobile/mobile-sites-mobile-first-indexing

🎓 Audit mobile parity step by step in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#MobileFirst #TechnicalSEO #SEO

---

## Post 4: What are the 3 types of Google crawlers?

What are the 3 types of Google crawlers?

Not every "Google" visitor in your logs is Googlebot. Google groups its crawlers into three categories:

Type 1: Common crawlers
Examples: Googlebot, Googlebot-Image, Storebot-Google.
They always obey robots.txt when crawling automatically.

Type 2: Special-case crawlers
Examples: AdsBot-Google, Mediapartners-Google.
Used where a site has an agreement with a Google product. They may ignore robots.txt and use different IP ranges.

Type 3: User-triggered fetchers
Examples: Feedfetcher, Google Site Verifier, Google-NotebookLM.
A user triggers the fetch, so they generally ignore robots.txt.

How to use this:

Step 1: Group your log hits by user agent.

Step 2: Map each one to its category.

Step 3: Write robots.txt rules only for crawlers that actually follow them.

Explained simply:

These categories exist because each kind of fetch has a different reason. Automatic crawling for an index must respect your robots.txt. A fetch a user explicitly asks for (like adding a URL to a notebook) is more like a person visiting your site. And ads and safety systems have their own agreements. Knowing the category tells you which controls actually work.

Common mistake to avoid:

Writing robots.txt rules for user-triggered fetchers and assuming they're blocked. Those fetchers generally ignore robots.txt, so private content needs real access control.

Why it matters for rankings:

Only common crawlers like Googlebot feed Google Search. Knowing the difference stops you from blocking the wrong bot, or worrying about the wrong one.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/overview-google-crawlers

🎓 Master Google's crawler ecosystem in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Googlebot #SEO

---

## Post 5: What is Googlebot-Image?

What is Googlebot-Image?

Googlebot-Image is the crawler that fetches your images.

Rules you write for Googlebot-Image affect:
→ Google Images
→ Discover
→ Google Video
→ Every Search feature that shows images, logos and favicons

How to make your images crawlable:

Step 1: Use a standard <img src="..."> element, not CSS background images, for important images.

Step 2: Don't block your image folders or CDN in robots.txt.

Step 3: Add descriptive alt text and file names.

Step 4: List key images in an image sitemap if they're loaded in unusual ways.

Step 5: Check that your image CDN returns 200, not 403, to Googlebot-Image.

Explained simply:

Images are crawled separately from the pages they appear on. Googlebot fetches the HTML; Googlebot-Image fetches the image files. So a page can be fully indexed while its images are blocked, broken or never discovered. Image search, Discover cards and rich results all depend on the image files being reachable.

Common mistake to avoid:

Hosting images on a CDN subdomain with its own robots.txt that says 'Disallow: /'. The main site looks fine, but every image is blocked.

Why it matters for rankings:

Blocked images mean no image search traffic, no thumbnail in Discover, and sometimes no favicon or logo in results. All of these cost clicks.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers

🎓 Learn image SEO and crawl control hands-on in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#ImageSEO #TechnicalSEO #SEO

---

## Post 6: What is Storebot-Google?

What is Storebot-Google?

Storebot-Google is Google's crawler for Shopping.

Rules addressed to Storebot-Google affect all Google Shopping surfaces, including the Shopping tab in Search.

How to keep your products visible to Storebot-Google:

Step 1: Check robots.txt for any rule that blocks Storebot-Google or your product URLs.

Step 2: Make sure product pages return 200 with price and availability in the HTML.

Step 3: Add Product structured data with offers, price and availability.

Step 4: Keep the price on the page consistent with your Merchant Center feed.

Step 5: Watch your logs for Storebot-Google hits on key product URLs.

Explained simply:

Shopping results show live product facts: price, stock and offers. To show them confidently, Google needs to crawl the product page and check it matches what you claim in your feed. Storebot-Google does that work. If it can't fetch the page, or sees different data, products can be limited or disapproved.

Common mistake to avoid:

Showing prices only after JavaScript runs or a location is selected. Storebot may see no price, or a different price from your feed, and treat it as a mismatch.

Why it matters for rankings:

For ecommerce, Shopping surfaces are prime real estate. If Storebot can't crawl your products, they can drop out of Shopping results while your competitors keep showing.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers

🎓 Learn ecommerce technical SEO live in our 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#EcommerceSEO #TechnicalSEO #GoogleShopping

---

## Post 7: What is Google-InspectionTool?

What is Google-InspectionTool?

When you run a live test in Search Console or the Rich Results Test, the request comes from Google-InspectionTool, not Googlebot.

Important: rules for Google-InspectionTool affect only these testing tools. They have no effect on Google Search.

How to use it correctly:

Step 1: Run URL Inspection → Test Live URL in Search Console.

Step 2: Find the request in your server logs under Google-InspectionTool.

Step 3: Compare its response code and response time with normal Googlebot hits.

Step 4: If a live test fails but Googlebot succeeds, check firewall or bot rules that treat the two differently.

Explained simply:

Google separated testing traffic from real crawling so you can debug without affecting your index. When you click 'Test Live URL', you get a fresh fetch from a separate user agent. This is useful: it shows how your server responds right now, rather than what Google stored at the last crawl, which may be days old.

Common mistake to avoid:

Assuming a live test result is what Google has indexed. The indexed version is from the last real Googlebot crawl. Compare both views before drawing conclusions.

Why it matters for rankings:

Live tests are how you debug indexing problems. If your firewall blocks the inspection tool, you lose your best diagnostic view and may "fix" problems that don't exist.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers

🎓 Learn advanced Search Console debugging in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsole #TechnicalSEO #SEO

---

## Post 8: What is GoogleOther?

What is GoogleOther?

GoogleOther is a generic Google crawler that product teams use to fetch publicly available content, for example for one-off crawls for internal research and development.

Key point: rules for GoogleOther don't affect any specific Google product, including Search.

How to handle GoogleOther:

Step 1: Spot it in your logs by the "GoogleOther" user agent token.

Step 2: Verify it's real with reverse and forward DNS lookups.

Step 3: Decide whether you want to allow it. Blocking it doesn't affect your Search visibility.

Step 4: If it adds noticeable server load, add a specific rule:
User-agent: GoogleOther
Disallow: /heavy-section/

Explained simply:

Google teams sometimes need web data for research or product development that isn't for Search. Rather than reusing the Googlebot name, which would muddy your logs and controls, they use GoogleOther. That separation is good for site owners: you can make a separate decision about this traffic without any risk to your rankings.

Common mistake to avoid:

Seeing a spike of 'Google' traffic in logs and blocking Google IP ranges broadly. That can take Googlebot down with it. Always block by the specific user agent token.

Why it matters for rankings:

Knowing which Google crawlers actually feed Search stops you from panicking over crawl stats, and stops you from blocking Googlebot by mistake when you only meant to block another crawler.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-common-crawlers

🎓 Learn precise crawler control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #RobotsTxt #SEO

---

## Post 9: What is Google-Extended?

What is Google-Extended?

Google-Extended is a robots.txt token, not a separate crawler.

It lets you control whether content Google crawls from your site may be used to:
→ Train future Gemini models
→ Ground answers in Gemini Apps

Google states that Google-Extended does not affect inclusion in Google Search and is not a ranking signal.

How to opt out of Gemini training:

Step 1: Open your robots.txt.

Step 2: Add:
User-agent: Google-Extended
Disallow: /

Step 3: Leave your Googlebot rules unchanged.

Step 4: Re-check that robots.txt returns a 200 status.

Explained simply:

Google-Extended doesn't change how Googlebot crawls your site. Googlebot still fetches your pages for Search as normal. The token only tells Google whether that content may be used for Gemini model training and Gemini Apps grounding. It's a usage permission, not a crawl block, which is why it can't affect your Search visibility.

Common mistake to avoid:

Thinking Google-Extended controls AI Overviews. It doesn't. AI Overviews are part of Search, controlled by normal Search directives like noindex and nosnippet.

Why it matters for rankings:

Many sites block "Google" too broadly to stop AI training and accidentally hurt Search. Google-Extended lets you make an AI training decision with no impact on your Search rankings.

Source: https://developers.google.com/search/docs/appearance/ai-features

🎓 Learn AI-era crawl governance in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#GoogleExtended #AISearch #TechnicalSEO

---

## Post 10: What is Google-Agent?

What is Google-Agent?

Google-Agent is a user-triggered fetcher. Agents running on Google's infrastructure use it to navigate websites and take actions when a user asks them to.

It has two forms in requests: a mobile agent and a desktop agent. Its IP ranges are published in user-triggered-agents.json.

How to prepare your site for Google-Agent:

Step 1: Add "Google-Agent" to the bot dashboards you watch in your logs.

Step 2: Verify requests against Google's published IP ranges.

Step 3: Make sure key actions such as search, filtering and checkout work with plain HTML forms and links.

Step 4: Make sure your firewall doesn't block verified Google agent traffic.

Explained simply:

Traditional crawlers read pages. Agents act on them: searching a catalogue, comparing options, filling in a form for a user. Google-Agent identifies these visits so you can recognise and manage them. As users hand more tasks to AI assistants, your site's usability for an agent becomes part of being findable.

Common mistake to avoid:

Building key flows that only work with complex client-side widgets, hover menus or CAPTCHAs on every step. Agents struggle with these, just as accessibility tools do.

Why it matters for rankings:

AI agents are becoming a new way users reach your site. Sites agents can't use will lose that traffic, much like sites that blocked Googlebot lost organic traffic.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-user-triggered-fetchers

🎓 Get ready for agentic search in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#AIAgents #AISearch #TechnicalSEO

---

## Post 11: What are special-case crawlers?

What are Google's special-case crawlers?

These are crawlers for specific products where a site has an agreement with Google about crawling. Examples:

→ AdsBot-Google: checks the quality of ad landing pages
→ Mediapartners-Google: serves relevant ads for AdSense
→ APIs-Google: delivers push notifications
→ Google-Safety: finds malware and abuse

The trap: AdsBot-Google and Mediapartners-Google ignore the global "User-agent: *" group.

How to control them correctly:

Step 1: Don't assume "User-agent: *" covers every Google bot.

Step 2: To block one, name it explicitly:
User-agent: AdsBot-Google
Disallow: /private/

Step 3: Never block AdsBot on landing pages you run Google Ads to.

Step 4: Remember that Google-Safety ignores robots.txt entirely.

Explained simply:

Special-case crawlers serve products where you've made a choice, like running Google Ads or AdSense. Because you opted in, these bots follow their own rules. AdsBot, for example, checks landing pages so ad quality scores reflect reality. That's why a blanket '*' rule doesn't apply to it: you have to address it by name.

Common mistake to avoid:

Adding 'User-agent: * Disallow: /' on a staging or campaign site and assuming AdsBot is blocked. It isn't. Name AdsBot-Google explicitly if you really mean it.

Why it matters for rankings:

Getting this wrong won't directly hit organic rankings, but it can break ads quality checks and waste server resources you need for Googlebot.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-special-case-crawlers

🎓 Learn every Google crawler in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #GoogleAds #SEO

---

## Post 12: What are user-triggered fetchers?

What are user-triggered fetchers?

These are Google fetchers that run because a user asked for something, much like a wget request. Examples:

→ Feedfetcher: RSS/Atom feeds for Google News and WebSub
→ Google Site Verifier: Search Console verification
→ Google-NotebookLM: URLs that users add as sources
→ Google-Pinpoint: URLs added to document collections

Because a person triggers the fetch, these generally ignore robots.txt.

How to handle them:

Step 1: Don't rely on robots.txt to keep private content away from them.

Step 2: Protect private content with authentication instead.

Step 3: Verify the IPs against Google's user-triggered-fetchers.json.

Step 4: Treat a spike in these fetches as a sign of user interest.

Explained simply:

robots.txt was designed for automated crawlers that wander the web. When a person pastes your URL into a tool, the fetch is more like that person opening the page themselves. That's why these fetchers generally don't check robots.txt. It's a key reason why robots.txt should never be your privacy or security layer.

Common mistake to avoid:

Putting 'secret' URLs in robots.txt to hide them. robots.txt is public, so you're advertising those paths to anyone who reads it, and user-triggered fetchers can still load them.

Why it matters for rankings:

robots.txt isn't a security tool. If content must stay private, put it behind a login, or it can be fetched and surfaced in ways you didn't plan for.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/google-user-triggered-fetchers

🎓 Learn crawl security and control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #RobotsTxt #SEO

---

## Post 13: How to verify Googlebot

How to verify that a request really came from Googlebot

Scrapers often fake the Googlebot user agent. Here's Google's official verification method.

Step 1: Take the requesting IP from your logs, for example 66.249.66.1.

Step 2: Run a reverse DNS lookup:
host 66.249.66.1

Step 3: Confirm the hostname ends in googlebot.com, for example:
crawl-66-249-66-1.googlebot.com

Step 4: Run a forward DNS lookup on that hostname.

Step 5: Confirm it resolves back to the same IP. Only then is it a real Googlebot.

Bonus: For automated checks, match IPs against Google's published JSON IP range files.

Explained simply:

A user-agent string is just text that any script can copy. Scrapers often pretend to be Googlebot because many sites give Googlebot special treatment. DNS is much harder to fake: only Google controls the googlebot.com DNS records. The two-way lookup proves the IP really belongs to Google's crawler.

Common mistake to avoid:

Doing only the reverse lookup. Anyone controlling their own IP's reverse DNS could fake a googlebot.com name. The forward lookup back to the same IP is what proves it.

Why it matters for rankings:

If you block fake bots, you save server capacity for real Googlebot. If you block the real Googlebot by mistake, your crawling stops. Verification protects both your server and your rankings.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/verify-google-requests

🎓 Learn bot verification and log analysis live in our 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Googlebot #TechnicalSEO #LogAnalysis

---

## Post 14: How to use Google's crawler IP range files

How to use Google's crawler IP range files (they've moved)

Google publishes its crawler IP ranges as JSON files in CIDR format. In 2026 they moved to:
developers.google.com/crawling/ipranges/

The files:
→ common-crawlers.json
→ special-crawlers.json
→ user-triggered-fetchers.json
→ user-triggered-agents.json

How to update your setup:

Step 1: Find every firewall, CDN or bot-management rule that uses Google's IP lists.

Step 2: Replace the old /search/apis/ipranges/ paths with the new location.

Step 3: Schedule an automatic refresh, because the ranges change.

Step 4: Test that verified Googlebot traffic still gets a 200.

Explained simply:

DNS checks are reliable but slow to run on every request. Published IP ranges let firewalls and CDNs verify crawlers instantly, by checking which range an IP falls in. The files are split by crawler category, so you can allow common crawlers, special-case crawlers and user-triggered fetchers separately.

Common mistake to avoid:

Hard-coding a copy of the IP list into your firewall and never updating it. Google adds and changes ranges, so a frozen list will eventually block real Googlebot traffic.

Why it matters for rankings:

A stale allowlist can quietly block or challenge real Googlebot. That shows up later as crawl drops and pages falling out of the index.

Source: https://developers.google.com/search/blog/2026/03/crawler-ip-ranges

🎓 Learn crawler infrastructure hands-on in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Googlebot #DevOps

---

## Post 15: How to read Googlebot activity in server logs

How to read Googlebot activity in your server logs

Search Console shows samples. Your logs show every request.

Step 1: Export 30 days of access logs.

Step 2: Filter by user agent: Googlebot, Googlebot-Image, Storebot-Google.

Step 3: Verify the IPs, and remove fake bots.

Step 4: Group hits by status code. Look for 3xx, 4xx and 5xx clusters.

Step 5: Group hits by URL pattern. Spot parameter and filter URLs eating crawls.

Step 6: Compare against your sitemap. Find important URLs that are never crawled.

Step 7: Track response time. Slow responses mean less crawling.

Explained simply:

Search Console summarises crawling; your logs record every single request. Only logs show exactly which URLs Googlebot fetched, when, and what your server returned. On large sites, log analysis regularly finds Googlebot spending most of its visits on parameters, redirects and old URLs nobody cares about.

Common mistake to avoid:

Analysing logs without separating verified Googlebot from fakes. Fake bot traffic can make it look as if Google is crawling junk when it isn't, or hide what the real bot is doing.

Why it matters for rankings:

Logs show where your crawl activity actually goes. Moving crawling from junk URLs to revenue pages gets new content indexed faster and keeps key pages fresh in search.

Source: https://developers.google.com/crawling/docs/crawl-budget

🎓 Run real log-file analysis with us in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#LogFileAnalysis #TechnicalSEO #CrawlBudget

---

## Post 16: What is robots.txt?

What is robots.txt?

robots.txt is a plain-text file at the root of your domain that tells crawlers which URLs they may or may not crawl. It's standardized as RFC 9309.

How to create one properly:

Step 1: Create a file named robots.txt at https://yourdomain.com/robots.txt

Step 2: Add a group for a user agent:
User-agent: *

Step 3: Add rules:
Disallow: /cart/
Allow: /cart/help

Step 4: Add your sitemap:
Sitemap: https://yourdomain.com/sitemap.xml

Step 5: Make sure it returns HTTP 200 and is under 500 KiB.

Explained simply:

robots.txt is the first file a well-behaved crawler requests on your host, before any page. Its rules apply per host and protocol, so https://www.example.com and https://shop.example.com each need their own file. It's a set of crawl instructions, not access control, and it doesn't remove pages from the index. Think of it as signposts for crawlers, not a locked door.

Common mistake to avoid:

Using robots.txt to hide pages that are already indexed. Blocking crawling stops Google seeing any noindex, so the URLs can stay in results without a description.

Why it matters for rankings:

A clean robots.txt points crawling at the pages that earn rankings. A single wrong "Disallow: /" can wipe a site out of Google.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn advanced robots.txt strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 17: How robots.txt rule precedence works

How does Google decide between conflicting robots.txt rules?

Example:
Allow: /shop/
Disallow: /shop/checkout

Which rule wins for /shop/checkout/page?

Step 1: Google finds every rule that matches the URL path.

Step 2: The most specific rule (the longest matching path) wins.

Step 3: If two matching rules are equally specific, the least restrictive one (Allow) wins.

Step 4: Only the most specific user-agent group applies. Googlebot ignores "*" if a "Googlebot" group exists.

Answer: Disallow: /shop/checkout wins, because it's longer.

Explained simply:

Google doesn't read robots.txt top to bottom and stop at the first match, as many people assume. It looks at every rule that matches and picks the most specific one, meaning the one with the longest path. Order in the file doesn't matter. This lets you block a section broadly while carving out exceptions.

Common mistake to avoid:

Adding a new 'User-agent: Googlebot' group with one rule, without copying the existing '*' rules. Googlebot then follows only that group and ignores everything under '*'.

Why it matters for rankings:

Most robots.txt disasters come from misunderstood precedence. One extra Googlebot group can silently override every rule you wrote under "*".

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Practice robots.txt edge cases live in our 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 18: How to use wildcards in robots.txt

How to use wildcards in robots.txt

Google supports two special characters:

* matches any sequence of characters
$ marks the end of the URL

Step 1: Block every URL containing a session parameter:
Disallow: /*?sessionid=

Step 2: Block all PDFs:
Disallow: /*.pdf$

Step 3: Block sort parameters anywhere in the URL:
Disallow: /*?*sort=

Step 4: Test each pattern against real URLs from your logs before you publish.

Step 5: Watch Crawl Stats for a week after the change.

Explained simply:

Without wildcards, you would need a separate rule for every URL variation. Patterns let one line cover thousands of parameter combinations. The $ anchor matters because rules are prefix matches by default: 'Disallow: /*.pdf' also matches '/file.pdf?download=1' and '/file.pdfguide'. Adding $ restricts it to URLs that end exactly there.

Common mistake to avoid:

Writing a broad pattern like 'Disallow: /*?' to kill parameters, which also blocks pagination, internal search and tracking-free product variants you wanted crawled.

Why it matters for rankings:

Wildcards are the fastest way to shut down crawl traps such as session IDs, sorting and tracking parameters. Less crawling of junk URLs means more crawling of the pages you want to rank.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn crawl trap control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #CrawlBudget #TechnicalSEO

---

## Post 19: What happens when robots.txt returns 404?

What happens if your robots.txt returns a 404?

Google treats every 4xx status (except 429) for robots.txt as if no robots.txt exists.

That means Google assumes there are no crawl restrictions, and your whole site is open to crawling.

How to check yours:

Step 1: Run curl -I https://yourdomain.com/robots.txt

Step 2: Confirm the status is 200.

Step 3: If it's 404, check whether that's intentional. A deployment may have deleted the file.

Step 4: If it's 403, check your CDN or firewall rules.

Step 5: Re-check after every release.

Explained simply:

Google's logic is simple: a 4xx means the file doesn't exist, and if there are no rules, there are no restrictions. That's usually harmless for small sites. But if your robots.txt was holding back faceted URLs, internal search pages or staging paths, a 404 removes all those guardrails at once.

Common mistake to avoid:

A redesign or CDN migration that forgets to carry over robots.txt. The site launches fine, but crawling suddenly floods into URL patterns you'd previously blocked.

Why it matters for rankings:

A missing robots.txt can suddenly expose admin pages, filter combinations and staging paths to crawling. That wastes crawl activity and lets duplicate pages get indexed.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn release-safe technical SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 20: What happens when robots.txt returns 5xx?

What happens if your robots.txt returns a 5xx error?

This is one of the most dangerous technical SEO failures. Here's Google's documented behavior:

Step 1: For the first 12 hours, Google stops crawling your site and keeps retrying robots.txt.

Step 2: For up to 30 days after that, Google uses the last good copy it has, if it has one.

Step 3: After 30 days, if the rest of the site is reachable, Google behaves as if there's no robots.txt.

How to prevent it:

→ Serve robots.txt as a static file, or from the CDN edge.
→ Monitor its status code every few minutes.
→ Alert on any 5xx or timeout.

Explained simply:

A server error is ambiguous. Google can't tell whether you meant to block everything or the server is just broken, so it takes the cautious path: it stops crawling rather than risk crawling URLs you might have disallowed. That's why a robots.txt outage can affect your whole site more than an outage on any single page.

Common mistake to avoid:

Generating robots.txt dynamically from the same app and database as the rest of the site. When the app falls over, robots.txt fails too, and crawling stops along with it.

Why it matters for rankings:

A broken robots.txt can halt crawling of your whole site. New pages won't get indexed and updates won't be picked up until it's fixed.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn uptime-safe SEO infrastructure in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SiteReliability

---

## Post 21: What is the robots.txt 500 KiB limit?

What is the robots.txt size limit?

Google processes the first 500 KiB of a robots.txt file. Content after that limit is ignored.

How to stay safely under it:

Step 1: Check your file size:
curl -s https://yourdomain.com/robots.txt | wc -c

Step 2: Remove duplicate and outdated rules.

Step 3: Replace long lists of URLs with wildcard patterns:
Disallow: /*?filter=

Step 4: Keep your most important rules near the top.

Step 5: Use noindex or remove pages instead of listing thousands of individual URLs.

Explained simply:

Size limits keep crawlers from holding connections open for too long on huge files. The standard (RFC 9309) requires crawlers to parse at least 500 KiB; Google stops there. Most sites are nowhere near it, but auto-generated robots.txt files on very large platforms can grow without anyone noticing. A quick size check once a quarter is enough to catch it.

Common mistake to avoid:

Having a CMS or plugin append one Disallow line per URL over the years. The file grows huge, and rules near the bottom quietly stop working.

Why it matters for rankings:

Rules past 500 KiB are ignored. If your important Disallow rules are at the bottom of a huge file, the crawl traps they were meant to stop are open again.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn scalable crawl control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 22: How long does Google cache robots.txt?

How long does Google cache your robots.txt?

Google generally caches robots.txt for up to 24 hours. It can cache it longer if a refresh fails (for example timeouts or 5xx errors), and it may adjust the cache lifetime based on your Cache-Control max-age header.

How to roll out a robots.txt change safely:

Step 1: Edit and deploy the new robots.txt.

Step 2: Confirm it returns 200 with the new content.

Step 3: Expect up to about a day before Google uses it.

Step 4: Don't make emergency changes and then reverse them within hours.

Step 5: Watch Crawl Stats over the following days for the effect.

Explained simply:

Fetching robots.txt before every single page request would be wasteful, so Google keeps a copy and refreshes it about once a day. This means robots.txt changes aren't instant in either direction. A fix doesn't take effect right away, and neither does a mistake, which gives you a short window to catch errors.

Common mistake to avoid:

Expecting a robots.txt fix to immediately bring back crawling after an accidental block, then making more changes when nothing happens within an hour.

Why it matters for rankings:

Understanding the cache stops panic edits. A "Disallow: /" that's live for an hour can stay in Google's cache for a day, and that's a day of lost crawling.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Learn change management for SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 23: robots.txt vs noindex: what's the difference?

robots.txt vs noindex: which should you use?

robots.txt controls crawling.
noindex controls indexing.

The trap: if you block a page in robots.txt, Google can't see the noindex on it. The URL can still be indexed without content if other pages link to it.

How to remove a page from Google properly:

Step 1: Add <meta name="robots" content="noindex"> to the page, or send an X-Robots-Tag: noindex header.

Step 2: Make sure robots.txt allows the URL to be crawled.

Step 3: Wait for Google to recrawl the page and see the noindex.

Step 4: Only after it drops out of the index, consider blocking it in robots.txt if crawl budget matters.

Explained simply:

Crawling and indexing are separate steps. Google can know a URL exists (from links) without ever crawling it, and it can index that URL using only link information. noindex is an instruction inside the page, so Google has to fetch the page to read it. Block the fetch and the instruction is never delivered.

Common mistake to avoid:

Adding noindex and a robots.txt Disallow to the same pages at the same time. It feels doubly safe, but the Disallow stops Google seeing the noindex.

Why it matters for rankings:

Mixing up these two causes "Indexed, though blocked by robots.txt" pages: thin listings with no description that look bad in search.

Source: https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag

🎓 Learn index control the right way in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Noindex #RobotsTxt #TechnicalSEO

---

## Post 24: Which robots.txt rules does Google ignore?

Which robots.txt rules does Google ignore?

Many sites still rely on rules Google doesn't support:

→ crawl-delay: ignored by Google
→ noindex: in robots.txt: not supported
→ nofollow: in robots.txt: not supported

How to replace them:

Step 1: Instead of crawl-delay, temporarily return 503 or 429 if your server is overloaded.

Step 2: Instead of noindex in robots.txt, use the robots meta tag or the X-Robots-Tag header.

Step 3: Instead of nofollow in robots.txt, use rel="nofollow" on the individual links.

Step 4: Remove the unsupported lines to keep the file clean.

Step 5: Keep crawl-delay only if you need it for other bots that support it, such as ClaudeBot.

Explained simply:

robots.txt has a small, standardised set of rules: user-agent, allow, disallow and sitemap. Over the years, sites added unofficial lines that some crawlers supported and others didn't. Google formalised the protocol as RFC 9309 and stopped honouring unofficial rules like noindex in robots.txt, so relying on them is a silent failure.

Common mistake to avoid:

Trusting a robots.txt line because 'it was always there'. Old rules from another era may not do anything with Google today. Check each line against the documentation.

Why it matters for rankings:

If you rely on rules Google ignores, pages you think are noindexed can still be indexed, and pages you think are throttled can still overload your server.

Source: https://developers.google.com/search/blog/2019/07/a-note-on-unsupported-rules-in-robotstxt

🎓 Learn which signals Google actually uses in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 25: How to update robots.txt safely

How to update robots.txt without breaking your SEO

Step 1: Download the current live file and save a backup.

Step 2: Write the change and test every new rule against a list of 20 to 50 real URLs.

Step 3: Check that your key templates (home, category, product, blog) stay allowed.

Step 4: Check that CSS and JS paths stay allowed. Google needs them for rendering.

Step 5: Deploy, then confirm a 200 status and the new content.

Step 6: Check the robots.txt report in Search Console to see what Google last fetched.

Step 7: Monitor Crawl Stats and the Page Indexing report for 1 to 2 weeks.

Explained simply:

robots.txt is a single file with sitewide impact. One character can change the meaning of a rule: 'Disallow: /' blocks everything, while 'Disallow:' (empty) blocks nothing. That's why changes to it deserve the same testing and review as a code deployment, not a quick edit in production.

Common mistake to avoid:

Copying a staging robots.txt that contains 'Disallow: /' to production during a launch. It's one of the most common, and most damaging, technical SEO incidents.

Why it matters for rankings:

Blocking CSS or JS can stop Google rendering your pages properly. A broad Disallow can deindex whole sections. A tested rollout protects the rankings you already have.

Source: https://developers.google.com/crawling/docs/robots-txt/submit-updated-robots-txt

🎓 Learn our robots.txt QA process in the live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #TechnicalSEO #SEO

---

## Post 26: What is Googlebot's 2MB limit?

What is Googlebot's 2MB limit?

When crawling for Google Search, Googlebot fetches only the first 2MB of an HTML page, counting the HTTP headers.

Anything after 2MB isn't fetched, rendered or indexed. The page isn't rejected; the fetch just stops.

How to check whether you're at risk:

Step 1: Fetch the raw, uncompressed HTML of your biggest templates.

Step 2: Measure the size:
curl -s --compressed URL | wc -c

Step 3: Look for bloat: inline JSON state, inline SVG, inline CSS, huge menus.

Step 4: Move heavy CSS and JS into external files. Each external file gets its own 2MB limit.

Step 5: Re-measure until you have comfortable headroom.

Explained simply:

Google has to process billions of pages, so it limits how many bytes it takes from each URL. For HTML in Google Search, that limit is 2MB, including the HTTP headers. Most pages are far smaller, but modern frameworks can inline huge chunks of JSON, CSS and SVG, quietly pushing the real content further down.

Common mistake to avoid:

Assuming the limit is about images or video. It's about the HTML file itself. Images and scripts are separate requests, each with its own limit.

Why it matters for rankings:

If your main content, links or structured data sit past the cutoff, Google never sees them. Content Google doesn't see can't help you rank.

Source: https://developers.google.com/search/blog/2026/03/crawler-blog-post

🎓 Learn advanced crawl efficiency in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Googlebot #TechnicalSEO #PageSize

---

## Post 27: How the 2MB limit is measured

How is Googlebot's 2MB limit measured?

Many SEOs check the gzipped transfer size in DevTools and think they're safe. They may not be.

Google's file size limits apply to uncompressed data.

How to measure it correctly:

Step 1: In Chrome DevTools, open the Network tab and reload the page.

Step 2: Find the HTML document request.

Step 3: Look at the resource size, not the transferred size.

Step 4: Or run curl with --compressed and count the decoded bytes.

Step 5: Note that HTTP headers count toward the 2MB too. Huge Set-Cookie or Link headers add up.

Explained simply:

Servers usually send HTML compressed with gzip or Brotli, which can shrink it by 70 to 90 percent. Google decompresses it before applying the limit, because what matters is how much content there is to process, not how many bytes travelled over the network. Your DevTools 'transferred' number can therefore be very misleading.

Common mistake to avoid:

Ignoring HTTP headers. Long cookie headers, Link headers and security policies all count toward the 2MB, and some apps send many kilobytes of headers per response.

Why it matters for rankings:

A 400KB gzipped page can expand to over 2MB once decompressed. If it does, the bottom of your page, often FAQs, reviews and internal links, is silently dropped from Google's view.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/overview-google-crawlers

🎓 Learn to audit what Googlebot really sees in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Googlebot #SEO

---

## Post 28: How to place critical SEO tags early in the HTML

How to place critical SEO tags so Google always sees them

Google recommends keeping HTML lean and placing important elements higher in the document.

Step 1: Put <title> and <meta name="description"> near the top of <head>.

Step 2: Put <meta name="robots"> and <link rel="canonical"> early in <head>.

Step 3: Put hreflang <link> tags right after them.

Step 4: Place JSON-LD structured data in <head>, or early in <body>.

Step 5: Load large scripts and style blocks from external files instead of inlining them before these tags.

Step 6: Check that main content and key internal links appear early in the HTML too.

Explained simply:

If a fetch is cut off, it's always the end of the HTML that goes missing. So the order of your HTML is a priority list. Elements near the top are the safest. That's why Google suggests putting critical tags early and moving heavy code into external files, which get their own separate byte budget.

Common mistake to avoid:

Template systems that output big inline scripts, tracking snippets and style blocks at the top of <head>, before the title, canonical and robots tags.

Why it matters for rankings:

If a canonical or noindex sits after the 2MB cutoff, Google never sees it. Putting these signals early means Google always reads them, and they keep supporting your rankings.

Source: https://developers.google.com/search/blog/2026/03/crawler-blog-post

🎓 Learn HTML architecture for SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #HTML #SEO

---

## Post 29: What is the PDF crawl limit?

What is Google's PDF crawl limit?

For Google Search, Googlebot fetches the first 64MB of a PDF, compared with 2MB for HTML.

How to optimize PDFs for crawling:

Step 1: Keep PDFs well under 64MB. Compress images inside them.

Step 2: Use real text, not scanned images, so the content can be extracted.

Step 3: Give each PDF a meaningful title in its document properties.

Step 4: Link to PDFs from relevant HTML pages with a normal <a href> link.

Step 5: If an HTML version exists, send a canonical HTTP header from the PDF:
Link: <https://example.com/guide>; rel="canonical"

Explained simply:

PDFs often contain valuable content like manuals, research and price lists, and Google can index and rank them. Because PDFs are naturally large, Google gives them a much bigger limit than HTML. The text inside must be selectable, though: a scanned image of text gives Google very little to work with.

Common mistake to avoid:

Publishing the same content as both an HTML page and a PDF with no canonical. The PDF sometimes ranks instead of the page, and PDFs usually convert worse.

Why it matters for rankings:

PDFs can rank, but duplicate PDF and HTML versions split your signals. A header canonical consolidates them onto the page you want to rank.

Source: https://developers.google.com/search/blog/2026/03/crawler-blog-post

🎓 Learn non-HTML SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#PDF #TechnicalSEO #SEO

---

## Post 30: What is the 15MB default limit?

What is the 15MB limit?

Googlebot for Search has its own limits: 2MB for HTML and 64MB for PDFs.

For other Google crawlers that don't specify a limit, the default is 15MB, whatever the content type.

How to use this knowledge:

Step 1: Don't confuse the two numbers. The old "15MB" guidance isn't the Google Search HTML limit.

Step 2: Optimize HTML against the 2MB Search limit.

Step 3: Remember that each CSS and JS file has its own limit, separate from the HTML's.

Step 4: Watch out for huge JS bundles. A 3MB bundle may be cut off, so the page may not render fully.

Step 5: Split bundles and use code splitting for big apps.

Explained simply:

Different Google crawlers serve different products, so their limits can differ. The 15MB default applies when a crawler doesn't specify its own. Google Search's Googlebot uses 2MB for HTML and 64MB for PDFs. Each subresource (CSS, JS) is fetched separately and has its own limit, so the parent page's size doesn't include them.

Common mistake to avoid:

Reading an old article that says '15MB' and concluding your 4MB HTML page is fine for Google Search. For Search HTML, it isn't.

Why it matters for rankings:

A JS bundle that's cut off can mean a page that doesn't render properly. A page that doesn't render properly can't show its content, so it can't rank.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/overview-google-crawlers

🎓 Learn JS and crawl limits in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #JavaScriptSEO #SEO

---

## Post 31: How does Googlebot use HTTP/2?

Does Googlebot crawl over HTTP/2?

Yes. Google's crawlers support HTTP/1.1 and HTTP/2. HTTP/1.1 is the default, and Google may switch to HTTP/2 when it's useful.

Google notes that HTTP/2 crawling may save computing resources such as CPU and RAM, for both your site and Googlebot.

How to enable it:

Step 1: Check whether your server or CDN supports HTTP/2. Most modern CDNs do.

Step 2: Enable it over HTTPS.

Step 3: Confirm with: curl -I --http2 https://yourdomain.com

Step 4: Watch Crawl Stats for any changes in response time.

Step 5: If HTTP/2 causes problems, you can opt out of HTTP/2 crawling by returning a 421 status code to it.

Explained simply:

HTTP/2 can send many requests over a single connection instead of opening several. For a crawler fetching many URLs from your server, that means less connection overhead on both sides. Google decides when to crawl over HTTP/2, and HTTP/2 crawling itself isn't a ranking factor. The benefit is efficiency.

Common mistake to avoid:

Expecting HTTP/2 alone to boost rankings. It doesn't. It's a crawl efficiency improvement, so the gain shows up as smoother, cheaper crawling, not a ranking jump.

Why it matters for rankings:

More efficient connections can mean more crawling within the same server capacity, so new and updated pages get discovered faster.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/overview-google-crawlers

🎓 Learn server-level SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#HTTP2 #TechnicalSEO #WebPerformance

---

## Post 32: How does compression affect crawling?

How does compression affect Googlebot?

Google's crawlers support these encodings:
→ gzip
→ deflate
→ Brotli (br)

How to set up compression for crawlers:

Step 1: Enable Brotli or gzip for HTML, CSS, JS, JSON and XML (including sitemaps).

Step 2: Check the response header:
curl -I -H "Accept-Encoding: br,gzip" URL
Look for Content-Encoding: br

Step 3: Remember that compression speeds up transfer but doesn't increase the 2MB limit. The limit applies to uncompressed bytes.

Step 4: Reduce the actual HTML size too.

Explained simply:

Compression shrinks text-based files before they travel over the network. Brotli usually compresses smaller than gzip, and both are supported by Google's crawlers. Smaller transfers mean faster responses, and Google adjusts how much it crawls based on how quickly and reliably your server responds.

Common mistake to avoid:

Compressing HTML but not XML sitemaps, JSON APIs or CSS. Crawlers and the renderer fetch all of these, so every uncompressed file slows things down.

Why it matters for rankings:

Compression cuts download time. Faster responses can raise how much Google is willing to crawl and improve user metrics like LCP. Both help your pages stay fresh and competitive.

Source: https://developers.google.com/crawling/docs/crawlers-fetchers/overview-google-crawlers

🎓 Learn performance and crawl tuning in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #WebPerformance #SEO

---

## Post 33: What does "Googlebot is stateless" mean?

What does it mean that Googlebot is stateless?

Google's Web Rendering Service doesn't keep state between page loads. These are cleared across page loads:
→ Cookies
→ Local Storage
→ Session Storage

How to make content work for a stateless crawler:

Step 1: Never require a cookie to show the main content.

Step 2: Don't hide content behind consent or location gates that need stored choices.

Step 3: Don't rely on a previous page visit to load the next page's data.

Step 4: Test in a fresh incognito window with storage disabled.

Step 5: Use URL Inspection to confirm what Google renders.

Explained simply:

Each time Google renders a page, it's like a brand-new visitor in a fresh private window. There's no login, no saved preferences and no memory of a previous page. Anything your site stores in cookies or browser storage to change what's shown won't be there, so Google sees the 'first visit' version every time.

Common mistake to avoid:

Showing different main content to new and returning visitors, such as a full-page signup gate for first-timers. Google always sees the first-timer version.

Why it matters for rankings:

If content appears only for returning, cookied users, Googlebot sees an empty or different page. Content Google can't see can't help you rank.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/fix-search-javascript

🎓 Learn JavaScript SEO debugging in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #TechnicalSEO #SEO

---

## Post 34: How CDNs and firewalls can block Googlebot

How your CDN or firewall can quietly block Googlebot

CDNs help crawling: fast edge responses can let Google crawl more.

But bot-protection features (JS challenges, CAPTCHAs, aggressive rate limits) can block crawling if they're served to Googlebot.

How to check your setup:

Step 1: Filter CDN or WAF logs for verified Googlebot IPs.

Step 2: Look for challenge pages, 403s and blocked requests.

Step 3: Allowlist verified Google crawler IP ranges, using the new JSON files.

Step 4: Run URL Inspection → Test Live URL to confirm a clean 200.

Step 5: Re-check after every security rule change.

Explained simply:

Bot protection is built to stop automated traffic, and Googlebot is automated traffic. A JavaScript challenge or CAPTCHA that a human solves in a second stops a crawler completely. Googlebot then receives the challenge page instead of your content, which can look like an error, or like an empty page.

Common mistake to avoid:

Turning on a new 'block bots' feature during a traffic spike and forgetting about it. Weeks later, rankings fall and nobody connects it to the security change.

Why it matters for rankings:

If Googlebot hits a challenge page, it can't crawl your content. Sites have lost visibility after enabling "bot fight" style protection without allowlisting search crawlers.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-cdns

🎓 Learn CDN-safe SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CDN #TechnicalSEO #Googlebot

---

## Post 35: What are HTTP status codes to Google?

What do HTTP status codes mean to Google?

Every crawl ends with a status code from your server. That three-digit number tells Google what to do next.

Step 1: 2xx (success). The content may be considered for indexing.

Step 2: 3xx (redirect). Google follows up to 10 hops and considers the final URL.

Step 3: 4xx (client error). Not indexed. Already-indexed URLs are eventually dropped. Crawl rate isn't reduced (except for 429).

Step 4: 5xx and 429 (server error or overload). Google slows down crawling. Indexed URLs are kept for a while, then dropped if the errors continue.

How to audit yours:

→ Crawl your site with an SEO crawler.
→ Compare the results with your server logs.
→ Fix any important URL that isn't returning 200.

Explained simply:

Your server's status code is the very first thing Google reads in every response, before any content. It decides whether the content is even considered. A good page with the wrong code can be ignored, while a missing page with a 200 can waste crawling. Getting codes right is basic hygiene with a big impact.

Common mistake to avoid:

Only checking status codes in a browser. Browsers hide redirects and caches. Use a crawler or curl to see exactly what Googlebot gets.

Why it matters for rankings:

Status codes decide whether a page can be in the index at all. Wrong codes quietly remove pages from search.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Master status codes in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#HTTPStatusCodes #TechnicalSEO #SEO

---

## Post 36: Does a 200 status mean a page will be indexed?

Does a 200 status code mean your page will be indexed?

No. A 200 means Google got the content. Indexing is a separate decision.

With a 200:
→ The page goes into the render queue, unless a noindex tells Google otherwise
→ The content is evaluated
→ Google decides whether to index it

How to move from 200 to indexed:

Step 1: Check the URL in Search Console with URL Inspection.

Step 2: If it shows "Crawled – currently not indexed", improve its quality and uniqueness.

Step 3: Make sure the page isn't a duplicate of another URL.

Step 4: Add internal links to it from relevant, strong pages.

Step 5: Make sure the main content is in the HTML or renders reliably.

Explained simply:

Crawling, rendering and indexing are separate decisions. A 200 status only gets you through the first one. Google then decides whether the page adds enough unique value to keep in its index. That's why Search Console has two separate statuses: 'Discovered' (not crawled yet) and 'Crawled – currently not indexed' (crawled, but not kept).

Common mistake to avoid:

Repeatedly requesting indexing for 'Crawled – currently not indexed' pages without changing anything. The page needs to be improved, not resubmitted.

Why it matters for rankings:

A 200 is the minimum requirement. To get indexed and rank, the page also needs unique value and clear signals.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Learn to diagnose indexing issues in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Indexing #TechnicalSEO #SEO

---

## Post 37: 301 vs 302 redirects

301 vs 302: which redirect should you use?

Google follows both, but treats them differently:

→ 301 (permanent): a strong signal that the target should be the canonical URL
→ 302 (temporary): a weak signal that the target should be canonical

How to choose:

Step 1: Is the move permanent, like a migration, a URL change or merged content? Use 301 (or 308).

Step 2: Is it temporary, like an A/B test, a short promotion or maintenance? Use 302 (or 307).

Step 3: Update internal links to point straight at the final URL.

Step 4: Update your canonical tags and sitemap to match.

Step 5: Keep permanent redirects live for at least a year.

Explained simply:

Both codes send users to the new URL, but they tell Google different things. A 301 says 'this has moved for good, use the new URL'. A 302 says 'this is temporary, the old URL is still the real one'. Google uses that to decide which URL to show in results and where to consolidate ranking signals.

Common mistake to avoid:

Using 302 for a permanent change because it was the framework's default. Google may keep the old URL indexed for longer and be slower to consolidate signals.

Why it matters for rankings:

The wrong redirect type can leave Google indexing the old URL, or splitting signals between two URLs. The right one sends ranking signals to the URL you want.

Source: https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

🎓 Learn redirect strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Redirects #TechnicalSEO #SEO

---

## Post 38: What are 307 and 308 redirects?

What are 307 and 308 redirects, and how does Google treat them?

→ 308: permanent. Google treats it like a 301, a strong canonical signal.
→ 307: temporary. Google treats it like a 302, a weak canonical signal.

The difference from 301 and 302 is technical: 307 and 308 keep the HTTP method (POST stays POST).

How to use them:

Step 1: Check what your framework or CDN sends by default. Some send 307 or 308 automatically.

Step 2: For a permanent move, make sure you're sending 301 or 308, not 307.

Step 3: Watch for HSTS. Browsers show an "internal 307" that never reaches Googlebot.

Step 4: Check the real server response with curl -I, not just browser DevTools.

Explained simply:

307 and 308 were added to HTTP to fix an old ambiguity: with 301 and 302, some clients changed POST requests into GET. 307 and 308 guarantee the method stays the same. For Google Search, what matters is permanent versus temporary: 308 is treated like 301, and 307 like 302.

Common mistake to avoid:

Misreading Chrome DevTools: an HSTS 'internal redirect' appears as a 307, but your server never sent it. Always check the real server response with curl.

Why it matters for rankings:

If a permanent move goes live as a 307, Google may keep the old URL as canonical, which can slow the transfer of ranking signals to the new URL.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Learn redirect auditing in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Redirects #TechnicalSEO #SEO

---

## Post 39: How many redirects does Googlebot follow?

How many redirects will Googlebot follow?

Googlebot follows up to 10 redirect hops. After that, Search Console shows a "Redirect error" in the Page Indexing report.

Content on the intermediate redirecting URLs is ignored. Only the final URL is considered.

How to fix redirect chains:

Step 1: Crawl your site and export every redirect chain.

Step 2: Find chains of 2 or more hops, like http → https → www → trailing slash.

Step 3: Point the first URL straight at the final destination.

Step 4: Update internal links to the final URL so no redirect is needed.

Step 5: Check for and fix redirect loops.

Explained simply:

Every redirect hop is a separate HTTP request with its own latency and its own chance of failing. Chains usually build up over years: an http-to-https rule, then a domain change, then a URL restructure, each added on top of the last. Googlebot gives up after 10 hops, but even 3 hops is wasteful.

Common mistake to avoid:

Fixing redirects at the server but leaving old URLs in internal links, canonicals and sitemaps, so Googlebot keeps entering the chain from the start.

Why it matters for rankings:

Every hop costs crawl time and adds a point where something can fail. Single-hop redirects get users and Googlebot to the content faster and keep signals clean.

Source: https://developers.google.com/search/docs/crawling-indexing/http-network-errors

🎓 Learn to clean up redirects at scale in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Redirects #CrawlBudget #TechnicalSEO

---

## Post 40: 404 vs 410: what's the difference for Google?

404 vs 410: does it matter which one you use?

Both are 4xx errors. For Google:
→ The content isn't indexed
→ Already-indexed URLs are eventually dropped from the index
→ Crawl rate isn't reduced

In practice, both remove the page. A 410 ("Gone") states more clearly that the removal is intentional.

How to handle removed pages:

Step 1: Is there a close replacement page? Use a 301 to it.

Step 2: No replacement? Return 404 or 410.

Step 3: Don't redirect every dead page to the homepage. Google may treat that as a soft 404.

Step 4: Remove internal links to the dead URLs.

Step 5: Remove them from your XML sitemap.

Explained simply:

4xx codes mean the client asked for something that isn't there. Google's response is to stop showing the URL in results over time. Unlike 5xx errors, 404s don't make Google crawl less, because they aren't a sign your server is struggling. Having some 404s is completely normal and won't hurt the rest of your site.

Common mistake to avoid:

Panicking about 404s in Search Console and redirecting all of them to the homepage. That creates soft 404s and confuses both users and Google.

Why it matters for rankings:

Clean 404s and 410s are healthy. They tell Google to stop spending crawls on pages that no longer exist, so more crawling goes to pages that do.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Learn content pruning the technical way in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#404 #TechnicalSEO #SEO

---

## Post 41: What is a soft 404?

What is a soft 404?

A soft 404 is a page that says "not found" (or is basically empty) but returns a 200 OK status.

Google detects these from the content and reports them as "Soft 404" in Search Console's Page Indexing report. They aren't indexed.

How to find and fix soft 404s:

Step 1: Open Search Console → Pages → filter for "Soft 404".

Step 2: Open a sample of the affected URLs.

Step 3: If the page really doesn't exist, return a real 404 or 410.

Step 4: If it should exist, add real, unique main content.

Step 5: For empty category or search pages, return 404 or add noindex.

Step 6: Stop redirecting dead pages to the homepage.

Explained simply:

Google doesn't only trust your status code; it also looks at the content. If a page says 'product not found', has almost no content, or looks like an error template, Google may label it a soft 404 even with a 200 status. This protects search results from empty pages, and it means your codes should match reality.

Common mistake to avoid:

Out-of-stock product pages that remove all content and show only 'unavailable'. Keep useful content (specs, alternatives) or return a 404 if it's gone for good.

Why it matters for rankings:

Soft 404s keep getting crawled and waste crawl activity. Pages that look empty to Google won't rank, even if they look fine to you.

Source: https://developers.google.com/search/docs/crawling-indexing/troubleshoot-crawling-errors

🎓 Learn to clean up the index in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Soft404 #TechnicalSEO #SEO

---

## Post 42: What happens when you return 204 or an empty page?

What happens when your server returns 204 or an empty page?

A 204 (No Content) or an empty 200 means Google gets no content. Google will likely treat the URL as a soft 404, so it won't be indexed.

How to catch empty responses:

Step 1: Crawl your site and flag pages with very low word counts or tiny HTML size.

Step 2: Check whether your API or CMS ever returns empty templates while still sending a 200.

Step 3: Fix application errors so they return 5xx, not empty 200s.

Step 4: Use URL Inspection to see what Googlebot actually received.

Step 5: Set up alerts for spikes in tiny or zero-byte responses.

Explained simply:

A 204 literally means 'success, but no content'. For a search engine, a page with no content has nothing to index. Empty 200s often come from backend failures: an API call times out, the template renders with no data, but the server still reports success. Google sees an empty page and may treat it as a soft 404.

Common mistake to avoid:

Error handling that catches exceptions and renders a blank template with a 200 status. It should return a 5xx so Google retries later instead of indexing nothing.

Why it matters for rankings:

Intermittent empty responses can drop good pages out of the index. A temporary backend error that ends up indexed as "nothing" can cost you rankings for weeks.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Learn reliability-first SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Indexing #SEO

---

## Post 43: How 401 and 403 affect Google

How do 401 and 403 errors affect Google?

For Google, 401 (Unauthorized) and 403 (Forbidden) are 4xx errors:
→ The content isn't indexed
→ Already-indexed URLs are eventually dropped from the index
→ They don't slow down crawling

The risk: a firewall that returns 403 to Googlebot by mistake.

How to audit for accidental 403s:

Step 1: Filter your logs for verified Googlebot requests that got a 403.

Step 2: Compare them with what normal users receive for the same URLs.

Step 3: Check geo-blocking. Googlebot crawls mostly from US IP addresses.

Step 4: Check bot rules that are based on the user agent.

Step 5: Use 401 or 403 only for content that really should be private.

Explained simply:

401 means authentication is required, and 403 means access is refused. Both tell Google it isn't allowed to see the content, so the URL won't be indexed. That's correct for private areas. The risk is accidental 403s caused by geo-blocking, firewall rules or hotlink protection catching Googlebot by mistake.

Common mistake to avoid:

Blocking traffic from outside your country. Googlebot crawls mostly from US IP addresses, so country blocking can lock it out of your whole site.

Why it matters for rankings:

A firewall rule that wrongly sends 403s to Googlebot can slowly remove your pages from Google's index without any obvious error.

Source: https://developers.google.com/crawling/docs/troubleshooting/http-status-codes

🎓 Learn to debug access issues in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #Googlebot #SEO

---

## Post 44: What is a 429 status code for SEO?

What does a 429 status code do to your SEO?

429 means "Too Many Requests". Google treats it as a sign that your server is overloaded, so it's handled like a server error:
→ Googlebot slows down crawling
→ Indexed URLs are kept for a while
→ They're eventually dropped if the 429s continue

How to use 429 correctly:

Step 1: Use it only for short-term overload protection.

Step 2: Make sure your rate limiter doesn't trigger on normal Googlebot crawl rates.

Step 3: Allowlist verified Googlebot IPs in aggressive rate limiters.

Step 4: Watch Crawl Stats for 429 spikes.

Step 5: Fix the capacity problem behind it instead of rate limiting permanently.

Explained simply:

429 is how a server says 'slow down'. Google respects it: it reduces crawling to protect your server. That's helpful in an emergency. But because Google treats 429 as a server error, a long period of 429s eventually leads Google to drop the affected URLs from its index, as with 5xx errors.

Common mistake to avoid:

Rate limiters with thresholds tuned for human browsing. Googlebot crawls in parallel, so normal crawl rates can trip a 'requests per second' rule designed for people.

Why it matters for rankings:

429 is a valid emergency brake. If it stays on, it cuts crawling and can eventually remove URLs from Google's index.

Source: https://developers.google.com/search/docs/crawling-indexing/http-network-errors

🎓 Learn crawl rate management in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #TechnicalSEO #SEO

---

## Post 45: What do 5xx errors do to your rankings?

What do 5xx server errors do to your rankings?

When Googlebot gets 500, 502 or 503:
→ Crawling slows down
→ Content from that response is ignored
→ Already-indexed URLs are kept for a while
→ They're eventually dropped from the index if the errors continue

How to stop 5xx errors from hurting your visibility:

Step 1: Open Search Console → Settings → Crawl stats → By response.

Step 2: Check the trend in the "Server error (5xx)" share.

Step 3: Match the spikes with deployments, traffic peaks or backend outages.

Step 4: Fix the root cause, whether that's capacity, timeouts or failing dependencies.

Step 5: Set up uptime monitoring on your key templates, not just the homepage.

Explained simply:

A 5xx says the server failed, not that the page is gone. Google gives you time: it keeps the indexed version and retries. But it also crawls less, to avoid making the problem worse. If errors last long enough, Google concludes the URLs aren't reliably available and drops them from the index.

Common mistake to avoid:

Monitoring only the homepage. Category, search and product templates often fail under load while the homepage, served from cache, looks perfectly healthy.

Why it matters for rankings:

Short 5xx spikes slow crawling. Long-running 5xx errors remove pages from Google's index, and that costs you rankings.

Source: https://developers.google.com/search/docs/crawling-indexing/http-network-errors

🎓 Learn infrastructure SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#ServerErrors #TechnicalSEO #SEO

---

## Post 46: How to handle site maintenance with 503

How to take your site down for maintenance without hurting SEO

Use a 503 Service Unavailable response, not a 200 maintenance page.

Step 1: Configure your maintenance mode to return HTTP 503.

Step 2: Optionally add a Retry-After header, for example Retry-After: 3600.

Step 3: Don't change robots.txt to "Disallow: /" during maintenance, and never serve a maintenance page in place of robots.txt.

Step 4: Keep maintenance as short as possible, ideally hours, not days.

Step 5: Afterwards, confirm key URLs return 200 again.

Step 6: Watch Crawl Stats to see crawling recover.

Explained simply:

503 means 'temporarily unavailable', which is exactly what maintenance is. It tells Google not to treat the current response as the real content, and to try again later. A maintenance page with a 200 status says the opposite: 'this is the content of this URL now'. Google may index it.

Common mistake to avoid:

Planned maintenance that runs for days. A short 503 is safe, but returning it for a long time leads to crawl slowdowns, and eventually URLs dropping from the index.

Why it matters for rankings:

A 200 maintenance page can get indexed in place of your real content. A short 503 tells Google to come back later, which protects your existing rankings.

Source: https://developers.google.com/search/docs/crawling-indexing/http-network-errors

🎓 Learn release and maintenance playbooks in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #SiteMaintenance #SEO

---

## Post 47: How network and DNS errors affect crawling

How do network and DNS errors affect Google crawling?

Google treats network timeouts, connection resets and DNS errors similarly to 5xx errors:
→ Crawling slows down immediately
→ No content is received
→ Long-running problems can cause pages to drop out of the index

How to diagnose them:

Step 1: Open Crawl Stats → Host status. Check DNS resolution and server connectivity.

Step 2: Test DNS from several locations.

Step 3: Check your DNS provider's uptime and TTL settings.

Step 4: Check the server's connection limits and firewall drops.

Step 5: Look at timeouts. Slow backends can show up as network errors.

Explained simply:

Before any HTTP request, Googlebot has to look up your domain in DNS and open a connection to your server. If either step fails, there's no response at all, not even an error code. Google reads that as a sign the server can't cope, so it slows down crawling right away to avoid adding load.

Common mistake to avoid:

Moving DNS providers or changing nameservers without lowering TTLs first. Propagation problems can leave some resolvers, including Google's, failing to resolve your domain.

Why it matters for rankings:

If Google can't reach your server, it can't crawl anything. DNS problems can affect your whole site at once.

Source: https://developers.google.com/crawling/docs/troubleshooting/dns-network-errors

🎓 Learn host health diagnostics in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#DNS #TechnicalSEO #SEO

---

## Post 48: How to fix "Redirect error" in Search Console

How to fix "Redirect error" in Search Console

This status appears in the Page Indexing report when Google can't complete a redirect.

Common causes:
→ Chains longer than 10 hops
→ Redirect loops
→ Redirects to an empty or bad URL
→ URLs that exceed the maximum URL length

How to fix it:

Step 1: Export the affected URLs from Search Console.

Step 2: Trace each one with curl -IL to see every hop.

Step 3: Find any loop, such as A → B → A.

Step 4: Replace chains with a single hop to the final URL.

Step 5: Fix conflicting rules, for example CDN and server both forcing different trailing-slash or www rules.

Step 6: Click "Validate fix" in Search Console.

Explained simply:

Search Console groups several redirect problems under one label. The report tells you something went wrong, not exactly what, so you have to trace each URL yourself. Most cases come down to two systems (for example the CDN and the application) applying conflicting rules, so each sends the request back to the other.

Common mistake to avoid:

Fixing a redirect loop in the app but not in the CDN's page rules, so the CDN still sends the request back into the loop.

Why it matters for rankings:

URLs with redirect errors can't be indexed, and ranking signals pointing at them don't reach your real pages.

Source: https://developers.google.com/search/docs/crawling-indexing/http-network-errors

🎓 Learn Search Console troubleshooting in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsole #Redirects #TechnicalSEO

---

## Post 49: What is HTTP caching for crawlers?

What is HTTP caching for crawlers?

Google's crawling infrastructure supports HTTP caching as defined in the HTTP caching standard (RFC 9111), using:
→ ETag (response) + If-None-Match (request)
→ Last-Modified (response) + If-Modified-Since (request)

How it works:

Step 1: Googlebot fetches a page, and your server sends an ETag.

Step 2: On the next crawl, Googlebot sends that ETag back in If-None-Match.

Step 3: If nothing changed, your server replies 304 Not Modified with no body.

Step 4: Google knows the content is the same and doesn't reprocess it.

Explained simply:

Every time Googlebot recrawls an unchanged page and downloads it in full, both sides waste resources. HTTP caching lets the crawler ask 'has this changed since my last copy?' instead. If it hasn't, the server answers in a few bytes, Google skips the processing, and both sides save effort for pages that did change.

Common mistake to avoid:

Assuming your CDN handles this automatically. Many setups strip ETag headers or ignore conditional requests, so check the actual responses.

Why it matters for rankings:

Fewer full downloads leave more crawling capacity for new and updated pages, so your fresh content gets crawled and indexed faster.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-caching

🎓 Learn HTTP caching for SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#HTTPCaching #CrawlBudget #TechnicalSEO

---

## Post 50: How to implement ETags for Googlebot

How to set up ETags for Googlebot

Google recommends ETag over Last-Modified, because ETag doesn't have date-formatting problems.

Step 1: Generate the ETag from a hash of the page's main content, for example ETag: "a1b2c3".

Step 2: Exclude parts that change on every request, like ads, timestamps and CSRF tokens, from the hash.

Step 3: When a request includes If-None-Match, compare it with the current ETag.

Step 4: If they match, return 304 Not Modified with an empty body.

Step 5: If they differ, return 200 with the new content and the new ETag.

Step 6: Test:
curl -I -H 'If-None-Match: "a1b2c3"' URL

Explained simply:

An ETag is a fingerprint of a version of a page. If the content is the same, the fingerprint is the same. Google prefers ETags because they are simple strings compared exactly, while Last-Modified relies on correctly formatted dates. The key is generating the ETag from the content that matters, not the whole raw HTML.

Common mistake to avoid:

ETags that differ between servers behind a load balancer for the same content. Every request then looks 'changed', so 304s never happen.

Why it matters for rankings:

A stable ETag lets Google skip unchanged pages and spend its crawling on content that changed. On large sites, that means faster pickup of price, stock and content updates.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-caching

🎓 Build crawl-efficient servers with us in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#ETag #TechnicalSEO #CrawlBudget

---

## Post 51: How to use Last-Modified correctly

How to use the Last-Modified header correctly

Google's crawlers support Last-Modified with If-Modified-Since, exactly as defined in the HTTP caching standard.

Step 1: Send Last-Modified in HTTP date format:
Last-Modified: Mon, 05 Oct 2026 10:00:00 GMT

Step 2: Update it only when the main content actually changes.

Step 3: When a request includes If-Modified-Since, compare the dates.

Step 4: If nothing has changed since then, return 304 with an empty body.

Step 5: Don't set Last-Modified to "now" on every request. That defeats the point.

Step 6: Prefer ETag where you can. It's less error-prone.

Explained simply:

Last-Modified records when a page last changed. When Googlebot sends If-Modified-Since with a date, your server compares it with the page's real change date. If nothing changed after that date, a 304 saves the full download. It only works if the date reflects real content changes, not every time the page is generated.

Common mistake to avoid:

Frameworks that set Last-Modified to the current time on every request. Every page then looks freshly changed, which makes the header useless for crawlers.

Why it matters for rankings:

Accurate freshness signals help Google spend crawling on what changed. Fake "always new" dates waste crawling and make your freshness signals less trustworthy.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-caching

🎓 Learn freshness signals in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #HTTPCaching #SEO

---

## Post 52: What is a 304 Not Modified?

What is a 304 Not Modified response?

A 304 tells a crawler: "This hasn't changed since your last visit, so reuse your copy."

When Google's crawlers receive a 304, they signal to the next processing system that the content is the same as at the last crawl.

How to check whether your site supports 304s:

Step 1: Fetch a page and note its ETag or Last-Modified header.

Step 2: Request it again with If-None-Match or If-Modified-Since set to that value.

Step 3: Confirm the response is 304 with an empty body.

Step 4: Check your CDN. Some CDNs strip validators or always return 200.

Step 5: Check Crawl Stats by response to see your share of 304s.

Explained simply:

A 304 response has no body, just headers. It's one of the cheapest responses a server can send. For Google, it confirms the stored copy is still current, so the page doesn't need to be processed again. On large sites, the share of 304s in Crawl Stats is a simple measure of how efficient your crawling is.

Common mistake to avoid:

Returning 304 for content that actually changed, because the validator ignores parts of the page that matter (like price). Google then keeps showing outdated information.

Why it matters for rankings:

Every 304 is a crawl that cost almost nothing. On large sites, that saved capacity goes toward discovering and indexing new pages.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-caching

🎓 Learn crawl efficiency engineering in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#304 #TechnicalSEO #CrawlBudget

---

## Post 53: What is crawl budget?

What is crawl budget?

Crawl budget is the amount of crawling resources Google gives a site. It depends on two things:

1. Crawl capacity limit: how much crawling your server can handle
2. Crawl demand: how much Google wants to crawl your URLs

How to check whether you have a crawl budget problem:

Step 1: Compare the number of URLs on your site with daily Googlebot requests in Crawl Stats.

Step 2: Look at "Discovered – currently not indexed" in the Page Indexing report.

Step 3: Check how long new pages take to get crawled.

Step 4: Check your logs for crawling wasted on parameters, duplicates and redirects.

Explained simply:

Google can't crawl every URL on the web all the time, so it rations. Your crawl budget is how much crawling Google is willing and able to do on your site. Willing depends on how valuable and fresh your URLs seem. Able depends on how much load your server can handle without slowing down.

Common mistake to avoid:

Trying to 'increase crawl budget' by adding more URLs to the sitemap. More low-value URLs usually spread the same crawling more thinly.

Why it matters for rankings:

If Google can't crawl your important pages often enough, new content shows up late and updates (prices, stock, content refreshes) take longer to show in search.

Source: https://developers.google.com/crawling/docs/crawl-budget

🎓 Master crawl budget in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #TechnicalSEO #SEO

---

## Post 54: What is the crawl capacity limit?

What is the crawl capacity limit?

Google calculates a crawl capacity limit, also called hostload. It limits the total time your server spends holding connections open for Google, counting both the number of parallel connections and how long they last.

It goes up when your site responds quickly and consistently. It goes down when the site slows, returns 5xx errors, or sends 429s.

How to raise your crawl capacity:

Step 1: Reduce server response time (TTFB) on your key templates.

Step 2: Remove sources of 5xx errors and timeouts.

Step 3: Serve cacheable pages from a CDN.

Step 4: Support 304 responses so repeat crawls cost less.

Step 5: Avoid rate limiting verified Googlebot.

Explained simply:

Google doesn't want its crawling to slow your site down for real users. So it constantly measures your server's responses and adjusts. Fast, stable responses tell Google it can crawl more without causing harm. Slowdowns and errors tell it to back off. This happens automatically and keeps changing over time.

Common mistake to avoid:

Optimising only front-end performance (like images) while server response time stays slow. Crawl capacity reacts to how fast the server responds.

Why it matters for rankings:

A faster, more stable server means Google can safely crawl more. More crawling means faster indexing of the pages that drive revenue.

Source: https://developers.google.com/crawling/docs/crawl-budget

🎓 Learn server-side SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #TechnicalSEO #WebPerformance

---

## Post 55: What is crawl demand?

What is crawl demand?

Crawl demand is how much Google wants to crawl your site. It depends on:
→ Site size
→ How often the site is updated
→ Page quality
→ Relevance compared with other sites

Google says duplicate and unwanted URLs waste a lot of crawl time, and that's the factor you can control most.

How to improve crawl demand:

Step 1: Consolidate duplicates with canonicals and redirects.

Step 2: Remove or noindex thin, low-value pages.

Step 3: Keep content fresh and update important pages meaningfully.

Step 4: Link to priority pages from your strongest pages.

Step 5: Keep your sitemaps clean: canonical, 200-status URLs only.

Explained simply:

Even if your server could handle more crawling, Google only crawls what it thinks is worth crawling. Popular pages and pages that change often get recrawled more. Large numbers of near-duplicate URLs make your site look less valuable to crawl, and spread Google's attention thinly across pages that will never rank.

Common mistake to avoid:

Auto-generating thousands of thin pages (tag pages, empty location pages) to 'cover more keywords'. They dilute crawl demand for your strong pages.

Why it matters for rankings:

When Google sees a site full of high-quality, unique pages, it crawls that site more. When it sees a site full of duplicates, it crawls less.

Source: https://developers.google.com/crawling/docs/crawl-budget

🎓 Learn to grow crawl demand in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #TechnicalSEO #SEO

---

## Post 56: Does your site need to worry about crawl budget?

Does your site need to worry about crawl budget?

Google's guidance says crawl budget mainly matters for:
→ Large sites (1 million+ unique pages) whose content changes moderately often (about weekly)
→ Medium or large sites (10,000+ unique pages) whose content changes very quickly (daily)
→ Sites with many URLs stuck in "Discovered – currently not indexed"

How to decide for your site:

Step 1: Count your unique, indexable URLs.

Step 2: Estimate how often they change.

Step 3: Check Search Console for many "Discovered – currently not indexed" URLs.

Step 4: If none of these apply, focus on content and links instead.

Step 5: If they do apply, start log analysis and URL cleanup.

Explained simply:

Crawl budget is a real constraint, but only at scale. For most small and medium sites, Google crawls all the important pages comfortably. Focusing on crawl budget too early pulls effort away from content quality and links, which matter far more for small sites. The threshold is about size and how often content changes.

Common mistake to avoid:

Small sites using noindex, robots.txt and nofollow everywhere to 'save crawl budget'. This can do more harm than good when budget was never the problem.

Why it matters for rankings:

For a 200-page site, crawl budget is rarely the bottleneck. For a 2-million-URL store, it can be what decides whether new products rank this week or next month.

Source: https://developers.google.com/crawling/docs/crawl-budget

🎓 Learn enterprise SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #EnterpriseSEO #TechnicalSEO

---

## Post 57: What is faceted navigation and why is it a crawl trap?

What is faceted navigation, and why is it a crawl trap?

Faceted navigation lets users filter by color, size, price and more. Usually each filter adds URL parameters, which can create an almost infinite number of URLs.

Google says this leads to overcrawling, and slows discovery of important new content.

How to control it:

Step 1: Decide which filter combinations deserve to be indexed, for example "red running shoes".

Step 2: Block non-valuable filter combinations in robots.txt.

Step 3: Or handle those filters with URL fragments (#), which Google generally ignores.

Step 4: Return 404 for filter combinations with no results.

Step 5: Use a consistent parameter order and the standard & separator.

Explained simply:

Each filter (colour, size, brand, price) multiplies with the others. Five filters with ten options each can produce millions of URL combinations, almost all showing near-identical product lists. Googlebot can't tell which ones matter unless you say so, so it may spend most of its time crawling filter pages.

Common mistake to avoid:

Using nofollow on filter links and expecting that to stop crawling. Google can still discover those URLs from other sources. robots.txt or fragments are more reliable.

Why it matters for rankings:

Controlling facets moves crawling to category and product pages that can rank, instead of millions of near-duplicate filter URLs.

Source: https://developers.google.com/crawling/docs/faceted-navigation

🎓 Learn ecommerce crawl control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#FacetedNavigation #EcommerceSEO #TechnicalSEO

---

## Post 58: How to structure URL parameters for crawling

How to structure URL parameters so Google can crawl efficiently

Google's guidance:

Step 1: Use the standard ?key=value format.

Step 2: Use & to separate parameters. Avoid commas, semicolons and brackets.

Step 3: Use as few parameters as you can.

Step 4: Keep the parameter order consistent, so ?color=red&size=9 never also appears as ?size=9&color=red.

Step 5: Don't put session IDs or timestamps in URLs.

Step 6: Don't use #fragments to load different main content. Google generally doesn't support fragments for that.

Step 7: Use hyphens, not underscores, to separate words in URL paths.

Explained simply:

Google tries to understand URL parameters automatically: which change the content, and which only track or sort. Standard formatting makes that much easier. Non-standard separators or random parameter order create many URLs for the same content, which wastes crawling and splits signals across duplicates.

Common mistake to avoid:

Adding tracking parameters (utm_ and similar) to internal links. Every click path creates new URLs for the same page that Google can crawl.

Why it matters for rankings:

Clean, predictable URLs reduce duplicates, focus crawling, and make it easier for Google to consolidate signals onto one URL per page.

Source: https://developers.google.com/search/docs/crawling-indexing/url-structure

🎓 Learn URL architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#URLStructure #TechnicalSEO #SEO

---

## Post 59: How to do pagination for SEO

How to set up pagination so Google can crawl and index it

Google treats each page in a paginated series as a separate URL.

Step 1: Give each page a unique URL, for example ?page=2.

Step 2: Link the pages to each other with normal <a href> links (next, previous and page numbers).

Step 3: Link back to the first page from every page.

Step 4: Don't canonicalize page 2 and later to page 1. Each page has different items.

Step 5: Don't rely on rel="next" or rel="prev". Google no longer uses them.

Step 6: Make sure every product or article is reachable within a few clicks.

Explained simply:

Pagination is how Google reaches items deep in a list. Each page in the series is treated as its own URL with its own content. If page 2 points its canonical to page 1, you're telling Google page 2 is a duplicate, and the products linked only from page 2 and later may lose their main discovery path.

Common mistake to avoid:

Removing pagination links from the HTML and loading the next page with a JavaScript button. Google won't click it, so deep items become orphaned.

Why it matters for rankings:

Good pagination lets Googlebot reach deep products and articles. Items Google can't reach can't be indexed or rank.

Source: https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading

🎓 Learn site architecture for crawling in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Pagination #TechnicalSEO #EcommerceSEO

---

## Post 60: How to make infinite scroll SEO-friendly

How to make infinite scroll SEO-friendly

Googlebot doesn't scroll or click "Load more". If your items load only on scroll, Google may only see the first batch.

Step 1: Split the content into pages, each with its own persistent, unique URL, such as ?page=12.

Step 2: Make sure each URL always shows the same content when loaded directly.

Step 3: Use absolute page numbers, not relative ones like "next".

Step 4: Update the URL with the History API as the user scrolls.

Step 5: Add crawlable <a href> pagination links in the HTML for crawlers.

Step 6: Test with URL Inspection: can Google reach item 200?

Explained simply:

Infinite scroll is designed for people, who scroll. Googlebot doesn't scroll, so it sees whatever loads first. The fix is to back the scroll experience with real paginated URLs: users get smooth scrolling, while Google (and anyone sharing a link) gets stable URLs for each chunk of content.

Common mistake to avoid:

Using relative or session-based URLs for chunks, so the 'page 3' URL shows different items each time. Google can't index content that keeps changing per visit.

Why it matters for rankings:

Infinite scroll without paginated URLs hides deep content from Google. Paginated URLs make every item crawlable and able to rank.

Source: https://developers.google.com/search/docs/specialty/ecommerce/pagination-and-incremental-page-loading

🎓 Learn JS-heavy site SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#InfiniteScroll #JavaScriptSEO #TechnicalSEO

---

## Post 61: What is rendering in SEO?

What is rendering in SEO?

Rendering is when Google runs your page's JavaScript and CSS to see the final content, the same way a browser would.

Google processes JavaScript pages in three phases:

Step 1: Crawling. Googlebot fetches the raw HTML.

Step 2: Rendering. Once Google's resources allow, a headless Chromium runs the JavaScript.

Step 3: Indexing. Google indexes the rendered HTML and adds newly found links to the crawl queue.

How to check what Google renders:

→ Open Search Console → URL Inspection → View crawled page.
→ Compare the rendered HTML with your raw page source.
→ Look for missing content, links or structured data.

Explained simply:

Modern sites often send a minimal HTML shell and build the page in the browser using JavaScript. A crawler that only reads the raw HTML would see almost nothing. Google adds a rendering step: it runs the page in a browser engine to see the final result, then indexes that. Rendering adds time and can fail.

Common mistake to avoid:

Testing only in your own browser, which has fast hardware, cookies and no blocked resources. Google renders in a clean environment and may see something different.

Why it matters for rankings:

If your content only appears after JavaScript runs, ranking depends on rendering succeeding. Anything that fails to render is invisible to Google.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Master JavaScript SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #Rendering #TechnicalSEO

---

## Post 62: What is Google's Web Rendering Service (WRS)?

What is Google's Web Rendering Service (WRS)?

WRS is the system that renders your pages for Google Search. It:
→ Runs JavaScript in an evergreen (always up to date) Chromium
→ Fetches the CSS and JS files the page needs
→ Runs XHR and fetch requests
→ Doesn't request images or videos while rendering

How to make your pages easy for WRS:

Step 1: Allow CSS, JS and API endpoints in robots.txt.

Step 2: Keep the number of required resources low.

Step 3: Avoid JavaScript errors that stop rendering.

Step 4: Don't depend on user actions (click, scroll) to load content.

Step 5: Test with URL Inspection and check the console messages.

Explained simply:

WRS is essentially a headless Chrome that Google keeps up to date, so modern JavaScript features usually work. But it runs with constraints: it fetches only what's needed to build the page, it doesn't interact like a user, and resources blocked by robots.txt can't be loaded. Your page has to work within those limits.

Common mistake to avoid:

Blocking /api/ or /static/ paths in robots.txt. WRS then can't fetch the data or scripts the page needs, and renders an incomplete page.

Why it matters for rankings:

If WRS can't fetch a resource or runs into a JS error, your page may render half-empty, and Google may index the half-empty version.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-resources

🎓 Learn rendering diagnostics in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #WRS #TechnicalSEO

---

## Post 63: What is the render queue?

What is Google's render queue?

After crawling, Googlebot queues pages that returned 200 for rendering, unless a robots meta tag or header tells Google not to index the page.

A page may stay in this queue for a few seconds, but it can take longer.

How to reduce your dependence on the render queue:

Step 1: Put the main content in the initial server HTML (SSR or static generation).

Step 2: Put title, canonical, meta robots and structured data in the raw HTML.

Step 3: Put internal links in the raw HTML as <a href> elements.

Step 4: Use JavaScript to enhance the page, not to create its core content.

Step 5: Compare the raw HTML with the rendered HTML in URL Inspection.

Explained simply:

Crawling and rendering run as separate stages. After a page is fetched, it waits in a queue until rendering resources are available. Usually that's quick, but it adds a delay that raw HTML content doesn't have. Content in the initial HTML can be processed right away; content that needs JavaScript waits for its turn.

Common mistake to avoid:

Putting the canonical or robots tag only in JavaScript. Until rendering happens, Google sees the raw HTML values, which may be missing or say something else.

Why it matters for rankings:

Content in the raw HTML is available straight after crawling. Content that needs JavaScript has to wait for rendering. For fast-moving content like news or prices, that wait can matter.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Learn SSR vs CSR strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #Rendering #TechnicalSEO

---

## Post 64: How to make links crawlable

How to make links that Google can actually crawl

Google can only reliably crawl a link if it's an <a> element with an href attribute.

Crawlable:
<a href="/shoes/red">Red shoes</a>

Not reliably crawlable:
<span onclick="go('/shoes/red')">Red shoes</span>
<a onclick="route()">Red shoes</a>

How to fix your links:

Step 1: Crawl your site with JavaScript rendering turned off.

Step 2: List important pages with no <a href> links pointing to them.

Step 3: Replace click handlers with real <a href> elements.

Step 4: Use descriptive anchor text, not "click here".

Step 5: Make sure your SPA router still outputs real hrefs.

Explained simply:

Google discovers new pages by extracting URLs from links. It reliably reads the href attribute of <a> elements. Click handlers on other elements, or JavaScript routing without hrefs, may work fine for users but give Google no URL to follow. Navigation that looks normal to you can be a dead end for the crawler.

Common mistake to avoid:

Mega-menus built with buttons and JavaScript events instead of links. The menu works for users, but categories in it may get no crawlable internal links at all.

Why it matters for rankings:

Links are how Google discovers pages and understands how important they are. Pages without crawlable links pointing to them may never be found, even if they're in your menu.

Source: https://developers.google.com/search/docs/crawling-indexing/links-crawlable

🎓 Learn internal linking architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#InternalLinking #TechnicalSEO #SEO

---

## Post 65: How to lazy-load without hiding content from Google

How to lazy-load content without hiding it from Google

Google Search doesn't interact with your page: it doesn't scroll or click. Lazy-loaded content must load when it's visible in the viewport.

Step 1: Use native lazy loading for images: <img loading="lazy">

Step 2: For other content, use IntersectionObserver, not scroll events.

Step 3: Never require a click ("Show more") to load main content.

Step 4: Don't lazy-load content that's visible on first load, such as the LCP image.

Step 5: Test with URL Inspection and confirm the lazy-loaded text appears in the rendered HTML.

Explained simply:

Lazy loading delays content until it's needed, which speeds up the page. The question is what triggers the loading. Google renders with a viewport but doesn't scroll like a person. If content loads when it enters the viewport, Google's renderer can still trigger it. If it loads only on scroll events or clicks, it may never appear.

Common mistake to avoid:

Lazy-loading the main hero image. It's visible on first load anyway, so lazy loading only delays it, which hurts your Largest Contentful Paint score.

Why it matters for rankings:

Content that only loads after a scroll or click may never be seen by Google. Viewport-based loading keeps pages fast and fully indexable.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/lazy-loading

🎓 Learn performance-safe SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#LazyLoading #JavaScriptSEO #TechnicalSEO

---

## Post 66: How to return proper status codes in a single-page app

How to return correct status codes in a single-page app (SPA)

In SPAs, every route often returns 200, even "not found" pages. That creates soft 404s.

Google's documented options:

Step 1: For a missing page, use JavaScript to redirect to a URL where the server returns a real 404.

Step 2: Or add <meta name="robots" content="noindex"> to the error view with JavaScript.

Step 3: Use the History API for routing, not #fragments.

Step 4: Make sure each route has a unique title and canonical.

Step 5: Best option: render routes on the server so the server can send real status codes.

Explained simply:

In a single-page app, the server usually returns the same HTML shell, with a 200 status, for every route. The app then decides in the browser what to show. Google sees a 200 for URLs that don't exist and can index 'not found' views as real pages. You have to send a proper signal another way.

Common mistake to avoid:

Showing a friendly 'page not found' component with no noindex and no redirect. Google may index hundreds of identical error views as separate pages.

Why it matters for rankings:

Without proper error handling, your SPA can flood Google's index with empty "not found" pages and dilute your site's quality signals.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Learn SPA SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #SPA #TechnicalSEO

---

## Post 67: Can JavaScript remove a noindex?

Can JavaScript remove a noindex tag?

Don't count on it. Google says that if it finds a noindex in the original HTML, it may skip rendering, so JavaScript that removes or changes the tag may never run.

How to handle noindex safely:

Step 1: Decide on the server whether a page is indexable.

Step 2: Output the correct robots meta tag in the initial HTML.

Step 3: Never ship "noindex by default, JS removes it later".

Step 4: If you must change robots tags client-side, only add a noindex, never remove one.

Step 5: Check with URL Inspection whether Google sees the page as indexable.

Explained simply:

Google reads the robots meta tag in the raw HTML before rendering. If it says noindex, Google may decide not to spend resources rendering a page it won't index. So JavaScript that would have removed the noindex may never run. The safe rule: decide on the server whether a page is indexable.

Common mistake to avoid:

Launching a site built from a staging template where noindex is in the HTML and a script removes it in production. Google may never run that script.

Why it matters for rankings:

A leftover noindex from staging or a JS template can keep entire templates out of Google's index, no matter how good the content is.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Learn index-control pitfalls in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Noindex #JavaScriptSEO #TechnicalSEO

---

## Post 68: How rendering consumes crawl budget

How rendering uses up crawl budget

Every CSS and JavaScript file Google fetches to render a page counts against the crawl budget of the host serving it.

To save budget, WRS tries to cache JS and CSS for up to 30 days.

How to make rendering cheaper:

Step 1: Bundle your code into fewer, larger files instead of dozens of tiny ones.

Step 2: Avoid cache-busting parameters that change on every deploy when the file hasn't changed.

Step 3: Use content-hash file names, so URLs change only when the content does.

Step 4: Consider serving static assets from a separate CDN hostname, but keep critical assets fast.

Step 5: Remove unused scripts.

Explained simply:

Every file a page needs to render has to be fetched, and fetches use crawling resources. WRS caches CSS and JS aggressively to save them. When you change a file's URL on every deploy (with a version query string, for example), Google has to fetch it again even if the content is identical. Stable URLs help.

Common mistake to avoid:

Appending ?v=timestamp to all scripts on every page load. Each URL looks new, so Google's cache can never be reused.

Why it matters for rankings:

Fewer resources to fetch for each render leaves more crawling for your actual pages, which means faster discovery and refresh of pages that rank.

Source: https://developers.google.com/search/blog/2024/12/crawling-december-resources

🎓 Learn crawl-aware front-end architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CrawlBudget #JavaScriptSEO #TechnicalSEO

---

## Post 69: What is dynamic rendering?

What is dynamic rendering, and should you use it?

Dynamic rendering means serving search engine bots a pre-rendered HTML version while users get the client-side JavaScript app.

Google describes it as a workaround, not a recommended long-term solution.

How to move away from it:

Step 1: Check whether you currently serve bots different HTML from users.

Step 2: Make sure bots and users get the same content. Different content can be treated as cloaking.

Step 3: Plan a move to server-side rendering, static generation or hydration.

Step 4: Migrate one template at a time and compare rendered output.

Step 5: Retire the bot-only pipeline when you're done.

Explained simply:

Dynamic rendering was popular when search engine renderers were less capable. It means running two pipelines: one for users and one for bots. Google now renders JavaScript well, and calls dynamic rendering a workaround. The risk is that the two versions drift apart, which can lead to indexing problems and look like cloaking.

Common mistake to avoid:

Bot versions that miss recent content updates because the pre-render cache isn't refreshed. Users see new prices; Google sees old ones.

Why it matters for rankings:

Dynamic rendering adds maintenance risk: the bot version can quietly drift from what users see. SSR gives everyone, including AI crawlers, the same complete HTML.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/dynamic-rendering

🎓 Learn modern rendering strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#DynamicRendering #JavaScriptSEO #TechnicalSEO

---

## Post 70: SSR vs CSR for SEO

SSR vs CSR: which is better for SEO?

CSR (client-side rendering): the server sends an empty "app shell", and JavaScript builds the content in the browser.

SSR (server-side rendering): the server sends complete HTML, and JavaScript adds interactivity on top.

Google notes that with app-shell sites, it has to run JavaScript before it can see the content.

How to choose:

Step 1: List the templates that drive organic traffic.

Step 2: Server-render (or statically generate) those templates.

Step 3: Keep CSR for logged-in dashboards and app-only views.

Step 4: Confirm that the raw HTML contains the main content, links and structured data.

Step 5: Measure LCP before and after.

Explained simply:

With CSR, the browser builds the page. With SSR, the server sends the page already built. Both can be indexed by Google, but SSR removes the risk and delay of rendering. Frameworks like Next.js, Nuxt and Astro make SSR or static generation straightforward, while keeping the app interactive after load.

Common mistake to avoid:

Server-rendering only the page shell while the main content still loads client-side. Check that the actual product details or article text are in the raw HTML.

Why it matters for rankings:

SSR makes content visible right after crawling, avoids rendering failures, and often improves Core Web Vitals. Many AI crawlers may also not run JavaScript.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Learn rendering architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SSR #JavaScriptSEO #TechnicalSEO

---

## Post 71: Why Googlebot declines permission requests

Why Googlebot declines permission requests

Googlebot declines user permission requests, such as camera, microphone, location and notifications.

If your content only loads after a permission is granted, Google never sees it.

How to build permission-safe pages:

Step 1: List every feature that asks for a permission.

Step 2: Make sure the main content loads without any permission.

Step 3: For location features, show default or nationwide content first, and let users narrow it down afterwards.

Step 4: Ask for permissions only after a user action, never on page load.

Step 5: Test with URL Inspection to check that the content renders without permissions.

Explained simply:

Browsers ask users for permission before using sensitive features like location or notifications. Googlebot is an automated system, so it simply declines all of these requests. If your page waits for a 'yes' before loading content, Google will wait for ever. Your content needs a sensible default that shows without permission.

Common mistake to avoid:

Pop-ups asking for notification permission immediately on load, blocking the content behind them. Google may render the blocked state.

Why it matters for rankings:

A store locator that needs geolocation before showing any stores may show Google nothing. Default content keeps the page indexable and able to rank.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/fix-search-javascript

🎓 Learn JS edge cases in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#JavaScriptSEO #TechnicalSEO #SEO

---

## Post 72: How to see your page the way Google sees it

How to see your page the way Google sees it

Search Console's URL Inspection tool and the Rich Results Test show what Google loads and renders.

Step 1: Open Search Console → URL Inspection and enter the URL.

Step 2: Click "Test Live URL".

Step 3: Open "View tested page".

Step 4: Check the HTML tab. Is the main content there?

Step 5: Check the screenshot. Does it look complete?

Step 6: Check More info → Page resources. Did any resource fail to load?

Step 7: Check the JavaScript console messages for errors.

Step 8: Compare "User-declared canonical" with "Google-selected canonical".

Explained simply:

URL Inspection shows two views: what Google has indexed (from the last crawl), and a live test (a fresh fetch and render now). Together they let you compare the past with the present, and Google's view with your browser's. Most indexing mysteries are explained by a difference between them. If the live test looks right but the indexed version doesn't, Google simply hasn't recrawled yet.

Common mistake to avoid:

Only looking at the screenshot. A page can look complete while key text is in an image or iframe. Always check the HTML tab too.

Why it matters for rankings:

This is the closest you can get to seeing exactly what Google indexes. Most "why isn't this ranking?" problems show up here within minutes.

Source: https://support.google.com/webmasters/answer/9012289

🎓 Learn Search Console like a pro in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsole #TechnicalSEO #SEO

---

## Post 73: What is canonicalization?

What is canonicalization?

Canonicalization is how Google picks the representative (canonical) URL for a piece of content, so that only one version of duplicate content appears in search results.

Duplicates come from:
→ http vs https
→ www vs non-www
→ Trailing slashes
→ Parameters and tracking codes
→ Mobile and AMP versions

How to control canonicalization:

Step 1: Pick one preferred URL format.

Step 2: Redirect other formats to it.

Step 3: Add rel="canonical" pointing to the preferred URL.

Step 4: Link internally only to the preferred URL.

Step 5: Include only preferred URLs in your sitemap.

Explained simply:

The same content is often reachable at many URLs: with and without www, with tracking parameters, with different capitalisation. Google groups these duplicates and picks one to show. Your job is to make that choice obvious through consistent signals, so ranking signals are consolidated on one strong URL.

Common mistake to avoid:

Assuming Google will 'just figure it out'. It often does, but sometimes it picks the URL you didn't want, like a parameter version or the http page.

Why it matters for rankings:

Duplicates split links and other signals. Canonicalization brings them together on one URL, which strengthens that URL's ability to rank.

Source: https://developers.google.com/search/docs/crawling-indexing/canonicalization

🎓 Learn canonical strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Canonical #TechnicalSEO #SEO

---

## Post 74: How to use rel=canonical correctly

How to use rel="canonical" correctly

Step 1: Put the tag in the <head>:
<link rel="canonical" href="https://example.com/page">

Step 2: Use absolute URLs, not relative ones.

Step 3: Point to a URL that returns 200, not one that redirects or returns 404.

Step 4: Point to an indexable URL, without noindex.

Step 5: Use only one canonical per page.

Step 6: Don't canonicalize paginated pages to page 1.

Step 7: Make sure the page you point to has substantially the same content.

Step 8: Check "Google-selected canonical" in URL Inspection.

Explained simply:

rel=canonical is a strong hint, not a command. Google weighs it with other signals and can ignore it if they contradict it. Most ignored canonicals come from technical mistakes: pointing to a redirect, to a 404, to a noindexed page, or to a page with different content. A clean canonical is far more likely to be respected.

Common mistake to avoid:

Every page pointing its canonical to the homepage, usually from a template bug. Google will ignore it, but it's a sign other signals may be broken too.

Why it matters for rankings:

A correct canonical brings ranking signals together on your preferred URL. A broken one can send them to the wrong page, or get your canonical ignored.

Source: https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

🎓 Learn to debug canonicals in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Canonical #TechnicalSEO #SEO

---

## Post 75: How to set a canonical for PDFs and non-HTML files

How to set a canonical for PDFs and other non-HTML files

You can't put a <link> tag inside a PDF. Instead, use an HTTP response header:

Link: <https://example.com/guide>; rel="canonical"

Step 1: Find PDFs that duplicate an HTML page.

Step 2: Configure your server or CDN to add the Link header to those PDF responses.

Step 3: Point it to the HTML version you want to rank.

Step 4: Check it: curl -I https://example.com/guide.pdf

Step 5: Confirm with URL Inspection on the PDF URL.

Explained simply:

Non-HTML files have no <head>, so you can't add a <link> tag. HTTP headers solve this: the server attaches the canonical to the response itself. Google reads it just like an HTML canonical. The same approach works for X-Robots-Tag, so headers are the standard way to control indexing for files. You can set them once in your server or CDN config and they apply to every matching file.

Common mistake to avoid:

Adding the Link header to the HTML page instead of the PDF. The header must be on the duplicate (the PDF) and point to the version you prefer.

Why it matters for rankings:

Without a canonical header, a PDF and an HTML page can compete for the same query. The header brings signals together on the page that converts better.

Source: https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

🎓 Learn header-level SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Canonical #PDF #TechnicalSEO

---

## Post 76: How strong are different canonical signals?

How strong are different canonical signals?

Google lists these ways to show your preferred URL, from strongest to weakest:

1. Redirects: strong signal
2. rel="canonical": strong signal
3. Sitemap inclusion: weak signal

Google says these methods stack, and work better together.

How to make your canonical signals agree:

Step 1: Redirect duplicate URLs to the preferred URL where possible.

Step 2: Add a self-referencing canonical on the preferred URL.

Step 3: List only preferred URLs in your sitemap.

Step 4: Link internally only to preferred URLs.

Step 5: Use the same URL in hreflang and structured data.

Explained simply:

Google combines many signals to choose a canonical: redirects, canonical tags, sitemaps, internal links, hreflang and more. Each signal is a vote. When they all vote the same way, Google follows them. When they disagree, Google has to pick for itself, and may not pick what you wanted.

Common mistake to avoid:

A canonical to URL A while the sitemap lists URL B and internal links point to URL C. Google sees three different answers.

Why it matters for rankings:

When signals conflict, Google may choose a different canonical from the one you want. When they all agree, Google is far more likely to rank your preferred URL.

Source: https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls

🎓 Learn signal alignment in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Canonical #TechnicalSEO #SEO

---

## Post 77: What is the robots meta tag?

What is the robots meta tag?

The robots meta tag controls, page by page, how an HTML page is indexed and shown in Google Search.

<meta name="robots" content="noindex, nofollow">

Common values:
→ noindex: don't show this page in results
→ nofollow: don't follow links on this page
→ nosnippet: no text snippet
→ max-snippet:[number]: limits the snippet length
→ max-image-preview:large: allows large image previews
→ unavailable_after:[date]: removes the page after a date

How to use it:

Step 1: Add it in <head>.

Step 2: Target Google only with name="googlebot" if needed.

Step 3: Make sure robots.txt doesn't block the page, or Google can't read the tag.

Step 4: Check with URL Inspection.

Explained simply:

The robots meta tag lives inside the page, so it only takes effect when Google crawls the page. It gives very fine control: one page can be indexed with limited snippets, another kept out of the index entirely. You can address all search engines with name="robots" or only Google with name="googlebot".

Common mistake to avoid:

Using nofollow on a whole page to 'save link equity'. It mainly stops Google discovering pages through those links. It's rarely what you actually want.

Why it matters for rankings:

Used carefully, it removes low-value pages and improves how your results look. Used carelessly, it can deindex the pages that earn you money.

Source: https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag

🎓 Learn index governance in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsMeta #TechnicalSEO #SEO

---

## Post 78: What is X-Robots-Tag?

What is X-Robots-Tag?

X-Robots-Tag is an HTTP response header that does the same job as the robots meta tag. It works on any file: PDFs, images, videos and documents.

X-Robots-Tag: noindex
X-Robots-Tag: googlebot: nosnippet

How to use it:

Step 1: Find the non-HTML files you don't want in search results.

Step 2: Add the header in your server or CDN configuration for those paths or file types.

Step 3: For sitewide rules, apply it by pattern, for example all *.pdf files in /internal/.

Step 4: Check it: curl -I URL

Step 5: Make sure robots.txt allows crawling those files, or Google can't see the header.

Explained simply:

Some files can't carry a meta tag: PDFs, images, videos, feeds. X-Robots-Tag moves the same directives into the HTTP response header, so the server can apply them to any file type. It's also useful for setting rules in bulk by path or file type in the server or CDN config, without editing pages.

Common mistake to avoid:

Setting X-Robots-Tag: noindex in a global config by mistake, often copied from staging. It applies to every response, including your HTML pages.

Why it matters for rankings:

It keeps internal PDFs, feeds and media duplicates out of the index, so your real pages aren't competing with them.

Source: https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag

🎓 Learn header-level index control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#XRobotsTag #TechnicalSEO #SEO

---

## Post 79: How to control snippets (and AI Overviews)

How to control your snippets, including in AI Overviews

Google's snippet controls apply to all forms of search results, including AI Overviews and AI Mode.

Step 1: Block the snippet for a whole page:
<meta name="robots" content="nosnippet">

Step 2: Limit the snippet length:
<meta name="robots" content="max-snippet:150">

Step 3: Exclude part of a page:
<span data-nosnippet>Hidden text</span>

Step 4: Allow large image previews:
<meta name="robots" content="max-image-preview:large">

Step 5: Test the effect on your click-through rate before rolling out sitewide.

Explained simply:

Snippets are the text Google shows from your page. The same controls now apply to AI Overviews and AI Mode, because those features use your content as a direct source. This gives you fine-grained control: keep pages indexed while limiting how much text Google can show or use in AI answers. You can also hide just one sensitive section of a page with data-nosnippet and leave the rest available.

Common mistake to avoid:

Adding nosnippet sitewide out of fear of AI. It removes snippets from normal results too, which can lower click-through rates.

Why it matters for rankings:

Snippets drive clicks. Blocking them too broadly can lower click-through and remove you as a source in AI answers. Use these controls carefully.

Source: https://developers.google.com/search/docs/crawling-indexing/robots-meta-tag

🎓 Learn snippet and AI visibility control in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#AIOverviews #TechnicalSEO #SEO

---

## Post 80: What is hreflang?

What is hreflang?

hreflang tells Google that several pages are language or regional versions of the same content, so it can show each user the right version.

How to set up hreflang:

Step 1: List every language or region version of the page.

Step 2: On each version, add a tag for every version, including itself:
<link rel="alternate" hreflang="en-in" href="https://example.com/in/">
<link rel="alternate" hreflang="en-gb" href="https://example.com/uk/">

Step 3: Make the tags reciprocal. If A points to B, B must point to A.

Step 4: Point only to canonical URLs that return 200.

Step 5: Use valid codes: language (ISO 639-1), plus region (ISO 3166-1) if needed.

Step 6: Add hreflang in HTML, HTTP headers or the sitemap. Pick one method.

Explained simply:

If you have English pages for India, the UK and the US, they can look like duplicates. hreflang tells Google they're intentional alternates for different audiences, so it can show the right one to each searcher. It doesn't boost rankings by itself; it makes sure the right version appears where you already rank.

Common mistake to avoid:

Missing return links. If the UK page lists India but the India page doesn't list the UK, Google may ignore the pairing.

Why it matters for rankings:

Correct hreflang shows the right local page in each market, so users don't land on the wrong currency or language version and bounce.

Source: https://developers.google.com/search/docs/specialty/international/localized-versions

🎓 Learn international SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Hreflang #InternationalSEO #TechnicalSEO

---

## Post 81: What is x-default in hreflang?

What is x-default in hreflang?

x-default is a reserved hreflang value for users whose language or region doesn't match any of your versions. It's the fallback page.

How to set it up:

Step 1: Choose the fallback: usually a language selector or your global English page.

Step 2: Add it to every version's hreflang set:
<link rel="alternate" hreflang="x-default" href="https://example.com/">

Step 3: Keep it consistent. Every version should point to the same x-default.

Step 4: Make sure the x-default URL returns 200 and is indexable.

Step 5: Check the setup with an hreflang crawler.

Explained simply:

hreflang covers the audiences you explicitly target. Everyone else, such as a French speaker on an English-only site, needs a default. x-default names that fallback page. It's often a language or country selector, or your most universal version. Without it, Google has to guess which version to show.

Common mistake to avoid:

Pointing x-default to a page that automatically redirects by IP. Googlebot crawls mostly from the US, so it may only ever see the US version.

Why it matters for rankings:

Without x-default, users from markets you don't target may land on a random regional page. A good fallback improves the experience for them, and gives Google a clear default to show.

Source: https://developers.google.com/search/docs/specialty/international/localized-versions

🎓 Learn global site architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Hreflang #InternationalSEO #TechnicalSEO

---

## Post 82: What is an XML sitemap?

What is an XML sitemap?

A sitemap is a file listing the URLs you want search engines to know about, with optional details such as last-modified dates.

How to build a good sitemap:

Step 1: Include only canonical, indexable URLs that return 200.

Step 2: Exclude redirects, 404s, noindexed pages and parameter duplicates.

Step 3: Use absolute URLs.

Step 4: Save it as UTF-8 XML, for example /sitemap.xml.

Step 5: Reference it in robots.txt:
Sitemap: https://example.com/sitemap.xml

Step 6: Submit it in Search Console → Sitemaps.

Step 7: Generate it automatically so it never goes stale.

Explained simply:

A sitemap is a list of URLs you consider important. It doesn't force indexing, but it helps Google discover pages that links alone might not reach quickly, and tells it which version of each URL you prefer. Its value depends on accuracy: a sitemap full of redirects and 404s teaches Google to trust it less.

Common mistake to avoid:

Listing every URL the CMS knows about, including noindexed, redirected and parameter pages. The sitemap should be a curated list.

Why it matters for rankings:

Sitemaps speed up discovery, especially for new, deep or poorly linked pages. A clean sitemap is also a (weak) canonical signal.

Source: https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap

🎓 Learn sitemap strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#XMLSitemap #TechnicalSEO #SEO

---

## Post 83: What are sitemap limits and sitemap index files?

What are the sitemap limits?

Each sitemap file is limited to:
→ 50,000 URLs, or
→ 50MB uncompressed

Above that, split it up and use a sitemap index file.

How to scale sitemaps:

Step 1: Split URLs by type: products, categories, blog, images.

Step 2: Keep each file under 50,000 URLs and 50MB.

Step 3: Create a sitemap index that lists every sitemap file.

Step 4: Add lastmod to each entry in the index, to show which files changed.

Step 5: Submit only the index file in Search Console.

Step 6: Check indexing per sitemap to find weak sections.

Explained simply:

Limits keep sitemap files a reasonable size to fetch and process. Large sites solve this with multiple sitemaps and an index file. Splitting by page type also helps with diagnostics: Search Console reports indexing per sitemap, so you can see that products are 90 percent indexed while blog tags are only 10 percent.

Common mistake to avoid:

Splitting sitemaps at random (sitemap1, sitemap2...) rather than by page type. You lose the ability to see which sections have problems.

Why it matters for rankings:

Splitting sitemaps by type shows you which sections Google indexes poorly, so you can fix what's stopping those pages from ranking.

Source: https://developers.google.com/search/docs/crawling-indexing/sitemaps/large-sitemaps

🎓 Learn enterprise sitemap architecture in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#XMLSitemap #EnterpriseSEO #TechnicalSEO

---

## Post 84: How Google uses lastmod

How does Google use lastmod in sitemaps?

Google uses <lastmod> only if it's consistently and verifiably accurate. It should reflect the last significant update to the page.

How to set lastmod properly:

Step 1: Update lastmod only when the main content changes (text, price, specs).

Step 2: Don't update it for footer, copyright year or sidebar changes.

Step 3: Never set every URL to today's date.

Step 4: Use the W3C Datetime format, for example 2026-10-05 or 2026-10-05T10:00:00+05:30.

Step 5: Match it to the real update time in your CMS.

Step 6: Skip priority and changefreq. Google ignores them.

Explained simply:

lastmod helps Google decide what to recrawl first. Google uses it only when it has learned it's accurate, by checking the dates against what it finds. If every URL claims to have changed today, the signal becomes noise and Google may ignore it for your whole site. Accurate dates are better than more frequent ones.

Common mistake to avoid:

Setting lastmod to the sitemap generation time. Every URL looks changed on every run, which teaches Google the dates aren't reliable.

Why it matters for rankings:

Accurate lastmod helps Google recrawl updated pages sooner, so refreshed content can start competing in search faster.

Source: https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap

🎓 Learn freshness optimization in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#XMLSitemap #TechnicalSEO #SEO

---

## Post 85: What are image, video and news sitemaps?

What are image, video and news sitemaps?

Google supports sitemap extensions that add details about media and news content:
→ Image sitemaps: help Google find images, for example ones loaded by JavaScript
→ Video sitemaps: give details about video content
→ News sitemaps: for recent articles on news sites
→ hreflang in sitemaps: localized versions

How to use them:

Step 1: Choose the extension that fits your content.

Step 2: Add the right namespace, for example:
xmlns:image="http://www.google.com/schemas/sitemap-image/1.1"

Step 3: Add the extension tags inside each <url> entry.

Step 4: Combine extensions in one sitemap if needed. Google supports that.

Step 5: Submit the file and watch for errors in Search Console.

Explained simply:

Standard sitemaps list page URLs. Extensions add details about the media or news on those pages. They help most when media is hard to discover through normal crawling, for example images loaded by JavaScript or videos in custom players. For news sites, news sitemaps help surface recent articles quickly.

Common mistake to avoid:

Listing images from a CDN domain that blocks Googlebot-Image in its own robots.txt. Listing them in the sitemap doesn't override the block.

Why it matters for rankings:

Media that Google can't find can't rank in Images, Video or News. Extensions make it easier to find, and qualify it for richer search features.

Source: https://developers.google.com/search/docs/crawling-indexing/sitemaps/combine-sitemap-extensions

🎓 Learn media SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#VideoSEO #ImageSEO #TechnicalSEO

---

## Post 86: How to migrate a site without losing rankings

How to migrate a site without losing rankings

Google recommends permanent server-side redirects for site moves, kept for as long as possible, generally at least one year.

Step 1: Map every old URL to its new equivalent, one to one.

Step 2: Set up 301 or 308 redirects. Avoid chains.

Step 3: Update canonicals, hreflang and structured data to the new URLs.

Step 4: Update internal links to point straight at the new URLs.

Step 5: Publish new sitemaps, and keep the old ones briefly so Google sees the redirects.

Step 6: Verify the new property in Search Console. Use Change of Address for domain moves.

Step 7: Monitor 404s, crawl stats and rankings daily for weeks.

Step 8: Keep the redirects for at least a year.

Explained simply:

When URLs change, all the signals pointing to the old URLs need to be transferred. Redirects are the bridge. Google needs to recrawl old URLs, see the redirects, and move the signals over, which takes time. That's why redirects should stay for a year or more, and why every old URL needs a precise new destination.

Common mistake to avoid:

Redirecting all old URLs to the new homepage. Google may treat many of these as soft 404s, and relevance built up by individual pages can be lost.

Why it matters for rankings:

Migrations are where years of rankings can be lost or kept. Accurate redirects carry your ranking signals over to the new URLs.

Source: https://developers.google.com/search/docs/crawling-indexing/site-move-with-url-changes

🎓 Learn migration playbooks in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SiteMigration #TechnicalSEO #SEO

---

## Post 87: How do pages get into Google's AI Overviews?

How do pages appear in Google's AI Overviews and AI Mode?

According to Google, to be shown as a supporting link a page must:
→ Be indexed
→ Be eligible to appear in Google Search with a snippet

Google says there are no additional technical requirements.

How to make your pages eligible:

Step 1: Allow Googlebot in robots.txt.

Step 2: Make sure the page returns 200 and is indexable.

Step 3: Don't block snippets with nosnippet if you want to be cited.

Step 4: Put important information in text, not only in images.

Step 5: Link internally so the page is easy to discover.

Step 6: Keep your structured data consistent with the visible content.

Explained simply:

AI Overviews and AI Mode use pages from Google's existing search index, so there's no separate AI crawler to optimise for. If your page can appear in normal results with a snippet, it's eligible to be a supporting link. Being eligible doesn't guarantee being cited; relevance and quality still decide that.

Common mistake to avoid:

Blocking Googlebot from parts of the site, or adding nosnippet, then wondering why those pages are never cited in AI answers.

Why it matters for rankings:

AI features are built on the same crawl and index as regular Search. Strong technical SEO is what makes you eligible to be cited in AI answers.

Source: https://developers.google.com/search/docs/appearance/ai-features

🎓 Learn technical SEO for AI search in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#AIOverviews #AISearch #TechnicalSEO

---

## Post 88: Do you need llms.txt for Google AI search?

Do you need llms.txt or "AI files" to appear in Google's AI search?

Google says no. To appear in AI Overviews or AI Mode, you don't need to create:
→ New machine-readable files
→ AI text files
→ Special schema.org markup

How to focus your effort instead:

Step 1: Make sure Googlebot can crawl your key pages.

Step 2: Make sure they're indexed. Check with URL Inspection.

Step 3: Write clear, well-structured text that answers questions directly.

Step 4: Support your text with relevant images and videos.

Step 5: Provide a good page experience.

Step 6: Use only the structured data types Google documents.

Explained simply:

llms.txt is a proposed format some sites use to summarise their content for language models. Google's documentation is explicit that it doesn't need special files or special markup for its AI search features. Other AI platforms may treat such files differently, but for Google, normal crawling and indexing is what counts.

Common mistake to avoid:

Spending weeks on AI-specific files while key pages have crawl errors, thin content or JavaScript-only text.

Why it matters for rankings:

Time spent on unsupported "AI files" is time not spent on crawlability and content, which is what actually decides whether you rank and get cited in Google.

Source: https://developers.google.com/search/docs/appearance/ai-features

🎓 Separate AI search myths from facts in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#AISearch #GEO #TechnicalSEO

---

## Post 89: What are OAI-SearchBot, GPTBot and ChatGPT-User?

What are OpenAI's crawlers?

OpenAI uses separate user agents for separate purposes:

→ OAI-SearchBot: surfaces sites in ChatGPT search results
→ GPTBot: crawls content that may be used to train generative AI models
→ ChatGPT-User: fetches pages when a user asks ChatGPT something. Because a user triggers it, robots.txt rules may not apply.

Each setting is independent.

How to stay visible in ChatGPT search but opt out of training:

Step 1: In robots.txt, allow OAI-SearchBot:
User-agent: OAI-SearchBot
Allow: /

Step 2: Block GPTBot:
User-agent: GPTBot
Disallow: /

Step 3: Check your CDN and WAF aren't blocking OAI-SearchBot.

Step 4: Verify the requests using OpenAI's published IP ranges.

Explained simply:

OpenAI separates its bots by purpose so you can make independent choices. Allowing search crawling while blocking training is a common setup. ChatGPT-User is different: it fetches pages for a specific user in real time, more like a browser visit than crawling, which is why robots.txt may not apply.

Common mistake to avoid:

Blocking all OpenAI user agents in one rule, then losing visibility in ChatGPT search, where many users now look for answers.

Why it matters for rankings:

If OpenAI's search bot is blocked, OpenAI says your site won't appear in ChatGPT search answers, apart from navigational links.

Source: https://developers.openai.com/api/docs/bots

🎓 Learn AI crawler strategy in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#ChatGPT #AISearch #TechnicalSEO

---

## Post 90: What are ClaudeBot, Claude-SearchBot and Claude-User?

What are Anthropic's crawlers?

Anthropic uses three robots:

→ ClaudeBot: collects web content that could contribute to AI model training
→ Claude-SearchBot: crawls to improve the quality of search results for Claude users
→ Claude-User: fetches pages when a Claude user asks a question

How to control them:

Step 1: Opt out of training only:
User-agent: ClaudeBot
Disallow: /

Step 2: Keep search visibility by allowing Claude-SearchBot and Claude-User.

Step 3: If you need to slow ClaudeBot down, use Crawl-delay. Anthropic supports it:
User-agent: ClaudeBot
Crawl-delay: 1

Step 4: Confirm your firewall isn't blocking the agents you allow.

Explained simply:

Anthropic also separates its bots by purpose: training, search indexing and user-requested fetches. Each can be allowed or blocked on its own. Unlike Google, Anthropic supports the Crawl-delay directive, which gives you a simple way to reduce load from its training crawler without blocking it.

Common mistake to avoid:

Treating every AI bot as the same thing. A training opt-out and a search opt-out have very different consequences for your visibility.

Why it matters for rankings:

Anthropic says blocking Claude-User may reduce your site's visibility for user-directed web search in Claude. Decide on each bot separately rather than blocking all AI at once.

Source: https://support.claude.com/en/articles/8896518-does-anthropic-crawl-data-from-the-web-and-how-can-site-owners-block-the-crawler

🎓 Learn AI crawl governance in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Claude #AISearch #TechnicalSEO

---

## Post 91: What are PerplexityBot and Perplexity-User?

What are Perplexity's crawlers?

→ PerplexityBot: surfaces and links websites in Perplexity search results. Perplexity says it isn't used to crawl content for AI foundation models.
→ Perplexity-User: visits pages when a Perplexity user asks a question, so it can cite them in the answer.

How to optimize for Perplexity visibility:

Step 1: Allow PerplexityBot in robots.txt.

Step 2: Allowlist Perplexity's published IP ranges in your WAF, using its official documentation.

Step 3: Serve complete content in the server HTML.

Step 4: Use clear headings and concise answers that are easy to cite.

Step 5: Monitor PerplexityBot and Perplexity-User hits in your logs.

Explained simply:

Perplexity answers questions with citations, and its crawler gathers pages it can cite. Perplexity-User fetches pages live when a user's question needs them. Both are about sending visitors back through citations rather than training models, so blocking them mainly costs visibility.

Common mistake to avoid:

Allowing PerplexityBot in robots.txt while a WAF rule blocks it. Check both layers, and use the officially published IP lists.

Why it matters for rankings:

Being crawlable by AI search engines is now part of technical SEO. If PerplexityBot can't reach you, you can't be cited in its answers.

Source: https://docs.perplexity.ai/docs/resources/perplexity-crawlers

🎓 Learn multi-engine AI visibility in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Perplexity #AISearch #TechnicalSEO

---

## Post 92: What is IndexNow?

What is IndexNow?

IndexNow is a protocol created by Microsoft Bing and Yandex. It lets you notify search engines straight away when URLs are added, updated or deleted. Participating engines share the submissions with each other.

Bing says timely IndexNow notifications also help keep Copilot answers and grounding results fresh.

How to set it up:

Step 1: Generate an API key.

Step 2: Host it as a UTF-8 text file at your site root, named {your-key}.txt.

Step 3: When content changes, submit the URL (or a batch) to the IndexNow endpoint with your key.

Step 4: Automate it from your CMS on publish, update and delete.

Step 5: Check submissions in Bing Webmaster Tools.

Note: Google doesn't use IndexNow. Keep your sitemaps for Google.

Explained simply:

Traditional crawling means waiting for search engines to come back and check. IndexNow reverses that: your site tells participating engines the moment something changes. That's especially useful for fast-changing content like prices, stock and news. One ping is shared across all participating engines.

Common mistake to avoid:

Submitting every URL on every deploy. Only submit URLs that actually changed, or the signal loses value.

Why it matters for rankings:

Faster indexing on Bing means faster visibility in Bing and in experiences built on its index.

Source: https://www.indexnow.org/documentation

🎓 Learn multi-engine indexing in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#IndexNow #Bing #TechnicalSEO

---

## Post 93: How to write an AI-aware robots.txt

How to write a robots.txt that's ready for AI crawlers

Step 1: Decide your policy for each purpose:
→ Search visibility: usually allow
→ AI training: your choice
→ User-triggered fetches: usually allow

Step 2: Keep Googlebot rules unchanged.

Step 3: Add training opt-outs, if you want them:
User-agent: Google-Extended
Disallow: /

User-agent: GPTBot
Disallow: /

User-agent: ClaudeBot
Disallow: /

Step 4: Explicitly allow AI search bots:
User-agent: OAI-SearchBot
Allow: /

User-agent: PerplexityBot
Allow: /

Step 5: Keep your Sitemap line at the bottom.

Step 6: Test, deploy and check the result in your logs.

Explained simply:

AI crawlers serve different purposes: some train models, some build search indexes, some fetch pages for a user in real time. A good robots.txt treats them separately. That way you can protect content from training if you want to, while staying visible in AI-powered search experiences.

Common mistake to avoid:

Copying an 'AI blocklist' from the internet that also contains search bots like OAI-SearchBot or PerplexityBot, and losing AI search visibility without realising.

Why it matters for rankings:

A blanket "block all AI" approach can remove you from AI search answers. A rule per bot protects your content and keeps your visibility.

Source: https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec

🎓 Build your AI crawl policy with us in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#RobotsTxt #AISearch #TechnicalSEO

---

## Post 94: Why server-side HTML matters for AI crawlers

Why server-side HTML matters more in the AI search era

Google's WRS renders JavaScript with an up-to-date Chromium. Many other crawlers and AI fetchers may not render JavaScript the same way.

How to make content readable by every crawler:

Step 1: Turn off JavaScript and load your key pages.

Step 2: If the main content disappears, you depend on rendering.

Step 3: Move critical templates to SSR or static generation.

Step 4: Keep headings, body text, prices and FAQs in the raw HTML.

Step 5: Keep links as <a href> in the raw HTML.

Step 6: Check your server logs to see which AI bots fetch your pages.

Explained simply:

Google has invested heavily in rendering JavaScript. Not every crawler does the same, and many AI fetchers prioritise speed by reading raw HTML. If your content only exists after JavaScript runs, some systems may see an empty page. Server-rendered HTML is the most portable format for the open web.

Common mistake to avoid:

Testing only with Google tools and concluding the site is fine. Disable JavaScript in your browser to see what non-rendering crawlers get.

Why it matters for rankings:

Content in the raw HTML can be read by Google, Bing and AI crawlers alike. That gives you the widest chance to rank and to be cited.

Source: https://developers.google.com/search/docs/crawling-indexing/javascript/javascript-seo-basics

🎓 Learn rendering for every engine in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#AISearch #JavaScriptSEO #TechnicalSEO

---

## Post 95: How to check whether your CDN blocks AI search bots

How to check whether your CDN or firewall is blocking AI search bots

Many CDNs now offer one-click "block AI bots" settings. They can block search bots along with training bots.

Step 1: List the bots you want to allow: Googlebot, Bingbot, OAI-SearchBot, Claude-SearchBot, PerplexityBot.

Step 2: Check your CDN or WAF bot settings for AI-blocking toggles.

Step 3: Filter your firewall logs by those user agents. Look for blocks, challenges and 403s.

Step 4: Verify each bot against the IP ranges its company publishes.

Step 5: Add allow rules for verified search bots.

Step 6: Recheck monthly. Vendors update their bot lists.

Explained simply:

Your robots.txt is a request; your CDN or firewall is enforcement. If a firewall blocks a bot first, the bot never reaches robots.txt, and never reaches your content. Many CDNs now ship AI-bot blocking features, sometimes turned on by default, that don't always separate search bots from training bots.

Common mistake to avoid:

Assuming a CDN's 'verified bots' list includes every AI search crawler. Check each bot you care about individually.

Why it matters for rankings:

Your robots.txt might say "Allow", but if the firewall blocks a bot first, the bot never gets that far. Your visibility in AI search depends on both layers.

Source: https://developers.openai.com/api/docs/bots

🎓 Learn infrastructure-level SEO in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#CDN #AISearch #TechnicalSEO

---

## Post 96: What is the Crawl Stats report?

What is the Crawl Stats report in Search Console?

It shows Google's crawling history on your site: how many requests, the server's responses, and any availability problems.

Find it in: Search Console → Settings → Crawl stats.

How to read it:

Step 1: Check Total crawl requests over time. Look for sudden drops.

Step 2: Check Average response time. Rising times can reduce crawling.

Step 3: Open Host status. Look at robots.txt fetching, DNS and server connectivity.

Step 4: Review By response for 3xx, 4xx and 5xx shares.

Step 5: Review By purpose: Discovery (new URLs) vs Refresh (known URLs).

Step 6: Review By Googlebot type: Smartphone should dominate.

Explained simply:

Crawl Stats is Google's own record of how it experiences your server. Unlike third-party tools, it reflects real Googlebot requests. Host status is the most urgent section: problems with robots.txt fetching, DNS or connectivity can affect your whole site, and they show up here first.

Common mistake to avoid:

Looking only at total crawl requests. A stable total can hide a growing share of 404s, redirects or slow responses.

Why it matters for rankings:

Crawl problems often show up here before rankings drop. Checking weekly lets you fix them before they cost you traffic.

Source: https://support.google.com/webmasters/answer/9679690

🎓 Learn Crawl Stats analysis in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsole #CrawlStats #TechnicalSEO

---

## Post 97: How to read the Page Indexing report

How to read Search Console's Page Indexing report

It shows the indexing status of every URL Google knows about on your property.

Step 1: Open Search Console → Indexing → Pages.

Step 2: Compare the indexed and not-indexed counts over time.

Step 3: Work through each "Why pages aren't indexed" reason:
→ Discovered – currently not indexed: often a crawl budget or priority issue
→ Crawled – currently not indexed: usually quality or duplication
→ Duplicate, Google chose a different canonical: check your canonical signals
→ Excluded by noindex: confirm this is intentional
→ Blocked by robots.txt: confirm this is intentional
→ Soft 404, 404, 5xx, Redirect error: fix the response

Step 4: Click into each reason and check sample URLs.

Step 5: Fix the issue, then click "Validate fix".

Explained simply:

This report shows Google's view of every URL it knows on your site, grouped by why it is or isn't indexed. Not all exclusions are problems: noindexed and redirected URLs are supposed to be excluded. The skill is telling intended exclusions apart from accidental ones that are costing you rankings.

Common mistake to avoid:

Trying to get 'not indexed' to zero. Some exclusions are healthy. Focus on important URLs that should be indexed but aren't.

Why it matters for rankings:

Every important URL listed as "not indexed" is a page that can't rank. This report is your list of things to fix.

Source: https://support.google.com/webmasters/answer/7440203

🎓 Learn indexing diagnostics in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsole #Indexing #TechnicalSEO

---

## Post 98: What is the URL Inspection API?

What is the Search Console URL Inspection API?

It gives you programmatic access to Google's indexing data for URLs in properties you manage, including:
→ Index status and coverage
→ Last crawl time
→ Google-selected vs user-declared canonical
→ Rich results status

How to use it at scale:

Step 1: Enable the Search Console API in Google Cloud.

Step 2: Authenticate with an account that has access to the property.

Step 3: Send your priority URLs (top revenue pages) in batches.

Step 4: Store the results daily in a sheet or database.

Step 5: Alert when a key URL changes from indexed to not indexed, or its canonical changes.

Step 6: Respect the daily quota.

Explained simply:

The Search Console interface checks one URL at a time. The API lets you check hundreds automatically every day. That turns indexing from something you check after traffic drops into something you monitor continuously. It's especially valuable for large sites where key pages can drop out of the index unnoticed.

Common mistake to avoid:

Inspecting random URLs. Use your daily quota on the URLs that matter most: top revenue pages, new launches and recently changed templates.

Why it matters for rankings:

It lets you catch deindexing of key pages within a day, instead of noticing weeks later when traffic drops.

Source: https://developers.google.com/search/blog/2022/01/url-inspection-api

🎓 Learn SEO automation in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#SearchConsoleAPI #SEOAutomation #TechnicalSEO

---

## Post 99: How to ask Google to recrawl your pages

How to ask Google to recrawl your pages

Google offers two documented methods:

Method 1: For a few URLs

Step 1: Open Search Console → URL Inspection.

Step 2: Enter the updated URL.

Step 3: Click "Request Indexing".

Step 4: Don't submit the same URL again and again. It doesn't speed things up.

Method 2: For many URLs

Step 1: Update your XML sitemap with accurate lastmod values.

Step 2: Resubmit it in Search Console → Sitemaps, or make sure robots.txt references it.

Step 3: Add internal links from frequently crawled pages to the updated URLs.

Note: crawling can take anywhere from days to weeks, and a request doesn't guarantee indexing.

Explained simply:

Google recrawls pages on its own schedule, based on importance and how often they change. These methods ask it to come sooner. They're requests, not commands: Google still decides when to crawl and whether to index. Good internal linking and accurate sitemaps make recrawling faster by default.

Common mistake to avoid:

Requesting indexing for hundreds of URLs one by one every day. There's a quota, and repeated requests for the same URL don't speed things up.

Why it matters for rankings:

Getting updated content recrawled sooner means your improvements reach search results sooner.

Source: https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl

🎓 Learn fast-indexing workflows in our live 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#Indexing #SearchConsole #TechnicalSEO

---

## Post 100: The complete crawl audit checklist

How to run a complete technical crawl audit: a 12-step checklist

Step 1: robots.txt returns 200, is under 500 KiB, and has no accidental "Disallow: /".

Step 2: Googlebot isn't blocked or challenged by your CDN or WAF.

Step 3: Uncompressed HTML is under 2MB, with SEO tags near the top.

Step 4: Redirects are single-hop. Use 301/308 for permanent moves.

Step 5: Removed pages return real 404/410. No soft 404s.

Step 6: No ongoing 5xx, 429 or DNS errors in Crawl Stats.

Step 7: ETag and 304 responses work for repeat crawls.

Step 8: Faceted and parameter URLs are under control.

Step 9: Pagination uses unique, crawlable URLs.

Step 10: Main content and links are in the raw HTML.

Step 11: Canonical, hreflang, sitemap and internal links all point to the same preferred URL.

Step 12: Your AI crawler policy is set for each bot, with search bots allowed.

Explained simply:

Each step in this checklist removes one barrier between your content and Google's index. Together, they make sure Google can reach your pages, read them fully, understand which version to rank, and spend its crawling on what matters. It's worth running this audit after every major release or migration.

Common mistake to avoid:

Running a technical audit once and never again. Releases, plugins and CDN changes regularly reintroduce old problems.

Why it matters for rankings:

Crawling is the first step to ranking. If Google can't crawl a page efficiently, everything else you do for that page is limited.

Source: https://developers.google.com/search/docs/essentials/technical

🎓 Walk through this whole checklist live, hands-on, in our 4-Day Advanced Technical SEO Workshop Series.
👉 https://www.theseocentral.com/workshops/advanced-technical-seo

#TechnicalSEO #SEOAudit #SEO

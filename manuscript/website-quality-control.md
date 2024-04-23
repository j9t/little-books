# _The Little Book of Website Quality Control_ (2016)

{pagebreak}

## Introduction

> There’s always something professional about doing a thing superlatively well.

—Colonel Pickering, in George Bernard Shaw’s _Pygmalion_

What is a good website? For us web professionals, this is an important question. Building good websites is part of our professionalism, stemming from a code of honor that asserts that we can be professionals only if our work is good.

But how do we know that our work—that our websites—are good? Many criteria and examinations come to mind, but there’s an entire field dedicated to informing us: _quality management._

Quality management, which can be broken down into quality planning, quality assurance, quality control, and quality improvement, comes with a host of methods not just to identify (control) and fix (improvement) defects, but to avoid them systematically (planning, assurance).

This little book focuses mostly on the quality control piece, for if we can’t “see” what’s wrong, we won’t fix or plan to avoid what’s wrong. Still, it’s going to share advice on how to tie quality to our processes, for it _is_ more useful to learn how to fish than to hope to be fed every day. The book does all of this in a loose and relaxed manner, however, and not to the extent ISO standards would cover quality.

Finally, and although this should matter only in few instances, the book hinges more on websites than web apps. That [distinction](https://meiert.com/en/blog/docs-and-apps/) is usually relevant when it comes to standards and development best practices, but there are some differences in how one should go about quality checking of sites as opposed to apps. What follows works better and allows for more complete quality control of _websites_.

This is a little book, then, because it’s short. Let’s leave the intro behind.

### Acknowledgments

Quality, as this book aims to show, is such an important matter that it would be surprising if I, writing about the very subject, could not name the people from whom I learned to improve my work. Lars Röwekamp and Jens Schumann, executives of [OPEN KNOWLEDGE](https://www.openknowledge.de/) in Oldenburg, Germany, are the first to come to my mind.

Many more people inspired my work, and many more people helped make this book reality. I thank my former colleague, manager, and friend, Kevin Khaw, for the foreword [for the original edition], and I thank the entire O’Reilly team for their swift, competent, and kind support. If this book turns out well, it’s because of them. Thank you.

{pagebreak}

## What Is Quality Control?

Wikipedia defines [quality control](https://en.wikipedia.org/wiki/Quality_control) (often abbreviated as “QC,” but rarely in this book) as “a process by which entities review the quality of all factors involved in production.” [ISO 9000](https://en.wikipedia.org/wiki/ISO_9000), also via Wikipedia, is said to define quality control as “a part of quality management focused on fulfilling quality requirements.” Google, not attributing the source, understands quality control to be “a system of maintaining standards in manufactured products by testing a sample of the output against the specification.”

We want to use a definition that’s stricter on the one end and more lenient on the other: “Website quality control includes the means to determine a) whether our websites meet our expectations and b) to what degree they meet professional best practices.”

“Means,” then, largely refers to infrastructure—that is, tools. As stated a moment ago, we’ll also look at processes and methods useful to improve, not just measure, the quality of our work.

{pagebreak}

## Why Is Quality Control Important?

Quality control is important because we need to be able to determine whether what we do and produce is any good.

Consistent quality is the mark of the professional. Quality control, therefore, is a key differentiator between professional and amateur work.

Quality control, finally, saves time and money and sometimes nerves, particularly in the long run.

But what are our options to control the quality of our websites? We’ll look at that in detail.

{pagebreak}

## The Great Website Quality Control Rundown

When _you_ think about the quality of websites, what comes to your mind? How would you test—and what would you test for? Take a moment to ponder this question.

We may readily recall _some_ tools and tests known to us from our everyday work. Some of us will think of validators; some may think of linters; and for others, security tests come to mind.

What do we test for? Not only spec compliance, as with validation, or code formatting, as with linters; we can—and probably should, as professionals—test for everything we can get our hands on. Going through what we can get our hands on and showing what tools we have at our disposal is the purpose of this section. For each area, in descending order of importance, we’ll go over why quality control matters and look at available tools and automation options.

The tools are mostly web-based; applications have been left out, and exceptions noted. The idea was not to shoulder the impossible task of listing and evaluating “all” tools, but to provide a ready-to-use starting point to evaluate production sites.

(Despite all diligence exercised in retrieving and evaluating these tools, neither author nor publisher assumes responsibility for the usefulness, accuracy, and reliability of the tools listed.)

### Security

Security can be considered the most important thing to test for. Whatever it is we (or our users) are doing, if the security of it is compromised, we (or our users) are compromised and can be harmed in a number of ways. This can go from losing data (and privacy) to losing the service itself, and possibly much more. We stand and fall with the security of the services we offer.

Security is critical, but it’s also tricky in the light of website quality control. For one, websites—rather than apps—may or may not deal with personal and sensitive information, or ask their users to give such information. For another, security is not trivial to test and not necessarily to be evaluated all from the outside. This leads us to the situation in which, although security is so crucial, there isn’t that much to add outside the context of dedicated information security.

Let’s go over some tools that are available to us (primarily with a focus on those that are web-based). The responsible website owner should employ additional, notably inner-organizational means to ensure that their services and the data those services gather are secure.

I> These resources had been collected in 2016. They were updated and augmented in 2021 with a focus on web-based tools, which is why you now find few extensions, CLI tools, and scripts, as well as no packages. If you like web-based tools, you find even more on one of my websites, [Frontend Dogma](https://frontenddogma.com/tools/), and on one by Stefan Judis, [Tiny Helpers](https://tiny-helpers.dev/).

* [Abuse Contact Lookup](https://viewdns.info/abuselookup/)
* [AES Encrypter](https://www.infoencrypt.com/)
* [Bandwidth Speed Tester](https://www.bandwidthplace.com/)
* [Blowfish Hash Generator](https://hash.online-convert.com/blowfish-generator)
* [Content Security Policy Validator (CSP Validator)](https://cspvalidator.org/)
* [Content Security Policy Validator (Google)](https://csp-evaluator.withgoogle.com/)
* [Cookie Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [Cross-Site WebSocket Hijacking Tester](https://cm2.pw/websocket)
* [CSR Decoder](https://www.sslshopper.com/csr-decoder.html)
* [DNS Analyzer](https://mxtoolbox.com/DNSLookup.aspx)
* [DNS Propagation Checker](https://www.whatsmydns.net/)
* [DNSSEC Checker](https://viewdns.info/dnssec/)
* [Domain or IP Spam Checker](https://check.spamhaus.org/)
* [Download Time Calculator](http://www.whytehouse.com/opener.html)
* [Email Blacklist Checker](https://mxtoolbox.com/blacklists.aspx)
* [FTP Server Tester](https://www.dotcom-tools.com/ftp-test)
* [Hash Generator](https://hashgenerator.de/)
* [HTTP Header Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/request-maker/kajfghlhfkcocafkcjlajldicbikpgnp)
* [HTTP Header Tester](https://www.rexswain.com/httpview.html)
* [HTTP Header Tester (Advanced)](https://www.askapache.com/online-tools/http-headers-tool/)
* [IP Address Trace](https://www.ip-tracker.org/)
* [IP Detector (Frontend Dogma)](https://frontenddogma.com/tools/helpers/ip-detector/)
* [IP Detector (ipleak.net)](https://ipleak.net/)
* [IP History Checker](https://viewdns.info/iphistory/)
* [Malware and Security Scanner](https://sitecheck.sucuri.net/)
* [MD5 Hash Generator](https://www.md5online.org/md5-encrypt.html)
* [MX Lookup](https://mxtoolbox.com/)
* [Network Intrusion Prevention and Analyzer (Kismet; command-line tool)](https://kismetwireless.net/)
* [Network Intrusion Prevention and Analyzer (Snort; command-line tool)](https://www.snort.org/)
* [Password Generator (Arantius.com)](https://tools.arantius.com/password)
* [Password Generator (GRC)](https://www.grc.com/passwords.htm)
* [Password Generator (Packetizer)](https://secure.packetizer.com/pwgen/)
* [Password Security Checker](https://howsecureismypassword.net/)
* [Password Security Checker (GRC)](https://www.grc.com/haystack.htm)
* [PGP Decrypter](https://www.igolder.com/pgp/decryption/)
* [PGP Encrypter](https://www.igolder.com/pgp/encryption/)
* [PGP Key Generator](https://www.igolder.com/pgp/generate-key/)
* [Ping Tool](https://tools.pingdom.com/)
* [Ping Tool (Regional)](https://www.dotcom-tools.com/ping-test)
* [Reverse IP Lookup](https://mxtoolbox.com/ReverseLookup.aspx)
* [Security Analyzer (OWASP Mantra; browser extension)](https://sourceforge.net/projects/getmantra/)
* [Security Leak Victim Checker (Hasso Plattner Institute)](https://sec.hpi.de/ilc/search?lang=en)
* [Security Leak Victim Checker (Have I Been Pwned)](https://haveibeenpwned.com/)
* [SHA-512 Hash Generator](https://hash.online-convert.com/sha512-generator)
* [SPF Record Checker](https://www.spf-record.com/spf-lookup)
* [SQL Injection and Database Checker (command-line tool)](https://sqlmap.org/)
* [SQL Injection Scanner (command-line tool)](https://wiki.owasp.org/index.php/Category:OWASP_SQLiX_Project)
* [SSL Certificate Checker (DigiCert)](https://www.digicert.com/help/)
* [SSL Certificate Checker (SSL Shopper)](https://www.sslshopper.com/ssl-checker.html)
* [SSL Client Checker](https://www.howsmyssl.com/)
* [SSL Scanner (command-line tool)](https://github.com/iSECPartners/sslyze)
* [SSL Server Tester](https://www.ssllabs.com/ssltest/)
* [Traceroute Tool](https://tools.keycdn.com/traceroute)
* [User Identity Generator](https://www.fakenamegenerator.com/gen-random-us-us.php)
* [Virus Scanner](https://www.virustotal.com/gui/home/upload)
* [Wake-on-LAN Service](https://www.dslreports.com/wakeup)
* [Web Application Security Analyzer (command-line tool)](https://github.com/spinkham/skipfish)
* [Web Application Security Analyzer (server application)](https://sourceforge.net/projects/owasp/)
* [Website Blockade Checker for China (Comparitech)](https://www.comparitech.com/privacy-security-tools/blockedinchina/)
* [Website Blockade Checker for China (Dotcom-Tools)](https://www.dotcom-tools.com/china-firewall-test)
* [Website Blockade Checker for England](https://www.blocked.org.uk/)
* [Website Blockade Checker for Iran](https://www.comparitech.com/privacy-security-tools/blockediniran/)
* [Website Blockade Checker for Russia](https://isitblockedinrussia.com/)
* [Website Certificate Fingerprint Checker](https://www.grc.com/fingerprints.htm)
* [Website Monitoring Service](https://www.montastic.com/)
* [Website Privacy Checker](https://webbkoll.dataskydd.net/)
* [Website Scam Checker](https://www.scamadviser.com/)
* [Website Security Checker (Google)](https://transparencyreport.google.com/safe-browsing/search)
* [Website Security Checker (Norton)](https://safeweb.norton.com/)

### Accessibility

[Per Wikipedia](https://en.wikipedia.org/wiki/Accessibility), accessibility “refers to the design of products, devices, services, or environments for people with disabilities”; “the concept of accessible design ensures both ‘direct access’ (i.e., unassisted) and ‘indirect access,’ meaning compatibility with a person’s assistive technology (for example, computer screen readers).”

Accessibility is one of the most important ideas to understand, because the Web is all about accessibility. Accessibility is the Web’s biggest promise. Accessibility has often been linked to making data available to machines—like search engine bots—but it is, first and foremost, about making information available to _people_.

Accessibility legislation exists in many countries, like [Section 508](https://www.section508.gov/) in the United States, [BITV](https://www.gesetze-im-internet.de/bitv_2_0/) in Germany, or [RGAA](https://web.archive.org/web/20151122054135/http://references.modernisation.gouv.fr/rgaa-3-0) in France. The key standards, the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG20/), published by the World Wide Web Consortium (W3C), have gone through two versions and are, though not perfect, robust. There are a good number of tools, as we shall see. And still, accessibility remains one of the industry’s stepchildren.

Independent of whether we would be held legally accountable, accessibility is one of the most impactful things to cater to on our sites.

* [Accessibility Checker (AATT; automated; command-line tool)](https://github.com/paypal/AATT)
* [Accessibility Checker (FAE)](https://fae.disability.illinois.edu/)
* [Accessibility Checker (WAVE)](https://wave.webaim.org/)
* [Accessibility Developer Tools (WebKit browser extension)](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
* [Accessibility, HTML, and Link Checker (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Accessibility Linter](https://accesslint.com/)
* [Accessibility Visualization (script)](https://github.com/Khan/tota11y)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [Breakpoint Viewer](https://www.responsivepx.com/)
* [Colorblind Web Page Filter](https://www.toptal.com/designers/colorfilter)
* [Color Contrast Analyzer (Jonathan Snook)](https://snook.ca/technical/colour_contrast/colour.html)
* [Color Contrast Analyzer (WCAG Contrast Checker; Gecko browser extension)](https://addons.mozilla.org/en-US/firefox/addon/wcag-contrast-checker/)
* [Color Contrast Analyzer (WebAIM)](https://webaim.org/resources/contrastchecker/)
* [Color Deficit Emulation](http://vischeck.com/vischeck/vischeckURL.php)
* [Section 508, WCAG 2.0, and BITV 1.0 Checker](https://achecks.org/checker/)
* [WCAG 2.0 and 2.1 Checker](https://mauve.isti.cnr.it/singleValidation.jsp)
* [WCAG 2.0 Checker (BOIA)](https://www.boia.org/)
* [WCAG 2.0 Checker (Level Access)](https://www.webaccessibility.com/)
* [WCAG 2.0 Checker (TAW)](https://www.tawdis.net/)

### Usability

Usability is also a critical area to focus on when running a website. Because it’s not a technical concern, however, it’s only mentioned in passing. If you’re interested in this and not already familiar with designing and ensuring a usable website, check out some key resources for further information, like [Usability.gov](https://www.usability.gov/), the [Nielsen Norman Group](https://www.nngroup.com/), or [UXmatters](https://www.uxmatters.com/).

### Performance

For the longest time, Google has worked following the mantras, [“every millisecond counts”](https://www.youtube.com/watch?v=aXJklICrFJI) as well as [“fast is better than slow.”](https://web.archive.org/web/20150823063537/https://www.google.com/about/company/philosophy/) And for good reason! Speed is a key factor for a positive user experience—so crucial, in fact, that it’s one of the determinants for customer satisfaction and conversion.

There are many studies that back performance up as important for quality websites, and Six Revisions (with [_Why Website Speed is Important_](https://www.webfx.com/blog/web-design/why-website-speed-is-important/)), Impressive Webs (with [_The Importance of Page Speed_](https://www.impressivewebs.com/importance-of-page-speed-sources/)), and WebSiteOptimization.com (with [_Empirical Study of Web Site Speed on Search Engine Rankings_](http://www.websiteoptimization.com/speed/tweak/website-speed-search-rankings-study/)) provide pointers for a number of them.

Today, test tools abound for performance measuring. Here are some of them:

* [Availability Checker (CurrentlyDown.com)](http://currentlydown.com/)
* [Availability Checker (isitdownrightnow.com)](https://www.isitdownrightnow.com/)
* [Availability Checker (NotOpening.com)](https://notopening.com/)
* [Availability Checker, Regional (InternetSupervision.com)](http://internetsupervision.com/scripts/urlcheck/check.aspx)
* [Availability Checker, Regional (Site24x7)](https://www.site24x7.com/check-website-availability.html)
* [Availability Checker, Regional (Uptime.com)](https://uptime.com/freetools/global-uptime-test)
* [CDN Use Checker](https://seositecheckup.com/tools/cdn-usage-test)
* [Image Performance Analyzer](https://webspeedtest.cloudinary.com/)
* [Load Time and Object Checker](https://www.websiteoptimization.com/services/analyze/)
* [Load Time Checker](http://www.1-hit.com/all-in-one/tool.loading-time-checker.htm)
* [Mobile Readiness Tester](https://ready.mobi/)
* [PageSpeed Results Comparer](https://pagespeed.compare/)
* [Performance and Scalability Tester (command-line tool)](http://tsung.erlang-projects.org/)
* [Website Batch Performance Analyzer](https://batchspeed.com/)
* [Website Browser and Location Speed Tester](https://www.dotcom-tools.com/website-speed-test)
* [Website Performance Analyzer (GTmetrix)](https://gtmetrix.com/)
* [Website Performance Analyzer (KeyCDN)](https://tools.keycdn.com/speed)
* [Website Performance Analyzer (Page Performance; WebKit browser extension)](https://chrome.google.com/webstore/detail/page-performance/gembkfinllgmbkgbgdoaeopbahikjomp)
* [Website Performance Analyzer (PageSpeed)](https://pagespeed.web.dev/)
* [Website Performance Analyzer (Pingdom)](https://tools.pingdom.com/)
* [Website Performance Analyzer (Uptime.com)](https://uptime.com/freetools/website-speed-test)
* [Website Performance Analyzer (Uptrends)](https://www.uptrends.com/tools/website-speed-test)
* [Website Performance Analyzer (Waterfaller)](https://waterfaller.dev/)
* [Website Performance Analyzer (wattspeed)](https://www.wattspeed.com/)
* [Website Performance Analyzer (WebPageTest)](https://www.webpagetest.org/)
* [Website Performance Analyzer (YSlow; browser extension)](http://yslow.org/)

### Functionality

Another user-centered matter concerns site functionality and navigation: Can we get from _A_ to _B_? Fortunately, even though this is important to ensure, it’s easy to verify—so easy that most of the time, functionality testing is “implied.”

How so? What have I just said? Essentially, when we build and extend our sites and their functionality, we know whether we can access what we just built and extended. For example, when we add a new registration page or post a new press release, we typically notice, as part of the testing and launch process, whether page or release actually made it live and can be found.

It’s advantageous to tell whether everything’s where we expect it to be, and whether it works as we expect it to work. Here are some tools to do that:

* [Accessibility, HTML, and Link Checker (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Browser Test Automator (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automator (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automator (Squish)](http://www.froglogic.com/)
* [Design Responsiveness Tester (Am I Responsive)](http://ami.responsivedesign.is/)
* [Design Responsiveness Tester (Website Planet)](https://www.websiteplanet.com/webtools/responsive-checker/)
* [Link and Image Checker](https://www.internetmarketingninjas.com/tools/broken-links-tool/)
* [Link Checker (Dead Link Checker)](https://www.deadlinkchecker.com/)
* [Link Checker (Dr. Link Check)](https://www.drlinkcheck.com/)
* [Link Checker (LinkTiger)](http://www.linktiger.com/)
* [Link Checker (W3C)](https://validator.w3.org/checklink)
* [Sitemap Checker](https://seositecheckup.com/tools/sitemap-test)
* [UI Test Automator (Ghost Inspector; browser extension)](https://ghostinspector.com/)
* [UI Test Automator (Screenster)](https://screenster.io/)
* [Web App Test Automator (command-line tool)](https://github.com/svenfuchs/steam)

### Maintainability

The first technical priority to watch out for is maintainability. Maintainability? Yes, our ability to efficiently make changes to our design and code. This degree, this efficiency, makes for one of the most crucial aspects of web development—and at the same time it’s regularly among the most neglected ones.

What is maintainability, what does this ability and efficiency refer to? That’s a valid question given that many long years of neglect have yielded little documentation and few best practices pertaining to maintainability and maintenance. [“One cannot not maintain”](https://meiert.com/en/blog/law-of-maintainability/)—that’s a “law” I once coined in despair. “One cannot not maintain” originates in the fact that anything we produce must at some point be dealt with again, whether by us or by others.

As for tools, we’re in need of more of them:

* [CMS Detector](https://whatcms.org/)
* [QA Style Sheet (bookmarklet)](https://github.com/j9t/qa-style-sheet)
* [Website Technology Analyzer (BuiltWith)](https://builtwith.com/)
* [Website Technology Analyzer (My Codeless Website)](https://mycodelesswebsite.com/)
* [WordPress Plugin Detector](http://wppluginchecker.earthpeople.se/)
* [WordPress Theme Detector](https://www.wpthemedetector.com/)

### Semantics

Semantics was one of the hot topics of the last decade, when the field of web development went through its first stage of maturation and developed a better sense for how HTML markup should be written. This awareness was motivated in part by a higher regard for web standards—largely in relation to the underlying specifications—and in part by stronger emphasis on the need for websites to be more accessible.

Today, the hype has moved on to web apps, and tolerance has stretched again to “anything goes.” [WAI-ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) has grown and matured as both tool and excuse. [Microdata](https://html.spec.whatwg.org/multipage/microdata.html) and [web components](https://www.webcomponents.org/) have, so far, also contributed to a flourishing mindset of “semantics is not important anymore.”

Is this all justified? No. But the situation is complex. To make more sense of it, let’s break things up.

For semantics, we should look at where it’s coming from and what people mean when they talk about it. [Semantics in HTML](https://meiert.com/en/blog/on-semantics-in-html/) refers to authority—and consensus-based meaning. The W3C or the WHATWG—the authorities—define in specifications what each element and attribute means. Vendors as well as community buy into these definitions. Sometimes they disagree (voiced in standard controversies), or push their own solutions (as with [microformats](https://microformats.org/)). ID and class names represent the most minimal form of consensus on meaning (well by a single developer).

For new technology and techniques, we find ourselves in a conflict. The standards community has given in to a form of arms race against itself. After years of slow progress, low output, and seeming indifference to the user and vendor community, suddenly those involved in standards want to push _everything_ forward. This has led the specifications to grow in number and size, and we still haven’t been able to take inventory of everything we’re now capable of doing. With that growing complexity, we risk losing it all, or [so I feel](https://meiert.com/en/blog/fing-up-standards/). But with respect to semantics, we’re right at the seam, and things have become loose there. Few focus on the _meaning_ of what documents and templates describe anymore. Divitis everywhere.

Semantics will make it back to our agendas for the following reason: We can only get the most out of code and information within code, ensure best access to that code, and work best together on code if the code has meaning, or is used according to its assigned meaning.

There are a number of semantics checks and generators for enriched markup:

* [Facebook Validator](https://developers.facebook.com/tools/debug/)
* [Google Structured Data Tester](https://developers.google.com/search/docs/advanced/structured-data)
* [hCalendar Generator](https://microformats.org/code/hcalendar/creator)
* [hCard Generator](https://microformats.org/code/hcard/creator)
* [HTML Outline Extractor](https://gsnedders.html5.org/outliner/)
* [LinkedIn Validator](https://www.linkedin.com/post-inspector/)
* [Metadata Viewer](https://www.extractmetadata.com/)
* [Microformats Analyzer](https://php.microformats.io/)
* [Schema Generator](https://seoscout.com/tools/schema-generator)
* [Semantics Parser and Extractor](http://buzzword.org.uk/swignition/try)
* [Twitter Card Tester](https://cards-dev.twitter.com/validator)

(Some accessibility and validation tools cover aspects of semantics, too; to avoid repetition and not distort the view on the “purely semantic” testing options, these have not been duplicated here.)

### Validation

Validation as a measurable priority had peaked, too, before [falling from grace](https://meiert.com/en/blog/valid-html-2021/). But popularity doesn’t correlate with quality, and one can build a strong case for validation—conformance—as a fundamental factor for website quality. It’s such an important factor for that reason that only validation ensures that we’ve been producing code according to the specs (and that we know our business).

Although this is a powerful argument for validation, the web development landscape begs to differ—especially when it comes to HTML and CSS.

HTML, then, is more stable and used in more places than CSS. CSS is under heavier development and occasionally experimental, yet style sheets live in relatively few places (CSS being “orthogonal” to HTML makes for its significance around maintainability). That means that HTML validation is more important than CSS validation. Because HTML is stable, it’s easier to validate, and because it’s so ubiquitous, it’s also more critical to validate.

We are in the envious situation of having a great many, good-quality validators at our disposal:

* [Accessibility, HTML, and Link Checker (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [CSS Validator (W3C)](https://jigsaw.w3.org/css-validator/)
* [CSS Validator (WDG)](https://www.htmlhelp.com/tools/csscheck/)
* [DAML Validator](http://www.daml.org/validator/)
* [hCard Validator](https://indiewebify.me/validate-h-card/)
* [.htaccess Validator](https://shop.alterlinks.com/htaccess-validator/htaccess-validator.php)
* [HTML 5 Validator](https://html5.validator.nu/)
* [HTML Validator](https://validator.w3.org/)
* [JSON Validator (FreeFormatter.com)](https://www.freeformatter.com/json-validator.html)
* [JSON Validator (JSONCompare)](https://jsoncompare.com/)
* [P3P Validator](https://www.w3.org/P3P/validator.html)
* [RDF Validator](https://www.w3.org/RDF/Validator/)
* [robots.txt Validator (Merkle)](https://technicalseo.com/tools/robots-txt/)
* [robots.txt Validator (Ryte)](https://en.ryte.com/free-tools/robots-txt/)
* [RSS and Atom Feed Validator](https://validator.w3.org/feed/)
* [SBML Validator](http://sbml.org/Facilities/Validator/)
* [Sitemap Validator](https://www.xml-sitemaps.com/validate-xml-sitemap.html)
* [SVG Validator](http://steltenpower.com/svgref.php)
* [XML Schema Validator](https://schneegans.de/sv/)
* [XML Validator](https://www.xmlvalidation.com/)
* [XML Well-Formedness Checker and Validator](https://www.cogsci.ed.ac.uk/~richard/xml-check.html)
* [XML-RPC Validator](http://scripting.com/code/xmlrpcbrowserclient/)

### Layout and Design Consistency

Normally filed under other categories, consistency-checking is also a factor in website quality control. What is it normally filed under? Browser testing. That’s, as we’ve noticed, a misnomer: We’re not testing browsers, we’re testing the layout and design of our websites for consistency across browsers and devices.

The differentiation makes clear what tools we can use: browser and device emulators, of which there are plenty. That testing landscape has changed significantly over the years. Although it has become a challenge to test for the slew of devices, web-based tools that allow quick comparisons have matured to the extent that we have to install fewer user agents than we used to.

(The change to always up-to-date, evergreen browsers as well as “consolidation” of rendering engines have led to improvements, too. For example, consider how [WebKit](https://webkit.org/) ~~is~~ was by far the most common engine [nowadays, it’s [Blink](https://en.wikipedia.org/wiki/Blink_(browser_engine))].)

To test layout and design, we can use tools and services like the following:

* [Android and iOS Emulators](https://appetize.io/)
* [Browser Screenshots for Windows and Android](https://www.browserling.com/)
* [Browser Screenshots for Windows, macOS, and Linux](https://browsershots.org/)
* [Browser Screenshots for Windows, macOS, Android, and iOS](https://www.browserstack.com/screenshots)
* [Browser Test Automator (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automator (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automator (Squish)](http://www.froglogic.com/)
* [Design Diff (script)](https://percy.io/)
* [Edge Compatibility Tester](http://doesitworkonedge.com/)
* [Internet Explorer Viewer (IE NetRenderer)](https://netrenderer.com/)
* [Internet Explorer Viewer (URL2PNG)](https://www.url2png.com/)
* [Layout Bug Tester (script)](https://code.google.com/archive/p/fighting-layout-bugs/)
* [Lynx Viewer](http://www.delorie.com/web/lynxview.html)
* [Mobile Emulator](http://mtld.mobi/emulator.php)
* [Opera Mini Emulator](http://opr.as/2cKpahy)
* [Progressive Web App Feature Detector](https://tomayac.github.io/pwa-feature-detector/)
* [User Agent Detector](https://ua.met.cz/)
* [Viewport Emulator](http://www.viewportemulator.com/)
* [Viewport Size Determiner](https://www.internetmarketingninjas.com/tools/whats-my-browser-size/)

### Typography

Typography is not what the common website owner may connect with website quality—and neither may every designer—but it’s an important aspect of every website. Typography is all the more important as the amount of website content increases—think of Robert Bringhurst, who taught that “typography exists to honor content.”

But why test? Obviously, for the reasons that typography matters—and so we’re not merely running into William Bruce Cameron’s (not Albert Einstein’s) famous statement, “Not everything that counts can be counted, and not everything that can be counted counts.” Typography can be counted, and typography does count. Not many tools are available to test for good typography, but still there are some that make our typographic work easier:

* [Font Capability Checker](https://wakamaifondue.com/)
* [Font Comparer](https://www.fontcomparer.com/)
* [Font Determiner (WhatFont; WebKit browser extension)](http://www.chengyinliu.com/whatfont.html)
* [Font Determiner (WhatTheFont)](https://www.myfonts.com/WhatTheFont/)
* [Font Determiner, Live](https://qwerty.dev/)
* [Font Diff](https://tiff.herokuapp.com/)
* [Font Fallback Determiner (bookmarklet)](http://www.hotelscrete.net/ffffallbackcom/)
* [Font Family Support Checker](http://fontfamily.io/)
* [Font Pairing Tester](https://fontjoy.com/)
* [Font Style Matcher](https://meowni.ca/font-style-matcher/)
* [Font Tester](https://play.typedetail.com/)
* [Golden Ratio Typography Calculator](https://grtcalculator.com/)
* [Text Decoration Generator](https://yaytext.com/)
* [Type Scale Generator (Jeremy Church)](https://typescale.com/)
* [Type Scale Generator (Tim Brown)](https://www.modularscale.com/)
* [Web Font Generator](https://www.fontsquirrel.com/tools/webfont-generator)

### Code Quality

Venturing again into the realm that’s invisible to the users of our sites, code quality has many attributes, some of which we’ve already addressed. Here, code quality touches on general overall checks, as well as on _linting_—that is, analyzing code for potential programmatic and stylistic errors (which we’ll focus on separately, in the next section).

Linting comes out of computer programming—something we haven’t traditionally filed web development under—but linters are by now available for pretty much anything, including CSS. Quality-related tools include the following:

* [Accessibility Linter](https://accesslint.com/)
* [Content-to-Code Ratio Calculator](https://www.duplichecker.com/code-to-text-ratio-checker.php)
* [CSS Analyzer (CSS Stats)](https://cssstats.com/)
* [CSS Analyzer (Lea Verou)](https://projects.verou.me/rework-utils/)
* [CSS Efficiency Checker](https://unused-css.com/)
* [CSS Linter](http://csslint.net/)
* [Internationalization Checker](https://validator.w3.org/i18n-checker/)
* [JavaScript Linter (JSHint)](https://jshint.com/)
* [JavaScript Linter (JSLint)](https://www.jslint.com/)
* [JavaScript Linter (ValidateJavaScript)](https://validatejavascript.com/)
* [Reputation and Safety Checker](https://www.mywot.com/)
* [Website Analyzer (Accessify)](https://www.accessify.com/)
* [Website Analyzer (Easy Counter)](https://www.easycounter.com/)
* [Website Analyzer (Frontend Dogma)](https://frontenddogma.com/tools/check/)
* [Website Analyzer (Mozilla)](https://observatory.mozilla.org/)
* [Website Analyzer (Nibbler)](https://nibbler.silktide.com/)
* [Website Analyzer (Open Admin Tools)](https://www.openadmintools.com/)
* [Website Analyzer (Site Analyzer)](https://www.site-analyzer.com/)
* [Website Analyzer (StatsCrop)](https://www.statscrop.com/)
* [Website Analyzer (Yellow Lab Tools)](https://yellowlab.tools/)
* [Website Grader](https://website.grader.com/)
* [Website Review](https://www.valuemyweb.com/reviewmyweb/reviewmyweb)
* [YAML Linter](https://codebeautify.org/yaml-validator)

### Coding Standard Compliance

Last but not least and not to be missed: We want to and we can measure the conformity and consistency of our code. For that—you may remember _The Little Book of HTML/CSS Coding Guidelines_—we look at common coding practices, and, notably, our coding guidelines.

The listed quality checks look at compliance, comparing code strings against predefined catalogs of rules. Only lowercase element names in HTML? Only single quotes in CSS? No global variables in JavaScript? No BOM in text files? This is done by website quality checks against code standards, such as the following:

* [Code Formatter (Code Beautifier)](https://ctrlq.org/beautifier/)
* [Code Formatter (Pretty Printer)](http://prettyprinter.de/)
* [CSS Formatter (Dan’s Tools)](https://www.cleancss.com/css-beautify/)
* [CSS Formatter (Lonnie Best)](http://www.lonniebest.com/FormatCSS/)
* [CSS Formatter and Minifier](https://www.cssportal.com/css-formatter/index.php)
* [CSS Formatter and Optimizer](https://www.tenman.info/csstidy/css_optimiser.php)
* [HTML, CSS, and JS Formatter](https://www.10bestdesign.com/dirtymarkup/)
* [HTML Formatter](https://www.freeformatter.com/html-formatter.html)
* [HTML Optimizer (HTML De-crapulator)](https://a11y-tools.com/markup-de-crapulator/)
* [HTML Optimizer (HtmlWasher)](https://www.htmlwasher.com/)
* [JSON Formatter (Curious Concept)](https://jsonformatter.curiousconcept.com/)
* [JSON Formatter (FracturedJson)](https://j-brooke.github.io/FracturedJson/)
* [JSON Formatter and Minifier](https://jsoncompare.com/)
* [SQL Formatter](https://www.freeformatter.com/sql-formatter.html)
* [XML Formatter](https://www.freeformatter.com/xml-formatter.html)

After we have properly formatted our code and made it consistent, we still want to make it production-ready by compressing and minifying it. Our work files should be easy (to understand) for us, and our production files should be easy (to parse and transfer) for others. For this there are additional tools.

* [CSS Minifier](https://csscompressor.net/)
* [HTML Minifier](https://htmlcompressor.com/compressor/)
* [HTML Optimizer and Minifier](https://kangax.github.io/html-minifier/)
* [JavaScript Minifier](https://jscompress.com/)

{pagebreak}

## Quality Control in Practice

With the overview and tools we’ve gathered, what does quality control of websites look like in practice? Is this all we need? What pitfalls are there? What do we need to watch out for? There are indeed a few things to consider.

### Training

Training is an important first step toward successfully implementing quality control practices. Training should be understood generally here, for any professional training that teaches people how to produce better work benefits quality, too. In that sense, training will not be elaborated on here.

However, training can also be offered and attended specifically to promote attention to quality, to learn about quality-related processes, and to master tools that measure and improve quality. (As such, training is also linked to the following points, but won’t be called out again.)

### Mindset

The most important factor when it comes to quality in practice is the mindset. The greatest quality initiative is not worth much if it’s not clear to the team and enterprise why quality matters, and how quality is beneficial everyone. The key to a quality mindset is communication; a potential trap are rewards.

#### Communication

Communication is the primary way to spread and instill quality as a goal and guiding principle.

This communication should sporadically be repeated, but doesn’t need to solely consist of reminders on why quality matters and how it benefits everybody. If we want to repeat the essence of both answers here, then: Quality is important in order to deliver work that’s good by professional standards and that benefits everyone, because products of quality are easier and more pleasant to consume and work with.

Communication is, for that reason, important because we benefit from being reminded of our priorities.

Based on this, communication can now range from bylines in regular team and company communications, thanking everyone for the vigilance to produce good work, to dedicated emails emphasizing the goal and importance of quality.

#### Rewards

Rewards, then, are _no_ key for a quality mindset. We should avoid rewards. As with any form of extrinsic motivation, rewards can compel people to participate in quality-related events, but they don’t necessarily compel people to embrace quality. They can instead have the opposite effect and distract from, rather than point to the message.

I’ve had some such experiences with international teams, when rewards helped draw attention to quality programs, but didn’t lead to a better understanding of quality, or a higher motivation to achieve high quality. What was more effective was communication, particularly through managers. Hierarchy and authority can be facilitators in our quest to improve the quality of our work.

### Automation

Insist on automation. Insist—on automation. _Of course_, we’re inclined to say—once we’ve automated all quality-relevant tasks and processes, what’s there to be missed, how could we get anything wrong? But we haven’t progressed yet to the point that we’re able to automate everything. Our reality is that not enough is being automated, and sensitizing for that is what this very practical recommendation aims at. We must automate as much as we can; we must insist on automation.

We have discussed many tools, and we’re going to summarize them. Some of the tools are easy to implement and automate, but others, per our goal to automate and _insist_ to automate, require a bit of an effort. A discussion on how to write and run automation scripts on different platforms is beyond the scope of this little book, but if you’d like to see what that can look like, check out complementary books like [_Learning Linux Shell Scripting_](https://www.amazon.com/dp/B013WWYVHK/?tag=meiert-20), [_Network Programmability and Automation_](https://www.amazon.com/dp/1491931256/?tag=meiert-20), or [_Learn AppleScript_](https://www.amazon.com/dp/1430223618/?tag=meiert-20).

### Enforcement

In the context of coding guidelines, we’ve learned to differentiate between descriptive or positive guidelines and those that are prescriptive or normative (see _The Little Book of HTML/CSS Coding Guidelines_). The difference is mostly practical—when code quality is at a high level, we merely document (describe) what everyone’s already doing; when code quality is low, we tell everyone what to do (prescribe). However, as it pertains to much of what we’ve discussed so far, this requires some way of enforcement.

How do we enforce quality? This is still a difficult question; so difficult, in fact, that in practice we often see it dodged. Why? Because enforcement easily upsets people, and we don’t want to upset people, not even—or especially—when they report to us. But we’re on the right track here.

Enforcement happens top-down. Executives and managers are to emphasize and _live_ quality, to reward good quality, and to—in one way or another—discourage poor quality. How? By doing what we frequently miss: measuring quality and tying related metrics to performance evaluations.

Two anecdotes illustrate that approach. There’s one tale of a manager who has, despite efforts of their team to up the ante and increase quality in their department, never endorsed, let alone supported or encouraged those team members’ efforts in team communications or goals. That quality initiative’s efforts, witnessed at one point at a major corporation, never felt like they gained the traction they could have gained.

At the same firm at another time, managers called out the importance of quality and used available data points, like performance scores as measured by [Google’s PageSpeed tools](https://developers.google.com/speed), accessibility problems as measured by [Sidar’s HERA](https://web.archive.org/web/20150726041535/http://www.sidar.org/hera/), or the number of validation errors as measured by [W3C’s Link Checker](https://validator.w3.org/checklink). Although the team in question never got to tie metrics like these to performance evaluations, that precise step was anticipated to encourage and lead to—enforce—higher quality.

### Logistics

In broad terms, our efforts around quality require logistics. These might consist of the following, listed briefly for inspiration:

Standards and guidelines documentation: No quality effort can succeed without standards and guidelines. These can be external, but wherever they can be found, they must be linked or spelled out.

Meta documentation: What our quality efforts require and entail must also be documented. That…

Internal websites or wikis: …is best done on some internal website or wiki. Here, we should gather everything we want, know, do, and plan.

Dedicated contacts: Quality stands and falls with people. At least one person should serve as a contact, and they must not only be responsible and accountable, but also discoverable and available.

Mailing lists: To coordinate quality efforts, communicate new and updated documentation, and so on, mailing lists are a crucial tool. There can be lists for quality-focused teams, as well as lists open to the entire enterprise.

Events: Google has a practice to host “fixits” or “fixlets,” events that let the company or departments clean up and improve their work and code base, but quality events can range from a toast on quality at the daily Scrum meeting to company representatives speaking about quality at industry conferences.

The more a quality initiative grows and matures, the more tools and methods it may employ. This here describes the basic options.

{pagebreak}

## Tools Overview

The following serves as an overview of web-based tools, browser extensions, command-line tools, scripts, and bookmarklets. It’s not complete; it lacks important tools; but many tools come with my endorsement, and the promise to serve you.

I> These resources had been collected in 2016. They were updated and augmented in 2021 with a focus on web-based tools, which is why you now find few extensions, CLI tools, and scripts, as well as no packages. If you like web-based tools, you find even more on one of my websites, [Frontend Dogma](https://frontenddogma.com/tools/), and on one by Stefan Judis, [Tiny Helpers](https://tiny-helpers.dev/).

* [Abuse Contact Lookup](https://viewdns.info/abuselookup/)
* [Accessibility Checker (AATT; automated; command-line tool)](https://github.com/paypal/AATT)
* [Accessibility Checker (FAE)](http://fae20.cita.illinois.edu/)
* [Accessibility Checker (WAVE)](https://wave.webaim.org/)
* [Accessibility Developer Tools (WebKit browser extension)](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
* [Accessibility, HTML, and Link Checker (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Accessibility Linter](https://accesslint.com/)
* [Accessibility Visualization (script)](https://github.com/Khan/tota11y)
* [AES Encrypter](http://www.infoencrypt.com/)
* [Android and iOS Emulators](https://appetize.io/)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [Availability Checker (CurrentlyDown.com)](http://www.currentlydown.com/)
* [Availability Checker (isitdownrightnow.com)](https://www.isitdownrightnow.com/)
* [Availability Checker (NotOpening.com)](https://notopening.com/)
* [Availability Checker, Regional (InternetSupervision.com)](http://internetsupervision.com/scripts/urlcheck/check.aspx)
* [Availability Checker, Regional (Site24x7)](https://www.site24x7.com/check-website-availability.html)
* [Availability Checker, Regional (Uptime.com)](https://uptime.com/freetools/global-uptime-test)
* [Bandwidth Speed Tester](http://www.bandwidthplace.com/)
* [Blowfish Hash Generator](http://hash.online-convert.com/blowfish-generator)
* [Breakpoint Viewer](https://www.responsivepx.com/)
* [Browser Screenshots for Windows and Android](https://www.browserling.com/)
* [Browser Screenshots for Windows, macOS, and Linux](https://browsershots.org/)
* [Browser Screenshots for Windows, macOS, Android, and iOS](https://www.browserstack.com/screenshots)
* [Browser Test Automator (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automator (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automator (Squish)](http://www.froglogic.com/)
* [CDN Use Checker](https://seositecheckup.com/tools/cdn-usage-test)
* [CMS Detector](https://whatcms.org/)
* [Code Formatter (Code Beautifier)](https://ctrlq.org/beautifier/)
* [Code Formatter (Pretty Printer)](http://prettyprinter.de/)
* [Color Contrast Analyzer (Jonathan Snook)](https://snook.ca/technical/colour_contrast/colour.html)
* [Color Contrast Analyzer (WCAG Contrast Checker; Gecko browser extension)](http://mzl.la/2cmVY1A)
* [Color Contrast Analyzer (WebAIM)](http://webaim.org/resources/contrastchecker/)
* [Color Deficit Emulation](http://www.vischeck.com/vischeck/vischeckURL.php)
* [Colorblind Web Page Filter](https://www.toptal.com/designers/colorfilter)
* [Content Security Policy Validator (CSP Validator)](https://cspvalidator.org/)
* [Content Security Policy Validator (Google)](https://csp-evaluator.withgoogle.com/)
* [Content-to-Code Ratio Calculator](https://www.duplichecker.com/code-to-text-ratio-checker.php)
* [Cookie Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [Cross-Site WebSocket Hijacking Tester](https://cm2.pw/websocket)
* [CSR Decoder](http://www.sslshopper.com/csr-decoder.html)
* [CSS Analyzer (CSS Stats)](https://cssstats.com/)
* [CSS Analyzer (Lea Verou)](https://projects.verou.me/rework-utils/)
* [CSS Efficiency Checker](https://unused-css.com/)
* [CSS Formatter (Dan’s Tools)](https://www.cleancss.com/css-beautify/)
* [CSS Formatter (Lonnie Best)](http://www.lonniebest.com/FormatCSS/)
* [CSS Formatter and Minifier](https://www.cssportal.com/css-formatter/index.php)
* [CSS Formatter and Optimizer](https://www.tenman.info/csstidy/css_optimiser.php)
* [CSS Linter](http://csslint.net/)
* [CSS Minifier](https://csscompressor.net/)
* [CSS Validator (W3C)](https://jigsaw.w3.org/css-validator/)
* [CSS Validator (WDG)](https://www.htmlhelp.com/tools/csscheck/)
* [DAML Validator](http://www.daml.org/validator/)
* [Design Diff (script)](https://percy.io/)
* [Design Responsiveness Tester (Am I Responsive)](http://ami.responsivedesign.is/)
* [Design Responsiveness Tester (Website Planet)](https://www.websiteplanet.com/webtools/responsive-checker/)
* [DNS Analyzer](https://mxtoolbox.com/DNSLookup.aspx)
* [DNS Propagation Checker](http://www.whatsmydns.net/)
* [DNSSEC Checker](https://viewdns.info/dnssec/)
* [Domain or IP Spam Checker](https://check.spamhaus.org/)
* [Download Time Calculator](http://www.whytehouse.com/opener.html)
* [Edge Compatibility Tester](http://doesitworkonedge.com/)
* [Email Blacklist Checker](http://mxtoolbox.com/blacklists.aspx)
* [Facebook Validator](https://developers.facebook.com/tools/debug/)
* [Font Capability Checker](https://wakamaifondue.com/)
* [Font Comparer](https://www.fontcomparer.com/)
* [Font Determiner (WhatFont; WebKit browser extension)](http://www.chengyinliu.com/whatfont.html)
* [Font Determiner (WhatTheFont)](https://www.myfonts.com/WhatTheFont/)
* [Font Determiner, Live](https://qwerty.dev/)
* [Font Diff](https://tiff.herokuapp.com/)
* [Font Fallback Determiner (bookmarklet)](http://www.hotelscrete.net/ffffallbackcom/)
* [Font Family Support Checker](http://fontfamily.io/)
* [Font Pairing Tester](https://fontjoy.com/)
* [Font Style Matcher](https://meowni.ca/font-style-matcher/)
* [Font Tester](https://play.typedetail.com/)
* [FTP Server Tester](http://www.dotcom-tools.com/ftp-server-test.aspx)
* [Golden Ratio Typography Calculator](https://grtcalculator.com/)
* [Google Structured Data Tester](https://developers.google.com/search/docs/advanced/structured-data)
* [Hash Generator](https://hashgenerator.de/)
* [hCalendar Generator](https://microformats.org/code/hcalendar/creator)
* [hCard Generator](https://microformats.org/code/hcard/creator)
* [hCard Validator](https://indiewebify.me/validate-h-card/)
* [.htaccess Validator](https://shop.alterlinks.com/htaccess-validator/htaccess-validator.php)
* [HTML 5 Validator](https://html5.validator.nu/)
* [HTML, CSS, and JS Formatter](https://www.10bestdesign.com/dirtymarkup/)
* [HTML Formatter](https://www.freeformatter.com/html-formatter.html)
* [HTML Minifier](https://htmlcompressor.com/compressor/)
* [HTML Optimizer (HTML De-crapulator)](https://a11y-tools.com/markup-de-crapulator/)
* [HTML Optimizer (HtmlWasher)](https://www.htmlwasher.com/)
* [HTML Optimizer and Minifier](https://kangax.github.io/html-minifier/)
* [HTML Outline Extractor](http://gsnedders.html5.org/outliner/)
* [HTML Validator](https://validator.w3.org/)
* [HTTP Header Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/request-maker/kajfghlhfkcocafkcjlajldicbikpgnp)
* [HTTP Header Tester](http://www.rexswain.com/httpview.html)
* [HTTP Header Tester (Advanced)](https://www.askapache.com/online-tools/http-headers-tool/)
* [Image Performance Analyzer](https://webspeedtest.cloudinary.com/)
* [Internationalization Checker](https://validator.w3.org/i18n-checker/)
* [Internet Explorer Viewer (IE NetRenderer)](https://netrenderer.com/)
* [Internet Explorer Viewer (URL2PNG)](https://www.url2png.com/)
* [IP Address Trace](http://www.ip-tracker.org/)
* [IP Detector (Frontend Dogma)](https://frontenddogma.com/tools/helpers/ip-detector/)
* [IP Detector (ipleak.net)](https://ipleak.net/)
* [IP History Checker](https://viewdns.info/iphistory/)
* [JavaScript Linter (JSHint)](https://jshint.com/)
* [JavaScript Linter (JSLint)](https://www.jslint.com/)
* [JavaScript Linter (ValidateJavaScript)](https://validatejavascript.com/)
* [JavaScript Minifier](https://jscompress.com/)
* [JavaScript Savings Analyzer](https://estimator.dev/)
* [JSON Formatter (Curious Concept)](https://jsonformatter.curiousconcept.com/)
* [JSON Formatter (FracturedJson)](https://j-brooke.github.io/FracturedJson/)
* [JSON Formatter and Minifier](https://jsoncompare.com/)
* [JSON Validator (FreeFormatter.com)](https://www.freeformatter.com/json-validator.html)
* [JSON Validator (JSONCompare)](https://jsoncompare.com/)
* [Layout Bug Tester (script)](https://code.google.com/archive/p/fighting-layout-bugs/)
* [Link and Image Checker](https://www.internetmarketingninjas.com/tools/broken-links-tool/)
* [Link Checker (Dead Link Checker)](https://www.deadlinkchecker.com/)
* [Link Checker (Dr. Link Check)](https://www.drlinkcheck.com/)
* [Link Checker (LinkTiger)](http://www.linktiger.com/)
* [Link Checker (W3C)](https://validator.w3.org/checklink)
* [LinkedIn Validator](https://www.linkedin.com/post-inspector/)
* [Load Time and Object Checker](https://www.websiteoptimization.com/services/analyze/)
* [Load Time Checker](http://www.1-hit.com/all-in-one/tool.loading-time-checker.htm)
* [Lynx Viewer](http://www.delorie.com/web/lynxview.html)
* [Malware and Security Scanner](https://sitecheck.sucuri.net/)
* [MD5 Hash Generator](https://www.md5online.org/md5-encrypt.html)
* [Metadata Viewer](https://www.extractmetadata.com/)
* [Microformats Analyzer](https://php.microformats.io/)
* [Mobile Emulator](http://mtld.mobi/emulator.php)
* [Mobile Readiness Tester](https://ready.mobi/)
* [MX Lookup](https://mxtoolbox.com/)
* [Network Intrusion Prevention and Analyzer (Kismet; command-line tool)](https://kismetwireless.net/)
* [Network Intrusion Prevention and Analyzer (Snort; command-line tool)](https://www.snort.org/)
* [Opera Mini Emulator](http://opr.as/2cKpahy)
* [P3P Validator](https://www.w3.org/P3P/validator.html)
* [PageSpeed Results Comparer](https://pagespeed.compare/)
* [Password Generator (Arantius.com)](https://tools.arantius.com/password)
* [Password Generator (GRC)](https://www.grc.com/passwords.htm)
* [Password Generator (Packetizer)](https://secure.packetizer.com/pwgen/)
* [Password Security Checker](https://howsecureismypassword.net/)
* [Password Security Checker (GRC)](https://www.grc.com/haystack.htm)
* [Performance and Scalability Tester (command-line tool)](http://tsung.erlang-projects.org/)
* [PGP Decrypter](http://www.igolder.com/pgp/decryption/)
* [PGP Encrypter](http://www.igolder.com/pgp/encryption/)
* [PGP Key Generator](http://www.igolder.com/pgp/generate-key/)
* [Ping Tool](http://tools.pingdom.com/ping/)
* [Ping Tool (Regional)](https://www.dotcom-tools.com/ping-test)
* [Progressive Web App Feature Detector](https://tomayac.github.io/pwa-feature-detector/)
* [QA Style Sheet (bookmarklet)](https://github.com/j9t/qa-style-sheet)
* [RDF Validator](https://www.w3.org/RDF/Validator/)
* [Reputation and Safety Checker](https://www.mywot.com/)
* [Reverse IP Lookup](http://mxtoolbox.com/ReverseLookup.aspx)
* [robots.txt Validator (Merkle)](https://technicalseo.com/tools/robots-txt/)
* [robots.txt Validator (Ryte)](https://en.ryte.com/free-tools/robots-txt/)
* [RSS and Atom Feed Validator](https://validator.w3.org/feed/)
* [SBML Validator](http://sbml.org/Facilities/Validator/)
* [Schema Generator](http://schema-creator.org/)
* [Section 508, WCAG 2.0, and BITV 1.0 Checker](https://achecks.org/checker/)
* [Security Analyzer (OWASP Mantra; browser extension)](https://sourceforge.net/projects/getmantra/)
* [Security Leak Victim Checker (Hasso Plattner Institute)](https://sec.hpi.de/ilc/search?lang=en)
* [Security Leak Victim Checker (Have I Been Pwned)](https://haveibeenpwned.com/)
* [Semantics Parser and Extractor](http://buzzword.org.uk/swignition/try)
* [SHA-512 Hash Generator](https://hash.online-convert.com/sha512-generator)
* [Sitemap Checker](https://seositecheckup.com/tools/sitemap-test)
* [Sitemap Validator](https://www.xml-sitemaps.com/validate-xml-sitemap.html)
* [SPDY Implementation Checker](http://spdycheck.org/)
* [SPF Record Checker](https://www.spf-record.com/spf-lookup)
* [SQL Formatter](https://www.freeformatter.com/sql-formatter.html)
* [SQL Injection and Database Checker (command-line tool)](http://sqlmap.org/)
* [SQL Injection Scanner (command-line tool)](https://wiki.owasp.org/index.php/Category:OWASP_SQLiX_Project)
* [SSL Certificate Checker (DigiCert)](http://www.digicert.com/help/)
* [SSL Certificate Checker (SSL Shopper)](http://www.sslshopper.com/ssl-checker.html)
* [SSL Client Checker](http://www.howsmyssl.com/)
* [SSL Scanner (command-line tool)](https://github.com/iSECPartners/sslyze)
* [SSL Server Tester](http://www.ssllabs.com/ssltest/)
* [SVG Validator](http://steltenpower.com/svgref.php)
* [Text Decoration Generator](https://yaytext.com/)
* [Traceroute Tool](https://tools.keycdn.com/traceroute)
* [Twitter Card Tester](http://cards-dev.twitter.com/validator)
* [Type Scale Generator (Jeremy Church)](https://typescale.com/)
* [Type Scale Generator (Tim Brown)](https://www.modularscale.com/)
* [UI Test Automator (Ghost Inspector; browser extension)](https://ghostinspector.com/)
* [UI Test Automator (Screenster)](https://screenster.io/)
* [User Agent Detector](https://ua.met.cz/)
* [User Identity Generator](https://www.fakenamegenerator.com/gen-random-us-us.php)
* [Viewport Emulator](http://www.viewportemulator.com/)
* [Viewport Size Determiner](https://www.internetmarketingninjas.com/tools/whats-my-browser-size/)
* [Virus Scanner](http://www.virustotal.com/)
* [Wake-on-LAN Service](http://www.dslreports.com/wakeup)
* [WCAG 2.0 and 2.1 Checker](https://mauve.isti.cnr.it/singleValidation.jsp)
* [WCAG 2.0 Checker (BOIA)](https://www.boia.org/)
* [WCAG 2.0 Checker (Level Access)](https://www.webaccessibility.com/)
* [WCAG 2.0 Checker (TAW)](https://www.tawdis.net/)
* [Web Application Security Analyzer (command-line tool)](https://github.com/spinkham/skipfish)
* [Web Application Security Analyzer (server application)](https://sourceforge.net/projects/owasp/)
* [Web App Test Automator (command-line tool)](https://github.com/svenfuchs/steam)
* [Web Font Generator](https://www.fontsquirrel.com/tools/webfont-generator)
* [Website Analyzer (Accessify)](https://www.accessify.com/)
* [Website Analyzer (Easy Counter)](https://www.easycounter.com/)
* [Website Analyzer (Frontend Dogma)](https://frontenddogma.com/tools/check/)
* [Website Analyzer (Mozilla)](https://observatory.mozilla.org/)
* [Website Analyzer (Nibbler)](https://nibbler.silktide.com/)
* [Website Analyzer (Open Admin Tools)](https://www.openadmintools.com/)
* [Website Analyzer (Site Analyzer)](https://www.site-analyzer.com/)
* [Website Analyzer (StatsCrop)](https://www.statscrop.com/)
* [Website Analyzer (Yellow Lab Tools)](https://yellowlab.tools/)
* [Website Batch Performance Analyzer](https://batchspeed.com/)
* [Website Blockade Checker for China (Comparitech)](https://www.comparitech.com/privacy-security-tools/blockedinchina/)
* [Website Blockade Checker for China (Dotcom-Tools)](https://www.dotcom-tools.com/china-firewall-test)
* [Website Blockade Checker for England](https://www.blocked.org.uk/)
* [Website Blockade Checker for Iran](https://www.comparitech.com/privacy-security-tools/blockediniran/)
* [Website Blockade Checker for Russia](https://isitblockedinrussia.com/)
* [Website Browser and Location Speed Tester](https://www.dotcom-tools.com/website-speed-test)
* [Website Certificate Fingerprint Checker](https://www.grc.com/fingerprints.htm)
* [Website Grader](https://website.grader.com/)
* [Website Monitoring Service](http://www.montastic.com/)
* [Website Performance Analyzer (GTmetrix)](https://gtmetrix.com/)
* [Website Performance Analyzer (KeyCDN)](https://tools.keycdn.com/speed)
* [Website Performance Analyzer (Page Performance; WebKit browser extension)](https://chrome.google.com/webstore/detail/page-performance/gembkfinllgmbkgbgdoaeopbahikjomp)
* [Website Performance Analyzer (PageSpeed)](https://pagespeed.web.dev/)
* [Website Performance Analyzer (Pingdom)](https://tools.pingdom.com/)
* [Website Performance Analyzer (Uptime.com)](https://uptime.com/freetools/website-speed-test)
* [Website Performance Analyzer (Uptrends)](https://www.uptrends.com/tools/website-speed-test)
* [Website Performance Analyzer (Waterfaller)](https://waterfaller.dev/)
* [Website Performance Analyzer (wattspeed)](https://www.wattspeed.com/)
* [Website Performance Analyzer (WebPageTest)](https://www.webpagetest.org/)
* [Website Performance Analyzer (YSlow; browser extension)](http://yslow.org/)
* [Website Privacy Checker](https://webbkoll.dataskydd.net/)
* [Website Review](https://www.valuemyweb.com/reviewmyweb/reviewmyweb)
* [Website Scam Checker](https://www.scamadviser.com/)
* [Website Security Checker (Google)](https://transparencyreport.google.com/safe-browsing/search)
* [Website Security Checker (Norton)](https://safeweb.norton.com/)
* [Website Technology Analyzer (BuiltWith)](https://builtwith.com/)
* [Website Technology Analyzer (My Codeless Website)](https://mycodelesswebsite.com/)
* [WordPress Plugin Detector](http://wppluginchecker.earthpeople.se/)
* [WordPress Theme Detector](https://www.wpthemedetector.com/)
* [XML Formatter](https://www.freeformatter.com/xml-formatter.html)
* [XML Schema Validator](https://schneegans.de/sv/)
* [XML Validator](https://www.xmlvalidation.com/)
* [XML Well-Formedness Checker and Validator](https://www.cogsci.ed.ac.uk/~richard/xml-check.html)
* [XML-RPC Validator](http://scripting.com/code/xmlrpcbrowserclient/)
* [YAML Linter](https://codebeautify.org/yaml-validator)

{pagebreak}

## Summary

This was a brief treatise on the subject of website quality control. What have we learned?

Quality management consists of quality planning, quality assurance, quality control, and quality improvement. It comes with a number of methods to identify (control), fix (improvement), and avoid defects (planning, assurance).

Website quality control includes the means to determine a) whether websites meet our own expectations and b) to what degree our websites meet professional best practices.

Quality control is important because otherwise we would have no way of knowing whether what we do and produce is any good. Quality control is professional; quality control saves time and money and sometimes nerves.

Quality control entails a great number of tests, covering security, accessibility, usability, performance, functionality, maintainability, semantics, validation, layout and design consistency, typography, (general) code quality, and coding standard compliance.

In practice, quality control requires training, depends on our mindsets, profits from automation, and needs enforcement.

And, finally, there are a gazillion tools for quality control and assurance.

Quality management is important, and no website should go without a plan for quality control.
# _The Little Book of Website Quality Control_ (2016)

## Introduction

> There’s always something professional about doing a thing superlatively well.

—Colonel Pickering, in George Bernard Shaw’s _Pygmalion_

What is a good website? For us web professionals, this is a most important question. Building good websites is part of our professional ethics, stemming from a code of honor that asserts that we can be professionals only if our work is good.

But how do we know that our work—that our websites—are good? Many criteria and examinations come to mind, but there is actually an entire field dedicated to informing us: _quality management._

Quality management, which can be broken down into quality planning, quality control, quality assurance, and quality improvement, comes with a host of methods to not just identify (control) and fix (improvement) defects, but to avoid them systematically (planning, assurance).

This little book, which is the third in a series of books that cover important components of modern web development (after web frameworks and coding standards), focuses mostly on the quality control piece, for if we can’t “see” what’s wrong, we won’t fix or plan to avoid what’s wrong. Still, it’s going to share advice on how to tie quality to our processes, for it _is_ more useful to learn how to fish than to hope to be fed every day. The book will do all of this in a loose and relaxed manner, however, and not to the extent ISO standards would cover quality.

Finally, and although this should matter only in few instances, the book hinges more on websites rather than web apps. That [distinction](https://meiert.com/en/blog/docs-and-apps/) is usually relevant when it comes to standards and development best practices, but there are some differences in how one should go about quality checking of sites as opposed to apps. What follows will work slightly better and allow for more complete quality control of web_sites_.

This is a little book, then, because it’s short. Let’s leave the intro behind.

### Acknowledgments

Quality, as this book aims to show, is such an important matter that it would be surprising if I, writing about the very subject, could not name the people to whom I’m indebted. Lars Röwekamp and Jens Schumann, executives of [Open Knowledge GmbH](https://www.openknowledge.de/) in Oldenburg, Germany—where I learned to improve my code—are the first to come to my mind. Yet, as an important goal and a sign of professionalism, the mindset of quality comes close to ideas like “if something’s worth doing, it’s worth doing well,” too.

This little book would not exist were it not for old role models and old sayings, as well as for all the people who have made it reality. For that, I want to thank very much my former colleague, manager, and (still) good friend Kevin Khaw for the Foreword. Finally, I want to recognize the entire O’Reilly team for their swift, competent, and kind help. When this book turns out well, it will have been because of them. Thank you all.

## What Is Quality Control?

Wikipedia defines quality control (often, but rarely in this book, abbreviated as “QC”) as “a process by which entities review the quality of all factors involved in production.” ISO 9000, also through Wikipedia, is said to define quality control as “a part of quality management focused on fulfilling quality requirements.” Google, without offering attribution, understands quality control to be “a system of maintaining standards in manufactured products by testing a sample of the output against the specification.”

We want to use a definition that is stricter on the one end and more lenient on the other: “Website quality control entails the means to determine (a) whether they meet our expectations and (b) to what degree our websites meet professional best practices.”

“Means,” then, will refer largely to infrastructure—that is, tools. Also, as stated a moment ago, we’ll look at some processes and methods useful to improve, not just measure, the quality of our work.

## Why Is Quality Control Important?

Quality control is—for that decisive reason—important, because without it we have no robust way of determining whether what we do and produce is any good.

Quality control, therefore, is a key differentiator between professional and amateur work. Consistent quality is the mark of the professional.

Quality control, finally, saves time and money and sometimes nerves, particularly in the long run.

But what are our options to control the quality of our websites? We’ll look at that now in more detail.

## The Great Website Quality Control Rundown

When _you_ think about the quality of websites, what comes to your mind? How would you test—and what would you test for? Take a moment to ponder this question.

We should readily recall _some_ tools and tests known to us from our everyday work. Some of us might remember validators; some might think of linters; and for others, security suites pop into their minds.

What do we test for? Not only spec compliance as with validation, or code formatting with linters, we can—and should, as professionals—test for everything we can get our hands on. Going through what we can get our hands on and showing what tools we have at our disposal is the purpose of this section. For each area, in descending order of importance, we’ll go over why quality control matters and look at available tools and automation options.

The tools are mostly web-based; applications have been left out, and exceptions noted. The idea was not to shoulder the probably impossible task of listing and evaluating _all_ tools, but to give the interested reader a starting point to evaluate production sites instantly. (Note that despite all diligence exercised in retrieving and evaluating these tools, neither author nor publisher assumes responsibility for the usefulness, reliability, or accuracy of the tools listed.)

### Security

Security can be considered the most important thing to test for because whatever it is we and our users are doing, if the security of it is compromised, we and our users are compromised and can be harmed in a number of ways, from losing data (and privacy) to losing the service itself, and possibly much more. We stand and fall with the security of the services that we offer.

Security is critical, but it’s also tricky in the light of website quality control. For one, websites—rather than apps—might or might not deal with any personal and sensitive information or even ask their users to provide such information. For another, security is not trivial to test and not necessarily to be evaluated all from the outside. This leads us to the situation in which, although security is so crucial, there’s not that much to add outside the context of dedicated information security.

Let’s go over some tools that are available to us (again primarily with a focus on web-based tools). The responsible website owner should—and will—employ additional, notably inner-organizational means to ensure that his services and the data those services gather are secure.

W> These tools were collected in 2016. Some of them are not around anymore. Where possible, links have been corrected, otherwise restored to point to a previous version available on the [Internet Archive](https://archive.org/). You find similar and more tools on the author’s website, [UITest.com](https://uitest.com/), or on Stefan Judis’s website, [Tiny Helpers](https://tiny-helpers.dev/).

* [AES Encrypter](https://www.infoencrypt.com/)
* [Bandwidth Speed Test](https://www.bandwidthplace.com/)
* [Blowfish Hash Generator](https://hash.online-convert.com/blowfish-generator)
* [Cookie Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [CSR Decoder](https://www.sslshopper.com/csr-decoder.html)
* [DNS Analysis](https://web.archive.org/web/20150802080214/https://cloudmonitor.ca.com/en/dnstool.php)
* [DNS Propagation Check](https://www.whatsmydns.net/)
* [Download Time Calculator](http://www.whytehouse.com/opener.html)
* [Email Blacklist Check](https://mxtoolbox.com/blacklists.aspx)
* [FTP Server Test](https://www.dotcom-tools.com/ftp-test)
* [HTTP Header Editor (Request Maker; WebKit browser extension)](https://chrome.google.com/webstore/detail/request-maker/kajfghlhfkcocafkcjlajldicbikpgnp)
* [HTTP Header Editor (Tamper Data; Gecko browser extension)](https://web.archive.org/web/20150604025101/https://addons.mozilla.org/en-US/firefox/addon/tamper-data/)
* [HTTP Header Test](https://www.rexswain.com/httpview.html)
* [HTTP Header Test (Advanced)](https://www.askapache.com/online-tools/http-headers-tool/)
* [IP Address Trace](https://www.ip-tracker.org/)
* [IP Determiner (DSLReports)](https://web.archive.org/web/20150601091833/http://www.dslreports.com/whois)
* [IP Determiner](http://www.ipdatabase.com/)
* [IP Spam Check](https://check.spamhaus.org/)
* [Malware and Security Scanner](https://sitecheck.sucuri.net/)
* [MD5 and SHA Hash Generator](http://onlinemd5.com/)
* [MD5 Encrypter](https://www.md5online.org/md5-encrypt.html)
* [MX Lookup](https://mxtoolbox.com/)
* [Network Intrusion Prevention and Analysis (Kismet; command-line tool)](https://kismetwireless.net/)
* [Network Intrusion Prevention and Analysis (Snort; command-line tool)](https://www.snort.org/)
* [Password Generator (Arantius.com)](https://tools.arantius.com/password)
* [Password Generator (GRC)](https://www.grc.com/passwords.htm)
* [Password Generator (Packetizer)](https://secure.packetizer.com/pwgen/)
* [Password Security Check](https://howsecureismypassword.net/)
* [Password Security Check (GRC)](https://www.grc.com/haystack.htm)
* [PGP Decrypter](https://www.igolder.com/pgp/decryption/)
* [PGP Encrypter](https://www.igolder.com/pgp/encryption/)
* [PGP Key Generator](https://www.igolder.com/pgp/generate-key/)
* [Ping Tool](https://tools.pingdom.com/)
* [Ping Tool (Regional)](https://www.dotcom-tools.com/ping-test)
* [Reverse IP Lookup](https://mxtoolbox.com/ReverseLookup.aspx)
* [Security Breach Victim Check](https://haveibeenpwned.com/)
* [Security Analysis (OWASP Mantra; browser extension)](https://sourceforge.net/projects/getmantra/)
* [SHA-512 Hash Generator](https://hash.online-convert.com/sha512-generator)
* [SPDY Implementation Check](https://spdycheck.org/)
* [SQL Injection and Database Check (command-line tool)](https://sqlmap.org/)
* [SQL Injection Scanner (command-line tool)](https://wiki.owasp.org/index.php/Category:OWASP_SQLiX_Project)
* [SSL Certificate Check (DigiCert)](https://www.digicert.com/help/)
* [SSL Certificate Check (SSL Shopper)](https://www.sslshopper.com/ssl-checker.html)
* [SSL Client Check](https://www.howsmyssl.com/)
* [SSL Scanner (command-line tool)](https://github.com/iSECPartners/sslyze)
* [SSL Server Test](https://www.ssllabs.com/ssltest/)
* [Traceroute Tool](https://web.archive.org/web/20150627073214/https://cloudmonitor.ca.com/en/traceroute.php)
* [Traceroute Tool (Visualized)](https://web.archive.org/web/20140628001934/http://traceroute.monitis.com/)
* [User Identity Generator](https://www.fakenamegenerator.com/gen-random-us-us.php)
* [Virus Scanner](https://www.virustotal.com/gui/home/upload)
* [Wake-on-LAN Service](https://www.dslreports.com/wakeup)
* [Web Application Security Analysis (Canoo; command-line tool)](https://web.archive.org/web/20150330153931/http://webtest.canoo.com/webtest/manual/WebTestHome.html)
* [Web Application Security Analysis (OWASP; server application)](https://sourceforge.net/projects/owasp/)
* [Web Application Security Analysis (Skipfish; command-line tool)](https://github.com/spinkham/skipfish)
* [Website Blockade Check for China](https://www.comparitech.com/privacy-security-tools/blockedinchina/)
* [Website Blockade Check for England](https://www.blocked.org.uk/)
* [Website Fingerprint Check](https://www.grc.com/fingerprints.htm)
* [Website Monitoring Service](https://www.montastic.com/)

### Accessibility

[Per Wikipedia](https://en.wikipedia.org/wiki/Accessibility), accessibility “refers to the design of products, devices, services, or environments for people with disabilities”; “the concept of accessible design ensures both ‘direct access’ (i.e., unassisted) and ‘indirect access,’ meaning compatibility with a person’s assistive technology (for example, computer screen readers).” Accessibility is one of the most important ideas to understand, for the Web is all about accessibility—accessibility is, in fact, the Web’s biggest promise. Accessibility has often been linked to making data available to machines—like search engine bots—but it is, first and foremost, about making information available to _people_.

Legislation exists in many countries—like [Section 508](https://www.section508.gov/) in the United States, [BITV](https://www.gesetze-im-internet.de/bitv_2_0/) in Germany, or [RGAA](https://web.archive.org/web/20151122054135/http://references.modernisation.gouv.fr/rgaa-3-0) in France—that supports and presses for worldwide accessibility. The key standards, the [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/TR/WCAG20/), published by the World Wide Web Consortium (W3C) have gone through two versions and are, though not perfect, robust. There are a good number of tools, as we shall see. And still, accessibility remains one of the industry’s stepchildren.

Independent of whether we would be held accountable legally, accessibility is one of the most important things that we should cater to on our sites.

* [Accessibility Analysis (Gecko browser extension)](https://web.archive.org/web/20150604084239/https://addons.mozilla.org/en-US/firefox/addon/juicy-studio-accessibility-too/)
* [Accessibility Check (AATT; Automated; command-line tool)](https://github.com/paypal/AATT)
* [Accessibility Check (FAE)](https://fae.disability.illinois.edu/)
* [Accessibility Check (WAEX)](https://web.archive.org/web/20150709134717/http://www.it.uc3m.es/vlc/waex.html)
* [Accessibility Check (WAVE 3.0)](https://wave.webaim.org/)
* [Accessibility Developer Tools (WebKit browser extension)](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
* [Accessibility, HTML, and Link Check (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Accessibility Linter](https://accesslint.com/)
* [Accessibility Visualization (script)](https://github.com/Khan/tota11y)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [Colorblind Web Page Filter](https://www.toptal.com/designers/colorfilter)
* [Color Contrast Analysis (Jonathan Snook)](https://snook.ca/technical/colour_contrast/colour.html)
* [Color Contrast Analysis (WCAG Contrast Checker; Gecko browser extension)](https://addons.mozilla.org/en-US/firefox/addon/wcag-contrast-checker/)
* [Color Contrast Analysis (WebAIM)](https://webaim.org/resources/contrastchecker/)
* [Color Deficit Emulation](http://vischeck.com/vischeck/vischeckURL.php)
* [Color Selector](https://web.archive.org/web/20200328084352/https://gmazzocato.altervista.org/en/colorwheel/wheel.php)
* [CSS Accessibility Analysis](https://web.archive.org/web/20150419215647/https://juicystudio.com/services/csstest.php)
* [Design Responsiveness Test](http://www.responsivepx.com/)
* [Mobile-Friendliness Check](https://search.google.com/test/mobile-friendly)
* [Section 508 Check](https://web.archive.org/web/20150706014945/http://www.508checker.com/)
* [Section 508 and WCAG 1.0 Check (Site Valet)](https://web.archive.org/web/20150707231218/http://valet.webthing.com/access/url.html)
* [Section 508 and WCAG 2.0 Check (Cynthia Says)](http://www.cynthiasays.com/)
* [Section 508, WCAG 2.0, and BITV 1.0 Check](https://web.archive.org/web/20150809114127/https://achecker.ca/checker/)
* [WCAG 1.0 Check (SIDAR)](https://web.archive.org/web/20150726041535/http://www.sidar.org/hera/)
* [WCAG 1.0 Check (TAW)](https://www.tawdis.net/)
* [WCAG 2.0 Check (BOIA)](https://www.boia.org/)
* [WCAG 2.0 Check ([Level Access])](https://www.webaccessibility.com/)

### Usability

Usability is one of the most critical areas to focus on when running a website, hence it deserves special mention here. Because it is not a technical concern, however, it’s only mentioned in passing. If you are interested in this and not already familiar with designing and keeping a usable website, you might want to check out some key resources for further information, like [Usability.gov](https://www.usability.gov/), [Nielsen Norman Group](https://www.nngroup.com/articles/), or [UXmatters](https://www.uxmatters.com/).

### Performance

For the longest time, Google has worked following the mantras, [“every millisecond counts”](https://www.youtube.com/watch?v=aXJklICrFJI) and, though weaker, [“fast is better than slow.”](https://web.archive.org/web/20150823063537/https://www.google.com/about/company/philosophy/) And for good reason! Speed is a key factor for a positive user experience—so crucial, in fact, that it’s one of the determinants for customer satisfaction and conversion.

There are many studies that back performance up as important for quality websites, and Six Revisions (with [_Why Website Speed is Important_](https://www.webfx.com/blog/web-design/why-website-speed-is-important/)), Impressive Webs (with [_The Importance of Page Speed_](https://www.impressivewebs.com/importance-of-page-speed-sources/)), and WebSiteOptimization.com (with [_Empirical Study of Web Site Speed on Search Engine Rankings_](http://www.websiteoptimization.com/speed/tweak/website-speed-search-rankings-study/)) provide pointers for a good number of them.

Today, test tools abound for performance measuring. Here are some of them:

* [Availability Check (CurrentlyDown.com)](http://currentlydown.com/)
* [Availability Check (Is It Down Right Now)](https://www.isitdownrightnow.com/)
* [Availability Check (Regional; InternetSupervision.com)](http://internetsupervision.com/scripts/urlcheck/check.aspx)
* [Availability Check (Regional; Site24x7)](https://www.site24x7.com/check-website-availability.html)
* [CSS Analysis](https://cssstats.com/)
* [Load Time and Object Check](http://www.websiteoptimization.com/services/analyze/)
* [Load Time Check](http://www.1-hit.com/all-in-one/tool.loading-time-checker.htm)
* [Performance and Scalability Test (Pylot; command-line tool)](https://web.archive.org/web/20150619155406/http://www.pylot.org/)
* [Performance and Scalability Test (Tsung; command-line tool)](http://tsung.erlang-projects.org/)
* [Website Browser and Location Speed Test](https://www.dotcom-tools.com/website-speed-test)
* [Website Performance Analysis (GTmetrix)](https://gtmetrix.com/)
* [Website Performance Analysis (IISpeed)](https://web.archive.org/web/20150331063207/https://www.iispeed.com/pagespeed/insights)
* [Website Performance Analysis (Page Performance; WebKit browser extension)](https://chrome.google.com/webstore/detail/page-performance/gembkfinllgmbkgbgdoaeopbahikjomp)
* [Website Performance Analysis (PageSpeed)](https://developers.google.com/speed/pagespeed/insights/)
* [Website Performance Analysis (Pingdom)](https://tools.pingdom.com/)
* [Website Performance Analysis (WebPageTest)](https://www.webpagetest.org/)
* [Website Performance Analysis (YSlow; browser extension)](http://yslow.org/)
* [Website Timer](https://web.archive.org/web/20150602145726/http://www.octagate.com/service/SiteTimer/)

### Functionality

Another user-centered matter concerns site functionality and workflows: can we get from _A_ to _B_? Fortunately, even though this is important to ensure, it’s easy to verify—so easy in fact, that most of the time functionality testing is “implied.”

How so? What have we just said? Essentially, that we’d know whether when building and extending our sites and their functionality, we can’t get to what we just built and extended. Whether we’d add a new registration page or post a new press release, we typically notice as part of the testing and launch process whether it actually made it live and can be found.

Thus, it’s advantageous to tell by other means whether everything’s where we expect it to be, and whether it works as we expect it to work. Here are some tools to do that:

* [Accessibility, HTML, and Link Check (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Browser Test Automation (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automation (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automation (Squish)](http://www.froglogic.com/)
* [Browser Test Automation (Watir; browser extension)](https://web.archive.org/web/20150627162429/http://watirwebdriver.com/)
* [“Cognitive Walkthrough for the Web” Tools](https://web.archive.org/web/20150924073807/http://autocww.colorado.edu/HomePage.html)
* [Image and Link Analysis](https://web.archive.org/web/20150816054027/http://tools.seochat.com/tools/broken-links-images-tool/)
* [Link Analysis](http://juicystudio.com/services/linktest.php)
* [Link Check (LinkTiger)](http://www.linktiger.com/)
* [Link Check (Site Valet)](https://web.archive.org/web/20130714065334/http://valet.webthing.com/link/)
* [Link Check (W3C)](https://validator.w3.org/checklink)
* [Responsiveness Test](https://web.archive.org/web/20210506140954/https://www.viewlike.us/)
* [UI Test Automation (Ghost Inspector; browser extension)](https://ghostinspector.com/)
* [UI Test Automation (Screenster)](https://screenster.io/)
* [Universal Validator](http://watson.addy.com/)
* [Web App Test Automation (command-line tool)](https://github.com/svenfuchs/steam)

### Maintainability

The first, rather technical item to watch out and test for is maintainability. Maintainability? Yes, the degree of our ability to efficiently make changes to our design and code. This degree, this efficiency, makes for one of the most crucial aspects of web development—and at the same time it’s regularly among the most neglected ones.

What is maintainability, what does this ability and efficiency really refer to? That is a valid question in light of the fact that many long years of neglect have yielded little documentation and few best practices pertaining to maintainability and maintenance. [“One cannot not maintain”](https://meiert.com/en/blog/law-of-maintainability/)—that is the “law” I’ve coined in despair. One cannot not maintain originates in the fact that anything we produce must at some point be dealt with again, whether by us or by others.

(As for tools, only sadness seems to be available as of yet.)

* [QA Style Sheet (bookmarklet)](https://github.com/j9t/qa-style-sheet)

### Semantics

Semantics was one of the hot topics of the last decade, when the field of web development went through its first stage of maturation and developed a better sense for how HTML markup should be written. This awareness was motivated in part by a higher and closer regard for web standards—mostly in relation to the underlying specifications—and in part by stronger emphasis on the need for websites to be more accessible.

Today, the hype has long moved on to web apps, and tolerance has stretched a bit again to “anything goes.” [WAI-ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) has grown and matured as both tool and excuse. [Microdata](https://html.spec.whatwg.org/multipage/microdata.html) and [web components](https://www.webcomponents.org/) have, so far, also done their share to allow a mindset of “semantics is not important anymore” to flourish.

Is this all justified? No. But the situation is complex. To make a bit more sense of it, we should break things apart.

For semantics, we should look at where it’s coming from and what people mean when they talk about it. [Semantics in HTML](https://meiert.com/en/blog/on-semantics-in-html/) refers to authority—and consensus-based meaning. The W3C or the WHATWG—the authorities—define in specifications what each element and attribute means. Vendors and the web development community buy into these definitions. Sometimes, as for consensus, they disagree (voiced in standard controversies) or they add their own solutions (as with [microformats](http://microformats.org/)). ID and class names represent the most minimal form of consensus on meaning, sometimes just brought forth by a single developer.

For new technology and techniques, we find ourselves in a conflict. The standards community has given in to a form of arms race against itself. After years of slow progress, low output, and seeming indifference to the user and vendor community, suddenly those involved in standards want to micromanage _everything_. This has led the specifications to grow in number and size, and we’ve still not been able to take inventory of everything we’re now capable of doing. With that growing complexity, we risk losing it all, or [so I feel](https://meiert.com/en/blog/fing-up-standards/). But with respect to semantics, we’re right at the seam, and things have become loose there. No one focuses any longer on the _meaning_ of what documents and templates describe anymore.

Semantics will make it back to our agendas for the following reason: we can only get the most out of code and information within code, ensure best access to that code, and work best together on code if the code has meaning, or is used according to the meaning it had been assigned.

There are a number of semantics checks and generators for enriched markup available:

* [hCalendar Generator](http://microformats.org/code/hcalendar/creator)
* [hCard Generator](http://microformats.org/code/hcard/creator)
* [HTML Outline Extractor](https://gsnedders.html5.org/outliner/)
* [Microformat Extractor and Transformer](https://web.archive.org/web/20150627202810/http://microform.at/)
* [Open Graph and Semantics Extractor](https://developers.facebook.com/tools/debug)
* [Schema Generator](https://seoscout.com/tools/schema-generator)
* [Semantics Check (Gecko browser extension)](https://web.archive.org/web/20150426142109/https://addons.mozilla.org/en-US/firefox/addon/semantic-checker/)
* [Semantics Extractor](https://www.w3.org/2003/12/semantic-extractor.html)
* [Semantics Parser and Extractor](http://buzzword.org.uk/swignition/try)
* [Structured Data Test (Google)](https://developers.google.com/search/docs/advanced/structured-data)
* [Structured Data Test (Yandex)](https://web.archive.org/web/20150319181926/https://webmaster.yandex.com/microtest.xml)
* [Twitter Card Test](https://cards-dev.twitter.com/validator)

(Some accessibility and validation tools cover aspects of semantics, too; to avoid repetition and not distort the view on the “purely semantic” testing options, these have not been duplicated here.)

### Validation

Validation as a measurable priority had peaked, too, before falling from grace. But popularity does not correlate with validity (hah!), accuracy, or quality, and one can argue well how validation is a relevant factor for website quality. It is such an important factor for that reason that only validation ensures we’ve been coding according to the different specs—a condition that corresponds with professionalism, or at least professional ethics.

Although this is almost all there is to say about validation, the web development landscape begs to differ, most notably when it comes to HTML and CSS. HTML is more stable and used in more places than CSS. CSS is under heavier development and occasionally experimental, yet style sheets live in relatively few places (CSS being “orthogonal” to HTML makes for its relevance in maintainability). That means that validation for HTML is far more important than for CSS. Because HTML is stable, it is easier to validate, and because it’s so prevalent—all over the place in templates and documents—it’s also much more critical to validate.

We are in the envious situation of having a great many, good-quality validators at our disposal:

* [Accessibility, HTML, and Link Check (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [CSS Validator (W3C)](https://jigsaw.w3.org/css-validator/)
* [CSS Validator (WDG)](https://www.htmlhelp.com/tools/csscheck/)
* [DAML Validator](http://www.daml.org/validator/)
* [hCard Validator](http://hcard.geekhood.net/)
* [.htaccess Validator](https://shop.alterlinks.com/htaccess-validator/htaccess-validator.php)
* [HTML Validator (W3C)](https://validator.w3.org/)
* [HTML Validator (WDG)](https://web.archive.org/web/20150721050450/http://www.htmlhelp.com/tools/validator/)
* [HTML 5 Validator](https://html5.validator.nu/)
* [HTML, CSS, and Conformance Validator](https://validator.w3.org/unicorn/)
* [Internationalization Check](https://validator.w3.org/i18n-checker/)
* [JSON Validator](https://jsoncompare.com/)
* [Markup Validator](https://web.archive.org/web/20151006113546/http://www.validome.org/)
* [P3P Validator](https://www.w3.org/P3P/validator.html)
* [Rich Pin Validator](https://web.archive.org/web/20150615230955/https://developers.pinterest.com/rich_pins/validator/)
* [RDF Validator](https://www.w3.org/RDF/Validator/)
* [robots.txt Syntax Check](https://web.archive.org/web/20151126053219/http://tool.motoricerca.info/robots-checker.phtml)
* [RSS and Atom Feed Validator](https://validator.w3.org/feed/)
* [SADiC Validator](https://web.archive.org/web/20160322204459/https://www.the-web-middle-earth.com/sadic/sadicOnlineValidator.html)
* [SBML Validator](http://sbml.org/Facilities/Validator/)
* [Sitemap Validator](https://web.archive.org/web/20160715025623/http://www.validome.org/google/validate)
* [SQL Validator](https://web.archive.org/web/20160821011626/http://developer.mimer.se/validator/index.htm)
* [SVG Validator](https://web.archive.org/web/20050306190554/http://jiggles.w3.org/svgvalidator/ValidatorURI.html)
* [Universal Validator](http://watson.addy.com/)
* [XHTML 1.0 Schema Validator](https://schneegans.de/sv/)
* [XML Schema Validator](https://web.archive.org/web/20130728234212/http://www.w3.org/2001/03/webdata/xsv)
* [XML Validator](https://www.xmlvalidation.com/)
* [XML Well-Formedness Check and Validator](https://www.cogsci.ed.ac.uk/~richard/xml-check.html)

### Layout and Design Consistency

Normally filed under other categories, consistency-checking is also a key factor in website quality control. What is it normally filed under? Browser-testing. That is, as we’ve just noticed, a misnomer: we’re not testing browsers, we’re testing the layout and design of our websites for consistency across browsers and devices.

Making this little differentiation makes clear what tools we can use: browser and device emulators, of which there are plenty. The testing landscape has changed significantly over the years, and although it’s become a big issue to test for the slew of devices, web-based tools that allow quick comparisons have matured to the extent that we have to install fewer user agents than we used to. (The normalization and unification of rendering engines has contributed to improvements, too, considering that [WebKit](https://www.webkit.org/) is now by far the most common engine.)

To test layout and design, we can use tools and services like the following:

* [Android Emulators](https://web.archive.org/web/20160624025405/http://www.manymo.com/emulators)
* [Browser Screenshots (Windows, Mac OS, Android, iOS)](https://www.browserstack.com/screenshots)
* [Browser Screenshots (Windows, Mac OS, Linux)](http://browsershots.org/)
* [Browser Test Automation (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automation (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automation (Squish)](http://www.froglogic.com/)
* [Browser Test Automation (Watir; browser extension)](https://web.archive.org/web/20150627162429/http://watirwebdriver.com/)
* [Design Diff (script)](https://percy.io/)
* [Edge Compatibility Test](http://doesitworkonedge.com/)
* [Internet Explorer Viewer (IE NetRenderer)](http://netrenderer.com/)
* [Internet Explorer Viewer (URL2PNG)](https://www.url2png.com/)
* [iPhone Emulator](https://web.archive.org/web/20160822221822/http://iphone4simulator.com/)
* [Layout Bug Test (script)](https://code.google.com/archive/p/fighting-layout-bugs/)
* [Lynx Viewer](http://www.delorie.com/web/lynxview.html)
* [Mobile Emulator](http://mtld.mobi/emulator.php)
* [Opera Mini Emulator](http://opr.as/2cKpahy)
* [User Agent Detector](http://ua.met.cz/)
* [Viewport Size Determiner](https://www.internetmarketingninjas.com/seo-tools/whats-my-browser-size/)
* [Website Design History (DomainTools)](https://web.archive.org/web/20160121044614/https://research.domaintools.com/research/screenshot-history/)
* [Website Design History (Screenshots.com)](https://web.archive.org/web/20160706230510/http://www.screenshots.com/)

### Typography

Typography is not what the common website owner will connect to website quality—and, sadly, neither might every designer—but it is, of course, an important aspect of every website. Typography is all the more important, as the amount of content a website actually has increases—we remind ourselves of Robert Bringhurst, who taught us that “typography exists to honor content.”

But why test? Obviously, for the reasons that typography matters—and so we’re not just running into William Bruce Cameron’s (and apparently not Albert Einstein’s) famous statement, “Not everything that counts can be counted, and not everything that can be counted counts.” Typography can be counted—the surprise of this section, perhaps—and typography does count. Not many tools are available to test for good typography, but still there are some that make our typographic jobs easier:

* [Font Combinator](https://web.archive.org/web/20160708165032/http://font-combinator.com/)
* [Font Comparison](https://www.typetester.org/)
* [Font Determiner (WhatFont; WebKit browser extension)](http://www.chengyinliu.com/whatfont.html)
* [Font Determiner (WhatTheFont)](https://www.myfonts.com/WhatTheFont/)
* [Font Fallback Determiner (bookmarklet)](http://www.hotelscrete.net/ffffallbackcom/)
* [Golden Ratio Typography Calculator](https://grtcalculator.com/)
* [Type Diff](https://tiff.herokuapp.com/)
* [Type Live Test](https://web.archive.org/web/20160617205754/http://typewonder.com/)
* [Type Scale](https://type-scale.com/)
* [Type Scale (Modular)](https://www.modularscale.com/)
* [Web Font Generator](https://www.fontsquirrel.com/tools/webfont-generator)

### Code Quality

Venturing again into the realm that’s invisible to the users of our sites, code quality has many attributes, some of which we’ve already addressed. Here, code quality will touch on general overall checks, as well as on _linting_—that is, analyzing code for potential programmatic and stylistic errors (which we’ll focus on separately in the next section).

Linting comes out of computer programming, something we don’t file web development under, but linters are by now available for pretty much anything, including CSS. Some general quality-related tools include the following:

* [Accessibility Linter](https://accesslint.com/)
* [CMS Detector](https://web.archive.org/web/20160714054200/http://guess.scritch.org/)
* [CSS Linter](http://csslint.net/)
* [Google Webmaster Guidelines Check](https://web.archive.org/web/20160823020128/http://varvy.com/)
* [HTML Compatibility Check for XHTML](https://web.archive.org/web/20101120133016/http://qa-dev.w3.org/appc/)
* [JavaScript Linter (JSHint)](https://jshint.com/)
* [JavaScript Linter (JSLint)](https://www.jslint.com/)
* [Reputation and Safety Check](https://www.mywot.com/)
* [Trustworthiness Check](https://www.scamadviser.com/)
* [Website Analysis (Alexa)](https://www.alexa.com/)
* [Website Analysis (Nibbler)](https://nibbler.silktide.com/)
* [Website Analysis (RankFlex)](https://web.archive.org/web/20160617035405/http://www.rankflex.com/en/)
* [Website Analysis (Site Analyzer)](https://www.site-analyzer.com/)
* [Website Analysis (StatsCrop)](https://www.statscrop.com/)
* [Website Analysis (UITest.com)](https://uitest.com/check/)
* [Website Grader](https://website.grader.com/)
* [Website Review](https://www.valuemyweb.com/reviewmyweb/reviewmyweb)
* [Website Technology Analysis](https://builtwith.com/)

### Coding Standard Compliance

Last but not least and not to be missed: we want to and can measure the conformity and consistency of our code. For that—and you might remember _The Little Book of HTML/CSS Coding Guidelines_ (or want to check it out)—we look at common coding practices, and, notably, our coding guidelines.

The listed quality checks, now, simply look at compliance, comparing code strings against a predefined catalog of rules. Only lowercase element names in HTML? Only single quotes in CSS? No global variables in JavaScript, if the more experienced scripter fancies? No BOM in text files? This is done by website quality checks against code standards, such as the following:

* [Code Formatter (Code Beautifier)](https://ctrlq.org/beautifier/)
* [Code Formatter (Pretty Printer)](http://prettyprinter.de/)
* [CSS Formatter (CSS Portal)](https://www.cssportal.com/format-css/index.php)
* [CSS Formatter (Lonnie Best)](http://www.lonniebest.com/FormatCSS/)
* [CSS Optimizer and Formatter (CSS Beautifier)](https://www.cleancss.com/css-beautify/)
* [CSS Optimizer and Formatter (CSScomb)](https://web.archive.org/web/20160719231432/http://csscomb.com/online/)
* [HTML Formatter](https://www.freeformatter.com/html-formatter.html)
* [HTML, CSS, and JS Formatter](https://www.10bestdesign.com/dirtymarkup/)
* [JSON Formatter](https://jsonformatter.curiousconcept.com/)

After we have properly formatted our code and made it consistent, however, we might still want to make it production-ready by compressing and minifying it. Our work files should be easy (to understand) for us and our production files should be easy (to parse and transfer) for others. For this there are additional tools.

* [CSS Compressor](https://hell.meiert.org/aux/compress/css/gui/)
* [HTML Compressor](http://htmlcompressor.com/compressor/)
* [HTML Compressor (html-minifier)](https://npm.runkit.com/html-minifier)
* [JavaScript Compressor](http://dean.edwards.name/packer/)

## Quality Control in Practice

With the overview and tools we’ve now gathered, what does quality control of websites look like in practice? Is this all we need? What pitfalls are there? What do we need to watch out for? There are indeed a few things to consider.

### Training

Training is a first, very important step toward successfully implementing quality control practices. Training should be understood very generally here, for any professional training that teaches people how to produce better work will at the same time help quality. In that sense, training will not be elaborated on here.

However, training can also be offered and attended specifically to establish a quality mindset, to improve the associated skills, and to promote tools that measure and improve quality. (As such, training will also be linked to the following points, but not be called out again.)

### Mindset

The most important factor when it comes to practical quality is the mindset. The greatest quality initiative is not worth much if it’s not clear to the team and enterprise why quality matters, and how quality is beneficial for them. The key to a conducive mindset is communication; a potential trap is rewards.

#### Communication

Communication is the primary way to spread and instill a mindset of quality, with quality as the goal and guiding principle.

This communication should sporadically repeat, but doesn’t need to consist of overt reminders on why quality matters and how it benefits everybody. If we want to repeat the essence of both answers here, then: quality is important to deliver work that is good by professional standards and benefits everyone, because products of quality are easier and more pleasant to consume and work with.

Communication is, for that reason, important because we all benefit from being reminded of our priorities.

Based on this, communication can now range from bylines in regular company and team communications, thanking everyone for the vigilance to produce good work, to dedicated emails emphasizing the goal and importance of quality.

#### Rewards

Rewards, then, are _no_ key for a quality mindset. We should avoid rewards. Rewards might compel people to participate in quality-related events, but they don’t necessarily compel people to embrace quality (in fact, they rarely do). They seem to distract from, rather than point to the message.

I’ve had some such experiences with international teams, whereby rewards did help draw attention to quality-related initiatives, but they didn’t lead to a better understanding of, or a higher motivation, for more quality. What was more effective was communication, notably through managers. Hierarchy and authority can, of course, be great facilitators in our quest to improve the quality of our work.

### Automation

Insist on automation. Insist—on automation. _Of course_, we’re inclined to say—once we’ve automated all quality-relevant tasks and processes, what’s there to be missed, how could we get anything wrong? But we haven’t progressed quite yet to the point that we’re able to automate everything. Our reality is that not enough is being automated, and sensitizing for that is what this very practical recommendation aims at. We must automate as much as we can; we must insist on automation.

We have discussed many tools so far and are going to summarize them again (it follows a section listing all our tools)—some of those are very easy to implement and automate, but for others, per our now-defined goal to automate and _insist_ to automate, will require a bit of an effort. A discussion on how to write and run automation scripts on different platforms is beyond the scope of this little book, but if you’d like to see what that can look like, read complementary books like [_Learning Linux Shell Scripting_](https://www.amazon.com/dp/B013WWYVHK/?tag=j9t-21-20), [_Network Programmability and Automation_](https://www.amazon.com/dp/1491931256/?tag=j9t-21-20), or [_Learn AppleScript_](https://www.amazon.com/dp/1430223618/?tag=j9t-21-20).

### Enforcement

In the context of coding guidelines, we’ve learned to differentiate between descriptive or positive guidelines and those that are prescriptive or normative (see _The Little Book of HTML/CSS Coding Guidelines_). The difference is mostly practical—when code quality is at a high level, we merely document (describe) what everyone’s already doing; when code quality is low, we tell everyone what to do (prescribe). However, as it pertains to much of what we’ve discussed so far, this requires some way of enforcement.

How do we enforce quality? This is still a difficult question; so difficult, in fact, that in practice we often see it dodged. Why? Because enforcement easily upsets people, and we don’t want to upset people, not even—or especially—when they report to us. But we’re on the right track here.

Enforcement happens top-down. Executives and managers are to be looked at to emphasize and _live_ quality, to reward good quality, and to—in one way or another—discourage poor quality. How? By doing what we surprisingly forget frequently: measuring quality and tying related metrics to performance evaluations.

Two anecdotes illustrate that approach. There’s one tale of a manager who has, despite efforts of his team to up the ante and increase quality in his department, never endorsed, let alone supported or encouraged those team members’ efforts in team communications or goals. That quality initiative’s efforts, witnessed at one point at a major corporation, suffered a significant blowback.

At the same firm at another time, managers called out the importance of quality and used available data points, like performance scores as measured by [Google’s PageSpeed tools](https://developers.google.com/speed), accessibility problems as measured by [Sidar’s HERA](https://web.archive.org/web/20150726041535/http://www.sidar.org/hera/), or the number of validation errors as measured by [W3C’s Link Checker](https://validator.w3.org/checklink). Although the team in question never got to tie metrics like these to performance evaluations, that precise step was on the table as to have strong encouragement and—ultimately enforce—higher quality.

### Logistics

In broad terms, our efforts around quality require logistics. These might consist of the following, listed briefly for inspiration:

Standards and guidelines documentation
: No quality effort can succeed without standards and guidelines. These can be external, but wherever they can be found, they must still be documented.

Meta documentation
: What our quality efforts entail and require must also be documented. That…

Internal websites or wikis
: …is best done on some internal website or wiki. Here, we should gather everything we want, know, do, and plan.

Dedicated contacts
: Quality stands and falls with people. At least one among them should serve as a primary contact, and that person must not just be responsible and accountable (and laudable), but also discoverable and available.

Mailing lists
: To coordinate quality efforts, communicate new and updated documentation, and so on, mailing lists are a crucial tool. There might be lists for quality-related teams to lists for the entire enterprise.

Events
: Google has a practice to host “fix-its” or “fixlets,” events that let the company or departments clean up and improve their work and code base, but quality events can really range from a toast on quality at the daily scrum meeting to external conferences (with company representation) talking about quality.

The more a quality initiative grows and matures, the more tools and methods it might employ, and yet what we describe here is about showing some of the basic items that we can turn to.

## Tools

The following serves as an index of a range of web-based tools, browser extensions, command-line tools, scripts, and bookmarklets. It is not complete; it might lack some important tools; but many tools come with my endorsement, and the promise to also serve others well.

(By the way, my [UITest.com](https://uitest.com/) site is a hub for web-based testing tools, generators, and anything else web-based that’s useful for web developers and designers. You can find many of the tools listed in this book and more there.)

W> These tools were collected in 2016. Some of them are not around anymore. Where possible, links have been corrected, otherwise restored to point to a previous version available on the [Internet Archive](https://archive.org/). You find similar and more tools on the author’s website, [UITest.com](https://uitest.com/), or on Stefan Judis’s website, [Tiny Helpers](https://tiny-helpers.dev/).

* [Accessibility Analysis (Gecko browser extension)](https://web.archive.org/web/20150604084239/https://addons.mozilla.org/en-US/firefox/addon/juicy-studio-accessibility-too/)
* [Accessibility Check (AATT; Automated; command-line tool)](http://github.com/paypal/AATT)
* [Accessibility Check (FAE)](http://fae20.cita.illinois.edu/)
* [Accessibility Check (WAEX)](https://web.archive.org/web/20150709134717/http://www.it.uc3m.es/vlc/waex.html)
* [Accessibility Check (WAVE 3.0)](https://wave.webaim.org/)
* [Accessibility Developer Tools (WebKit browser extension)](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb)
* [Accessibility, HTML, and Link Check (WebKit and Gecko browser extension)](http://www.totalvalidator.com/)
* [Accessibility Linter](https://accesslint.com/)
* [Accessibility Visualization (script)](http://github.com/Khan/tota11y)
* [AES Encrypter](http://www.infoencrypt.com/)
* [Android Emulators](https://web.archive.org/web/20160624025405/http://www.manymo.com/emulators)
* [ARIA Validator (WebKit browser extension)](https://chrome.google.com/webstore/detail/aria-validator/oigghlanfjgnkcndchmnlnmaojahnjoc)
* [Availability Check (CurrentlyDown.com)](http://www.currentlydown.com/)
* [Availability Check (Is It Down Right Now)](http://www.isitdownrightnow.com/)
* [Availability Check (Regional; InternetSupervision.com)](http://internetsupervision.com/scripts/urlcheck/check.aspx)
* [Availability Check (Regional; Site24x7)](https://www.site24x7.com/check-website-availability.html)
* [Bandwidth Speed Test](http://www.bandwidthplace.com/)
* [Blowfish Hash Generator](http://hash.online-convert.com/blowfish-generator)
* [Browser Screenshots (Windows, Mac OS, Android, iOS)](https://www.browserstack.com/screenshots)
* [Browser Screenshots (Windows, Mac OS, Linux)](http://browsershots.org/)
* [Browser Test Automation (Sahi; browser extension)](https://resources.sahipro.com/alldocs/v9.5.0/introduction/)
* [Browser Test Automation (Selenium; browser extension)](https://www.selenium.dev/projects/)
* [Browser Test Automation (Squish)](http://www.froglogic.com/)
* [Browser Test Automation (Watir; browser extension)](https://web.archive.org/web/20150627162429/http://watirwebdriver.com/)
* [CMS Detector](https://web.archive.org/web/20160714054200/http://guess.scritch.org/)
* [Code Formatter (Code Beautifier)](https://ctrlq.org/beautifier/)
* [Code Formatter (Pretty Printer)](http://prettyprinter.de/)
* [“Cognitive Walkthrough for the Web” Tools](https://web.archive.org/web/20150924073807/http://autocww.colorado.edu/HomePage.html)
* [Colorblind Web Page Filter](http://colorfilter.wickline.org/)
* [Color Contrast Analysis (Jonathan Snook)](https://snook.ca/technical/colour_contrast/colour.html)
* [Color Contrast Analysis (WCAG Contrast Checker; Gecko browser extension)](http://mzl.la/2cmVY1A)
* [Color Contrast Analysis (WebAIM)](http://webaim.org/resources/contrastchecker/)
* [Color Deficit Emulation](http://www.vischeck.com/vischeck/vischeckURL.php)
* [Color Selector](https://web.archive.org/web/20200328084352/https://gmazzocato.altervista.org/en/colorwheel/wheel.php)
* [Cookie Editor (WebKit browser extension)](https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg)
* [CSR Decoder](http://www.sslshopper.com/csr-decoder.html)
* [CSS Accessibility Analysis](https://web.archive.org/web/20150419215647/https://juicystudio.com/services/csstest.php)
* [CSS Analysis](http://cssstats.com/)
* [CSS Compressor](https://hell.meiert.org/aux/compress/css/gui/)
* [CSS Formatter (CSS Portal)](https://www.cssportal.com/format-css/index.php)
* [CSS Formatter (Lonnie Best)](http://www.lonniebest.com/FormatCSS/)
* [CSS Linter](http://csslint.net/)
* [CSS Optimizer and Formatter (CSS Beautifier)](https://www.cleancss.com/css-beautify/)
* [CSS Optimizer and Formatter (CSScomb)](https://web.archive.org/web/20160719231432/http://csscomb.com/online/)
* [CSS Validator (W3C)](https://jigsaw.w3.org/css-validator/)
* [CSS Validator (WDG)](https://www.htmlhelp.com/tools/csscheck/)
* [DAML Validator](http://www.daml.org/validator/)
* [Design Responsiveness Test](http://responsivepx.com/)
* [DNS Analysis](https://web.archive.org/web/20150802080214/https://cloudmonitor.ca.com/en/dnstool.php)
* [DNS Propagation Check](http://www.whatsmydns.net/)
* [Download Time Calculator](http://www.whytehouse.com/opener.html)
* [Edge Compatibility Test](http://doesitworkonedge.com/)
* [Email Blacklist Check](http://mxtoolbox.com/blacklists.aspx)
* [Font Combinator](https://web.archive.org/web/20160708165032/http://font-combinator.com/)
* [Font Comparison](https://www.typetester.org/)
* [Font Determiner (WhatFont; WebKit browser extension)](http://www.chengyinliu.com/whatfont.html)
* [Font Determiner (WhatTheFont)](https://www.myfonts.com/WhatTheFont/)
* [Font Fallback Determiner (bookmarklet)](http://www.hotelscrete.net/ffffallbackcom/)
* [FTP Server Test](http://www.dotcom-tools.com/ftp-server-test.aspx)
* [Golden Ratio Typography Calculator](https://grtcalculator.com/)
* [Google Webmaster Guidelines Check](https://web.archive.org/web/20160823020128/http://varvy.com/)
* [hCalendar Generator](http://microformats.org/code/hcalendar/creator)
* [hCard Generator](http://microformats.org/code/hcard/creator)
* [hCard Validator](http://hcard.geekhood.net/)
* [.htaccess Validator](https://shop.alterlinks.com/htaccess-validator/htaccess-validator.php)
* [HTML Compatibility Check for XHTML](https://web.archive.org/web/20101120133016/http://qa-dev.w3.org/appc/)
* [HTML Compressor](http://htmlcompressor.com/compressor/)
* [HTML Compressor (html-minifier)](https://npm.runkit.com/html-minifier)
* [HTML Formatter](https://www.freeformatter.com/html-formatter.html)
* [HTML, CSS, and Conformance Validator](https://validator.w3.org/unicorn/)
* [HTML, CSS, and JS Formatter](https://www.10bestdesign.com/dirtymarkup/)
* [HTML Outline Extractor](http://gsnedders.html5.org/outliner/)
* [HTML Validator (W3C)](https://validator.w3.org/)
* [HTML Validator (WDG)](https://web.archive.org/web/20150721050450/http://www.htmlhelp.com/tools/validator/)
* [HTML 5 Validator](https://html5.validator.nu/)
* [HTTP Header Editor (Request Maker; WebKit browser extension)](https://chrome.google.com/webstore/detail/request-maker/kajfghlhfkcocafkcjlajldicbikpgnp)
* [HTTP Header Editor (Tamper Data; Gecko browser extension)](https://web.archive.org/web/20150604025101/https://addons.mozilla.org/en-US/firefox/addon/tamper-data/)
* [HTTP Header Test](http://www.rexswain.com/httpview.html)
* [HTTP Header Test (Advanced)](https://www.askapache.com/online-tools/http-headers-tool/)
* [Image and Link Analysis](https://web.archive.org/web/20150816054027/http://tools.seochat.com/tools/broken-links-images-tool/)
* [Internationalization Check](https://validator.w3.org/i18n-checker/)
* [Internet Explorer Viewer (IE NetRenderer)](http://netrenderer.com/)
* [Internet Explorer Viewer (URL2PNG)](https://www.url2png.com/)
* [IP Address Trace](http://www.ip-tracker.org/)
* [IP Determiner (DSLReports)](https://web.archive.org/web/20150601091833/http://www.dslreports.com/whois)
* [IP Determiner](http://www.ipdatabase.com/)
* [IP Spam Check](http://www.spamhaus.org/lookup.lasso)
* [iPhone Emulator](https://web.archive.org/web/20160822221822/http://iphone4simulator.com/)
* [JavaScript Compressor](http://dean.edwards.name/packer/)
* [JavaScript Linter (JSHint)](https://jshint.com/)
* [JavaScript Linter (JSLint)](https://www.jslint.com/)
* [JSON Formatter](https://jsonformatter.curiousconcept.com/)
* [JSON Validator](https://jsoncompare.com/)
* [Layout Bug Test (script)](https://code.google.com/archive/p/fighting-layout-bugs/)
* [Link Analysis](http://juicystudio.com/services/linktest.php)
* [Link Check (LinkTiger)](http://www.linktiger.com/)
* [Link Check (Site Valet)](https://web.archive.org/web/20130714065334/http://valet.webthing.com/link/)
* [Link Check (W3C)](https://validator.w3.org/checklink)
* [Load Time and Object Check](http://www.websiteoptimization.com/services/analyze/)
* [Load Time Check](http://www.1-hit.com/all-in-one/tool.loading-time-checker.htm)
* [Lynx Viewer](http://www.delorie.com/web/lynxview.html)
* [Malware and Security Scanner](http://sitecheck.sucuri.net/)
* [Markup Validator](https://web.archive.org/web/20151006113546/http://www.validome.org/)
* [MD5 and SHA Hash Generator](http://onlinemd5.com/)
* [MD5 Encrypter](http://www.md5online.org/md5-encrypt.html)
* [Microformat Extractor and Transformer](https://web.archive.org/web/20150627202810/http://microform.at/)
* [Mobile Emulator](http://mtld.mobi/emulator.php)
* [Mobile-Friendliness Check](https://search.google.com/test/mobile-friendly)
* [MX Lookup](http://mxtoolbox.com/)
* [Network Intrusion Prevention and Analysis (Kismet; command-line tool)](http://kismetwireless.net/)
* [Network Intrusion Prevention and Analysis (Snort; command-line tool)](http://www.snort.org/)
* [Open Graph and Semantics Extractor](http://developers.facebook.com/tools/debug)
* [Opera Mini Emulator](http://opr.as/2cKpahy)
* [Password Generator (Arantius.com)](http://tools.arantius.com/password)
* [Password Generator (GRC)](http://www.grc.com/passwords.htm)
* [Password Generator (Packetizer)](http://secure.packetizer.com/pwgen/)
* [Password Security Check](https://howsecureismypassword.net/)
* [Password Security Check (GRC)](http://www.grc.com/haystack.htm)
* [Performance and Scalability Test (Pylot; command-line tool)](https://web.archive.org/web/20150619155406/http://www.pylot.org/)
* [Performance and Scalability Test (Tsung; command-line tool)](http://tsung.erlang-projects.org/)
* [PGP Decrypter](http://www.igolder.com/pgp/decryption/)
* [PGP Encrypter](http://www.igolder.com/pgp/encryption/)
* [PGP Key Generator](http://www.igolder.com/pgp/generate-key/)
* [Ping Tool](http://tools.pingdom.com/ping/)
* [Ping Tool (Regional)](https://www.dotcom-tools.com/ping-test)
* [P3P Validator](https://www.w3.org/P3P/validator.html)
* [QA Style Sheet (bookmarklet)](http://github.com/j9t/qa-style-sheet)
* [RDF Validator](https://www.w3.org/RDF/Validator/)
* [Reputation and Safety Check](https://www.mywot.com/)
* [Responsiveness Test](https://web.archive.org/web/20210506140954/https://www.viewlike.us/)
* [Reverse IP Lookup](http://mxtoolbox.com/ReverseLookup.aspx)
* [Rich Pin Validator](https://web.archive.org/web/20150615230955/https://developers.pinterest.com/rich_pins/validator/)
* [robots.txt Syntax Check](https://web.archive.org/web/20151126053219/http://tool.motoricerca.info/robots-checker.phtml)
* [RSS and Atom Feed Validator](https://validator.w3.org/feed/)
* [SADiC Validator](https://web.archive.org/web/20160322204459/https://www.the-web-middle-earth.com/sadic/sadicOnlineValidator.html)
* [SBML Validator](http://sbml.org/Facilities/Validator/)
* [Schema Generator](http://schema-creator.org/)
* [Section 508 Check](https://web.archive.org/web/20150706014945/http://www.508checker.com/)
* [Section 508 and WCAG 1.0 Check (Site Valet)](https://web.archive.org/web/20150707231218/http://valet.webthing.com/access/url.html)
* [Section 508 and WCAG 2.0 Check (Cynthia Says)](http://www.cynthiasays.com/)
* [Section 508, WCAG 2.0, and BITV 1.0 Check](http://achecker.ca/checker/)
* [Security Breach Victim Check](http://haveibeenpwned.com/)
* [Security Analysis (OWASP Mantra; browser extension)](http://sourceforge.net/projects/getmantra/)
* [Semantics Check (Gecko browser extension)](https://web.archive.org/web/20150426142109/https://addons.mozilla.org/en-US/firefox/addon/semantic-checker/)
* [Semantics Extractor](https://www.w3.org/2003/12/semantic-extractor.html)
* [Semantics Parser and Extractor](http://buzzword.org.uk/swignition/try)
* [SHA-512 Hash Generator](https://hash.online-convert.com/sha512-generator)
* [Sitemap Validator](https://web.archive.org/web/20160715025623/http://www.validome.org/google/validate)
* [SPDY Implementation Check](http://spdycheck.org/)
* [SQL Injection and Database Check (command-line tool)](http://sqlmap.org/)
* [SQL Injection Scanner (command-line tool)](https://wiki.owasp.org/index.php/Category:OWASP_SQLiX_Project)
* [SQL Validator](https://web.archive.org/web/20160821011626/http://developer.mimer.se/validator/index.htm)
* [SSL Certificate Check (DigiCert)](http://www.digicert.com/help/)
* [SSL Certificate Check (SSL Shopper)](http://www.sslshopper.com/ssl-checker.html)
* [SSL Client Check](http://www.howsmyssl.com/)
* [SSL Scanner (command-line tool)](http://github.com/iSECPartners/sslyze)
* [SSL Server Test](http://www.ssllabs.com/ssltest/)
* [Traceroute Tool](https://web.archive.org/web/20150627073214/https://cloudmonitor.ca.com/en/traceroute.php)
* [Structured Data Test (Google)](http://search.google.com/structured-data/testing-tool)
* [Structured Data Test (Yandex)](https://web.archive.org/web/20150319181926/https://webmaster.yandex.com/microtest.xml)
* [SVG Validator](https://web.archive.org/web/20050306190554/http://jiggles.w3.org/svgvalidator/ValidatorURI.html)
* [Traceroute Tool (Visualized)](https://web.archive.org/web/20140628001934/http://traceroute.monitis.com/)
* [Trustworthiness Check](https://www.scamadviser.com/)
* [Twitter Card Test](http://cards-dev.twitter.com/validator)
* [Type Diff](https://tiff.herokuapp.com/)
* [Type Live Test](https://web.archive.org/web/20160617205754/http://typewonder.com/)
* [Type Scale](https://type-scale.com/)
* [Type Scale (Modular)](https://www.modularscale.com/)
* [UI Test Automation (Ghost Inspector; browser extension)](https://ghostinspector.com/)
* [UI Test Automation (Screenster)](https://screenster.io/)
* [Universal Validator](http://watson.addy.com/)
* [User Agent Detector](http://ua.met.cz/)
* [User Identity Generator](https://www.fakenamegenerator.com/gen-random-us-us.php)
* [Viewport Size Determiner](https://www.internetmarketingninjas.com/seo-tools/whats-my-browser-size/)
* [Virus Scanner](http://www.virustotal.com/)
* [Wake-on-LAN Service](http://www.dslreports.com/wakeup)
* [WCAG 1.0 Check (SIDAR)](http://www.sidar.org/hera/)
* [WCAG 1.0 Check (TAW)](http://www.tawdis.net/)
* [WCAG 2.0 Check (BOIA)](http://www.boia.org/)
* [WCAG 2.0 Check (Evaluera)](http://www.evaluera.co.uk/)
* [Web Application Security Analysis (Canoo; command-line tool)](https://web.archive.org/web/20150330153931/http://webtest.canoo.com/webtest/manual/WebTestHome.html)
* [Web Application Security Analysis (OWASP; server application)](http://sourceforge.net/projects/owasp/)
* [Web Application Security Analysis (Skipfish; command-line tool)](http://github.com/spinkham/skipfish)
* [Web App Test Automation (command-line tool)](https://github.com/svenfuchs/steam)
* [Web Font Generator](https://www.fontsquirrel.com/tools/webfont-generator)
* [Website Analysis (Alexa)](https://www.alexa.com/)
* [Website Analysis (Nibbler)](https://nibbler.silktide.com/)
* [Website Analysis (RankFlex)](https://web.archive.org/web/20160617035405/http://www.rankflex.com/en/)
* [Website Analysis (Site Analyzer)](https://www.site-analyzer.com/)
* [Website Analysis (StatsCrop)](https://www.statscrop.com/)
* [Website Analysis (UITest.com)](https://uitest.com/check/)
* [Website Blockade Check for China](http://www.blockedinchina.net/)
* [Website Blockade Check for England](http://www.blocked.org.uk/)
* [Website Browser and Location Speed Test](https://www.dotcom-tools.com/website-speed-test)
* [Design Diff (script)](https://percy.io/)
* [Website Design History (DomainTools)](https://web.archive.org/web/20160121044614/https://research.domaintools.com/research/screenshot-history/)
* [Website Design History (Screenshots.com)](https://web.archive.org/web/20160706230510/http://www.screenshots.com/)
* [Website Fingerprint Check](http://www.grc.com/fingerprints.htm)
* [Website Grader](https://website.grader.com/)
* [Website Monitoring Service](http://www.montastic.com/)
* [Website Performance Analysis (GTmetrix)](http://gtmetrix.com/)
* [Website Performance Analysis (IISpeed)](http://www.iispeed.com/pagespeed/insights)
* [Website Performance Analysis (Page Performance; WebKit browser extension)](https://chrome.google.com/webstore/detail/page-performance/gembkfinllgmbkgbgdoaeopbahikjomp)
* [Website Performance Analysis (PageSpeed)](https://developers.google.com/speed/pagespeed/insights/)
* [Website Performance Analysis (Pingdom)](http://tools.pingdom.com/fpt/)
* [Website Performance Analysis (WebPageTest)](http://www.webpagetest.org/)
* [Website Performance Analysis (YSlow; browser extension)](http://yslow.org/)
* [Website Review](https://www.valuemyweb.com/reviewmyweb/reviewmyweb)
* [Website Technology Analysis](https://builtwith.com/)
* [Website Timer](http://www.octagate.com/service/SiteTimer/)
* [XHTML 1.0 Schema Validator](https://schneegans.de/sv/)
* [XML Schema Validator](https://web.archive.org/web/20130728234212/http://www.w3.org/2001/03/webdata/xsv)
* [XML Validator](https://www.xmlvalidation.com/)
* [XML Well-Formedness Check and Validator](https://www.cogsci.ed.ac.uk/~richard/xml-check.html)

## Summary

This was a brief treatise on the subject of website quality control. What have we learned?

Quality management consists of quality planning, quality control, quality assurance, and quality improvement, and it comes with a number of methods to identify (control), fix (improvement), and avoid defects (planning, assurance).

Website quality control entails the means to determine (a) whether websites meet our own expectations and (b) to what degree our websites meet professional best practices.

Quality control is important because otherwise we would have no way of knowing whether what we do and produce is any good. Quality control is professional; quality control saves time and money and sometimes nerves.

Quality control entails and must include a great number of tests, covering security, accessibility, usability, performance, functionality, maintainability, semantics, validation, layout and design consistency, typography, (general) code quality, and coding standard compliance.

In practice, quality control requires training, depends on our mindsets, stands and falls with automation, and needs enforcement.

And, finally, there are a gazillion tools for quality control and assurance.

Quality management is important, and no website should go without a plan for quality control.
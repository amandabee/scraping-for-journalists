# Reporting Examples
I asked the folks in NICAR-L about stories that they couldn't have written without scraping and got a nice list:

+ Micheal Keller's team at Daily Beast used web scraping to track [presidential candidates' ground games in 2012](http://www.thedailybeast.com/articles/2012/10/19/ground-game-obama-opens-up-big-lead-in-state-headquarters.html). Bonus: They [wrote about the process](http://web.archive.org/web/20130203110512/http://newsbeastlabs.tumblr.com/post/34109019268/tracking-the-presidential-groundgame-as-the-two) when they were done.

+ Reporters at The Baltimore Sun scraped Baltimore's finance department website after city officials said it wasn't possible to provide reporters with access to property tax records. Their [series on the unintended consequences of a local tax credit](http://www.baltimoresun.com/business/bs-bz-baltimore-homestead-credits-20111217,0,5608651.story) would not have been possible without that data.   
 
 + Megan Twohey and the data team at Reuters scraped five years worth of archives of multiple Yahoo Groups for their five part series on [disrupted adoptions](http://www.reuters.com/investigates/adoption/#article/part1). This was an 18 month project -- that included a great deal of data entry to clean and sort the scraped posts. 

+ ProPublica's Dollars for Docs

+ For a Marketplace story on [court debts in Philadelphia](http://www.marketplace.org/topics/wealth-poverty/philadelphia-collects-court-debt-decades-later), I scraped 200,000 records from a public records database so that I could analyze the debt data for Amanda Aronczyk, the reporter on the larger story. 

+ S. Heather Duncan at The Telegraph (Middle Georgia) got an assist from outside the newsroom to pull thousands of PDFs of state records on day care inspections. They had added work to parse those PDFs, but ultimately found that many centers are allowed to continue operating despite very serious safety violations and deficiencies. The state had insisted that the inspection reports were generated manually and that there wasn't any central database. [Many midstate day cares still operating despite violations](http://www.macon.com/2010/06/27/1178636/many-midstate-day-cares-still.html)

+ Jennifer Gollan and Shane Shifflett at CIR first transcribed a great stack of documents to produce a list of judges and the companies they own stock in. They then scraped PACER to find cases those judges had heard involving those companies and found multiple Federal judges who had failed to recuse themselves and instead had [ruled favoring companies they  had a financial stake in](https://www.baycitizen.org/news/courts/federal-judges-rulings-favored-companies/). Note: The Center for Investigative Reporting was able to get a public interest waiver from PACER, which otherwise [charges a per-docket fee](https://www.baycitizen.org/news/courts/pacer-federal-court-record-fees-exceed/), and then had that waiver revoked, leading to a [short court battle](http://www.courthousenews.com/2013/08/29/60733.htm), the upshot of which is that other non-profit news organizations may be eligible for fee exemptions. 

+ When Matt Wynn was at The Arizona Republic, two county offices claimed they were not able to cross reference two online databases and identify real estate investors benefitting from a tax rebate meant for homeowners. The AZ Republic scraped both databases and and found a [million dollars in fraudulent rebates](http://www.azcentral.com/arizonarepublic/news/articles/2010/05/02/20100502tax-rebate-errors.html). 

+ The local police in Eugene, OR publish a [call log](http://ceapps.eugene-or.gov/epdpubliccad/cadday.aspx) but they don't aggregage the info anywhere and it isn't very well organized. John Heasly the *Register Guard*  has a scraper that runs on a timer to [collect those call logs, format them and map them](http://projects.registerguard.com/police/eugene/). 

+ Griff Palmer at *The New York Times* scraped listings on an online firearm marketplace and used [regular expressions](https://github.com/amandabee/cunyjdata/blob/master/lecture%20notes/regex.md) to find phone numbers in those listings, allowing reporters to connect individual listings to convicted felons and highlight the gap in background check rules (which don't extend to private transactions).

+ Though Rhode Island's General Assembly does keep legislator attendance records, Tim Barman at *Providence Journal* wrote a program to scrape the daily House and Senate journals from Rhode Island's General Assembly to determine each legislators [attendance record](http://www.providencejournal.com/politics/rhode-island/general-assembly/legislator-attendance/) over the last decade. Barman also [wrote about his process on *Source*](http://source.mozillaopennews.org/en-US/articles/rhode-island-general-assembly-attendance-data/).

+ Martin Burch's power outage scraper

+ Jamie Smith-Hopkins at *The Baltimore Sun* scraped [city property tax records](http://cityservices.baltimorecity.gov/realproperty/) for their "Taxing Baltimore" series. The stories found at [dramatic variations in property tax rates](http://www.baltimoresun.com/business/bs-bz-baltimore-homestead-credits-20111217,0,5608651.story) and [landlords taking advantage of a tax credit meant for homeowners](http://www.baltimoresun.com/news/maryland/bs-md-homestead-double-dippers-20111217,0,3064226.story).

	> To understand the effects of the homestead break, The Sun requested information from the city showing the net tax bill and any tax credits for every property in the city. Baltimore's Finance Department said it couldn't provide that level of detail because the information was essentially trapped inside an aging mainframe computer.

	> Using an automated process called "data scraping," The Sun instead created its own database of all 237,000 city property tax records by copying the information, one record at a time, from the individual tax records publicly available on the city's website.

+ Michael Keller at *Al Jazeera* (Yes, the same Michael Keller of the Daily Beast example) used regular expressions to find transfer dates in the .txt version a series of PDFs on [DocumentCloud](http://www.documentcloud.org) for his [timeline of hunger strikes at Guantanamo Bay](http://america.aljazeera.com/articles/multimedia/guantanamo-hungerstriketimeline.html). For example, Yusef Abdullah Saleh al Rabiesh was [transferred to GTF GTMO on Jan 16, 2012](http://projects.nytimes.com/guantanamo/detainees/109-yusef-abdullah-saleh-al-rabiesh#p4) The date information was purely background and context, really not the main story at all. But without the dates, there's no way to appreciate the scale of the hunger strikes. Regular expressions helped find dates like "10 June 2012" as well as "June 10, 2012" and, since the documents had to be OCRd, sometimes the dates came up as ".Iune IO" for "June 10" 

+ Marc Ellison at *The Toronto Star*  scraped city lobbying activity for their [Lobby Watch](http://www.thestar.com/news/city_hall/lobbyists.html) series. He also [wrote about the process](http://www.thestar.com/news/gta/2013/07/31/lobby_watch_how_we_did_it.html). 

+ The Supreme Chi-Town Coding Crew isn't exactly a newsroom, but they use Python (specifically Django) to scrape the Cook County Sheriff's Inmate Locator every day and provide that [scraped data as a web API](http://cookcountyjail.recoveredfactory.net). By scraping daily, they have developed a data model that the jail administrators themselves do not have access to (such as a history of charges, court dates, and housing locations for each inmate during their stay in jail or in a jail-related program like electronic monitoring). 

Title: Cook County Jail Inmate data API
Source: https://github.com/sc3/cookcountyjail
API: http://cookcountyjail.recoveredfactory.net
Visualization: http://26thandcalifornia.recoveredfactory.net 

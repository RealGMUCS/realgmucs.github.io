<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@600;700;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">

<style>
:root {
  color-scheme: light dark;
  --bg-color: #ffffff;
  --text-primary: #0f172a;
  --text-secondary: #334155;
  --text-muted: #64748b;
  --card-bg: #ffffff;
  --border-color: #e2e8f0;
  --hover-bg: #f8fafc;
  --accent: #0f172a;
  --tag-bg: #f1f5f9;
  --tag-text: #334155;
  --bamboo-green: #2e9e64;
  --bamboo-green-hover: #1d7a4c;
  --font-heading: 'Outfit', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  --font-mono: ui-monospace, 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
  --radius-sm: 4px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --text-xs: 0.8rem;
  --text-sm: 0.875rem;
  --text-base: 1rem;
  --text-lg: 1.25rem;
  --text-3xl: 2.25rem;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg-color: #15181c;
    --text-primary: #f1f5f9;
    --text-secondary: #cbd5e1;
    --text-muted: #94a3b8;
    --card-bg: #1c2126;
    --border-color: #2d333b;
    --hover-bg: #20262d;
    --tag-bg: #232a31;
    --tag-text: #cbd5e1;
  }
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
  background-color: var(--bg-color);
  background-image: linear-gradient(rgb(46 158 100 / 3%) 1px, transparent 1px), linear-gradient(90deg, rgb(46 158 100 / 3%) 1px, transparent 1px);
  background-size: 28px 28px;
  color: var(--text-primary);
  font-family: var(--font-body);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

.stats-app {
  max-width: 880px;
  margin: 0 auto;
  padding: 3.5rem 1.5rem 4rem;
}

@media (max-width: 560px) {
  .stats-app {
    padding: 2rem 1rem 3rem;
  }
}

header {
  margin-bottom: 2rem;
}

.title-row {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 0.5rem;
}

h1.site-title {
  font-family: var(--font-heading);
  font-size: var(--text-3xl);
  font-weight: 800;
  letter-spacing: -0.02em;
  color: var(--text-primary);
  margin: 0;
}

.subtitle-row {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 0.5rem;
  margin-top: 0.35rem;
}

.site-subtitle {
  margin: 0;
  color: var(--text-secondary);
  font-size: var(--text-sm);
  font-family: var(--font-mono);
}

.site-subtitle span:first-child {
  color: var(--bamboo-green);
}

.top-nav {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.top-nav a {
  color: var(--text-secondary);
  font-size: var(--text-sm);
  font-weight: 600;
  text-decoration: none;
  padding: 0.25rem 0.65rem;
  border-radius: var(--radius-sm);
  transition: color 0.15s ease, background-color 0.15s ease;
}

.top-nav a:hover,
.top-nav a.active {
  color: var(--text-primary);
  background: var(--hover-bg);
}

.stat-tiles {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 0.75rem;
  margin: 1.5rem 0 2rem;
}

.stat-tile {
  padding: 0.9rem 0.75rem;
  text-align: center;
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-md);
  transition: transform 0.15s ease, border-color 0.15s ease;
}

.stat-tile:hover {
  border-color: var(--bamboo-green);
  transform: translateY(-2px);
}

.stat-tile-value {
  font-family: var(--font-heading);
  font-size: 1.6rem;
  font-weight: 800;
  color: var(--bamboo-green);
  line-height: 1.2;
}

.stat-tile-label {
  margin-top: 0.3rem;
  font-size: var(--text-xs);
  color: var(--text-secondary);
}

.stats-card {
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-md);
  padding: 1.5rem;
  margin-bottom: 1.75rem;
}

.stats-card h2, .stats-card h1 {
  font-family: var(--font-heading);
  font-size: 1.35rem;
  font-weight: 700;
  color: var(--text-primary);
  border-bottom: 2px solid var(--border-color);
  padding-bottom: 0.5rem;
  margin-top: 0;
  margin-bottom: 1rem;
}

.stats-card h3 {
  font-family: var(--font-heading);
  font-size: 1.1rem;
  font-weight: 600;
  color: var(--text-primary);
  margin-top: 1.25rem;
  margin-bottom: 0.5rem;
}

a {
  color: var(--bamboo-green);
  text-decoration: none;
  font-weight: 500;
}

a:hover {
  text-decoration: underline;
  color: var(--bamboo-green-hover);
}

ul, ol {
  margin: 0.5rem 0 1rem;
  padding-left: 1.4rem;
}

li {
  margin-bottom: 0.4rem;
  color: var(--text-primary);
}

blockquote {
  margin: 1rem 0;
  padding: 0.6rem 0.85rem;
  background: var(--hover-bg);
  border-left: 3px solid var(--bamboo-green);
  border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
  color: var(--text-secondary);
  font-size: var(--text-sm);
}

blockquote p {
  margin: 0;
}

img.hero-img, img.section-img {
  max-width: 100%;
  height: auto;
  border-radius: var(--radius-md);
  border: 1px solid var(--border-color);
  margin: 1rem 0;
  display: block;
}

details {
  background: var(--hover-bg);
  border: 1px solid var(--border-color);
  border-radius: var(--radius-md);
  padding: 0.75rem 1rem;
  margin: 0.75rem 0;
}

summary {
  font-weight: 600;
  cursor: pointer;
  color: var(--text-primary);
}
</style>

<div class="stats-app">

<header>
  <div class="title-row">
    <h1 class="site-title">GMU CS Stats</h1>
  </div>
  <div class="subtitle-row">
    <p class="site-subtitle"><span>George Mason University</span> · Department of Computer Science</p>
    <nav class="top-nav" aria-label="Primary navigation">
      <a href="./people/">Faculty/Staff</a>
      <a href="./people/students.html">Students/Alumni</a>
      <a href="./stats.md" class="active">Stats</a>
    </nav>
  </div>
</header>

<img class="hero-img" src="https://roars.dev/files/nguyen-engr.jpg" alt="Nguyen Engr building">

<div class="stat-tiles">
  <div class="stat-tile">
    <div class="stat-tile-value">#33</div>
    <div class="stat-tile-label">CSRankings ('25–'26)</div>
  </div>
  <div class="stat-tile">
    <div class="stat-tile-value">84</div>
    <div class="stat-tile-label">Total Faculty</div>
  </div>
  <div class="stat-tile">
    <div class="stat-tile-value">~200</div>
    <div class="stat-tile-label">Ph.D. Students</div>
  </div>
  <div class="stat-tile">
    <div class="stat-tile-value">~1100</div>
    <div class="stat-tile-label">M.S. Students</div>
  </div>
  <div class="stat-tile">
    <div class="stat-tile-value">~2600</div>
    <div class="stat-tile-label">Undergraduates</div>
  </div>
  <div class="stat-tile">
    <div class="stat-tile-value">$214M</div>
    <div class="stat-tile-label">Research Spending</div>
  </div>
</div>

<div class="stats-card">

# Why CS@GMU ?

- Reputation, quality, size steadily increase
  - [CSRankings](https://www.csrankings.org): **33** in '26,'25, 32 in '23--'24, 50 in '22, 60 in '21, 70 before 2020. See more details through [CSPicks](https://roars.dev/cspicks/?start=2016&end=2026&region=us&q=george+mason)
  - Faculty: double in size in past 3 years (84 total, 38 were new '20--'22)
  - Generous Ph.D. stipend: help recruit top students!
- Close to funding agencies NSF, DoD, NIH and industries (see Places below)
  - internships and opportunities for your students (or even yourself, e.g., Amazon Scholar program)
- Many generous internal (e.g., [IDIA](https://idia.gmu.edu)) and in-state grants (e.g., [CCI](https://cyberinitiative.org/))
- 1-semester study leave before tenure
- Flexible course scheduling: 2,3 days / week or 1 day / week
- On-campus living for faculty (Masonvale) and daycare for kids
- Active and helpful Slack channels!
  - questions about NSF? We have multiple faculty who are/were NSF directors / program managers
  - interested in Industrial funding? Our faculty win Amazon/Google/Meta awards every year (see [Awards](https://realgmucs.github.io/awards))

</div>

<div class="stats-card">

# GMU Computer Science

- *CS Rankings*: [33](https://www.csrankings.org) overall
  - top [25](https://csrankings.org/#/fromyear/2021/toyear/2026/index?all&us) in the last 5 years.
    - top 20 in mobile computing, software engineering, security, graphics and visualization. See ([CSPicks](https://roars.dev/cspicks/?start=2016&end=2026&region=us&q=george+mason) to see faculty and research strengths of GMU).
  - Learn more about the research strengths of GMU CS through [CSPicks](https://roars.dev/cspicks/?start=2016&end=2026&region=us&q=george+mason), which is developed at GMU CS.
- *Faculty*: 84 total (36 tenured, 21 tenure-track, 27 term)
  - 38 *new* faculty (27 tenured/tenure-track, 11 term) during Covid ('21--'23)
  - Research in a [wide range of areas](https://roars.dev/cspicks/?start=2016&end=2026&region=us&q=george+mason)
    - cybersecurity, cryptography, systems and networks, machine learning and data mining, artificial intelligence, robotics, mobile computing, natural language processing, theory, databases, bioinformatics, computer graphics, computer vision, HCI, and software engineering
  - [Awards](https://realgmucs.github.io/awards)
    - 10 Fellows (ACM, IEEE, etc)
    - 32 NSF CAREER and Young Investigator Awards
  - Many affiliated faculty from non-CS departments
  - Always [expanding](https://roars.dev/cspicks/?start=2016&end=2026&region=us&q=george+mason)

- *Students* (as of 2025)
  - ~200 Ph.D.
  - ~1100 M.S. (this is quite big compared to most other schools, 200 of them are in Software Engineering)
  - ~2600 undergraduate

- *Degrees*
  - Ph.D. in CS
  - MS in CS, MS in Software Engineering, MS in Information System
  - BS in CS and Applied CS

- Others
  - largest dept in the [College of Engineering and Computing](https://cec.gmu.edu)
  - TT track faculty, before tenure, can get a study leave semester (i.e., no teaching or services for a semester)

</div>

<div class="stats-card">

# GMU in general

- [R1](https://en.wikipedia.org/wiki/List_of_research_universities_in_the_United_States): Doctoral Universities – Very high research activity
  - $214M research spending in [2021](https://www.gmu.edu/news/2023-02/mason-research-shows-its-strength-nsf-report) (federal funding in Computer and Information Sciences #19 among all universities and #11 among public universities)
- 40,000+ students from 130 countries and all 50 states
  - **Largest** in Virginia
- Multiple campuses
  - Fairfax (main campus, where CS dept is)
  - Mason Square (Arlington)
  - Science and Technology (Manassas)
  - Mason Korea (Incheon Korea)
  - and [others](https://info.gmu.edu/campus-information/campuses-sites/)
- Age: 50 [in 2022](https://50th.gmu.edu)

</div>

<div class="stats-card">

# CS PhD Students' Stipend

- *GTA*
  - Full Tuition / Health Insurance / other benefits typical for R1 universities
- *GRA*: depending on advisor but at a minimum as good as GTA (usually better)
  - For example, I pay my students about $40K/year (including summer)
  - Overhead/Indirect: 58.9% (of MTDC). In short, about $70K budget per Ph.D. student

</div>

<div class="stats-card">

# PhD Application Info

- 2 LoRs
- GRE **NOT** required
- English tests through TOEFL/IELTS or Duolingo
  - **NOT** required for students from the US or from [these countries](#Standard-Tests-Waiver-Eligible-Countries)
- Eligible for _Presidential Scholarship_
  - awards to 2 incoming PhD students
  - at minimum as good as GTA

</div>

<div class="stats-card">

# Places

> estimated time from GMU

- Airports
  - Dulles IAD (30 mins)
  - Reagan DCA (30 mins)
  - Baltimore BWI (1 hr)
- Funding/Gov't Agencies
  - NSF (Alexandria VA, 30 mins): local for NSF Panel meetings
  - DARPA (Arlington VA, 30 mins)
  - DoD Pentagon (Arlington VA, 30 mins)
  - DoE (DC, 30 mins)
  - NASA (DC, 30 mins)
  - NIH (Bethesda MD, 40 mins)
  - Dept. Of Homeland Security (DHS) (DC, 30 mins)
  - National Security Agency (NSA) (Fort Meade MD 1 hr)
  - Dept. of Agriculture (USDA) (DC, 30 mins)
  - National Institute of Standards and Technology (NIST) (Gaithersburg MD, 40 mins)
  - CIA (Langley VA, 20 mins)

- Research Labs
  - NASA Goddard (Greenbelt MD, 1 hr)
  - Naval Research Lab (DC, 30 mins)
  - Institute for Defense Analyses (IDA) (Alexandria VA, 30 mins)
  - Johns Hopkins University Applied Physics Laboratory (APL) (Laurel MD, 1 hr)
  - Army Research Laboratory (ARL) (Adelphi MD, 40 mins)
  - National Oceanic and Atmospheric Administration (NOAA) (Silver Spring MD, 40 mins)

- Industry
  - Accenture Federal Services
  - Amazon
    - AWS (Herndon VA, 30 mins)
    - [Amazon HQ2](https://www.amazon.jobs/en/locations/arlington) (Arlington VA, 30 mins) is [now opened](https://www.cnbc.com/2023/06/19/why-amazon-built-hq2-and-how-covid-pandemic-reshaped-it.html)
  - [Upcoming Boeing HQ](https://www.washingtonpost.com/dc-md-va/2022/05/14/boeing-headquarters-move-arlington-chicago/) (Arlington VA, 30 mins)
  - Booz Allen Hamilton
  - Capital One
  - Facebook (DC office)
  - General Dynamics Information Technology
  - Leidos
  - Lockheed Martin
  - MITRE
  - Micron
  - Northrop Grumman
  - Raytheon Technologies
  - Science Applications International Corporation (SAIC)
  - and [a lot more](https://en.wikipedia.org/wiki/List_of_companies_headquartered_in_Northern_Virginia)

- Cities
  - Washington DC (30 mins)
  - Baltimore (1 hr)
  - Philadelphia (2:45 hrs)
  - Pittsburgh (4 hrs)
  - New York (4 hrs)

- Schools/Universities
  - Thomas Jefferson High School (Alexandria VA, 20 mins)
    - [#1](https://www.usnews.com/education/best-high-schools/national-rankings) HS in the US
    - Many faculty mentor TJHS students
  - American Univ. (30 mins)
  - Howard Univ. (30 mins)
  - Georgetown University (30 mins)
  - George Washington Univ. (30 mins)
  - Univ of Maryland-College Park (45 mins)
  - Johns Hopkins (1:45 hrs)
  - Univ of Virginia (2 hrs)
  - Virginia Commonwealth University (1.5 hrs)
  - Virginia Tech (4 hrs)
  - CMU (4 hrs)

- Miscs
  - White House (30 mins)

</div>

<div class="stats-card">

# Health & Life Quality & Others

- Healthiest College town
  - Fairfax, VA (home of GMU) [#2 healthiest college town](https://brokescholar.com/americas-healthiest-college-towns) in US
  - #1 is College Park, MD (UMD), #3 is Berkeley, CA (UC-Berkeley)
- Public schools:
  - The top public school systems in VA are in Northern VA, according to Niche'22's Best School Districts in Virginia
  - E.g., Arlington (1), Fairfax (2), Loudoun (3), Falls Church (4)

- Naturally Beautiful
  - stunning natural display of autumn leaf colors (Oct - mid Nov): [picture](https://roars.dev/files/autumn.jpeg) taken at GMU Fairfax
  - Cherry Blossom right on [campus](https://www.youtube.com/watch?v=gcBYRc23PYM)! (and of course the national one is in DC in the Spring around March)
  - Shenandoah National Park and [many more](https://www.onlyinyourstate.com/dc/natural-attractions-washington-dc/)

- Also, DC has **highest concentration of museums** in the world
  - 70+ museums in the city

</div>

<div class="stats-card">

# Things to keep in mind

> No place is perfect, here are some of the complaints you may hear about the area

- Living cost of NOVA: 43.33% higher than the national average!
  - Median household is ~105K (US Census'22)
    - National median is ~69K
  - Fairfax median household is $125K, making it ~55% higher than national average !!!
    - likely many of your neighbors will make more than you!

- Housing
  - Median home value in Fairfax is $646K (comparing to the national median of $310K, Zillow'22)

- Traffic: DC area (which includes NOVA) consistently ranked among the most congested cities in the US

- **But all of these are nowhere compared to other big cities including the Bay Area, New York, Boston, Seattle**

</div>

<div class="stats-card">

# Interesting Things

- GMU Fairfax is the first campus in the country that adopts the [Starship Robots](https://en.wikipedia.org/wiki/Starship_Technologies) for deliveries (in 2019)
  - ~60 robots
  - completed 335,489+ orders
    - 39,828 coffees delivered.
    - most popular item is Steak ‘N Shake’s The Original Double ‘N Fries (ordered 13,637 times!)
- The [Zotero](https://www.zotero.org) reference manager was created at GMU ([Center for History and New Media](https://rrchnm.org/))!
- VA is the [most patriotic state](https://wallethub.com/edu/most-patriotic-states/13680) in the US (based on Military Enlistees/Veterans and Voters). It is also designated as the "Purple Heart State".
- VA is known as the **Mother of Presidents**
  - 8 total: George Washington, Thomas Jefferson, James Madison, James Monroe, William Henry Harrison, John Tyler, Zachary Taylor, and Woodrow Wilson
  - also known as the "Birthplace of a Nation"
- Naval Station Norfolk, Norfolk, VA is the **largest naval base in the world**
  - 3,400 acres and including over 100 piers and wharves.
  - Home to over 75 ships and submarines, and over 130 aircraft, and serves as the headquarters for the Atlantic Fleet of the U.S. Navy
- Home to the Pentagon, the **[largest office building in the world](https://en.wikipedia.org/wiki/List_of_largest_office_buildings)** (over 6 million square feet of space)
- #5th in the US for the **wine industry**
  - 300 wineries and an industry worth over $1.37 billion; known for production of Virginia, Cabernet Franc, and Petit Verdot.
- **Pocahontas**, the famous Native American woman who played a key role in early English settlement in Virginia, was born in what is now modern-day Virginia.
- Has the longest continuous roadway in the world:
  - 469-mile-long Blue Ridge Parkway, which winds through Virginia and North Carolina, is the longest continuous roadway in the world that was designed specifically for scenic driving
- Appomattox, VA is where General Robert Lee surrendered to General Ulysses Grant, effectively ending the American Civil War
- In the event of nuclear war, we're close to ground zero (ouch).
- GMU started life as a UVA satellite and grew its reputation by being a basketball underdog (that's OK, being an underdog appears to help us flourish, e.g., largest university in VA).
- GMU is the **youngest R1 university** in the US (became R1 in 2016).

</div>

<div class="stats-card">

# Other stuff

### Useful Links
- [GMU Stats and Figures](https://oiep.gmu.edu/resources/fast-facts/)

### Standard Tests Waiver-Eligible Countries
<details>
<summary>Non-US Countries that do not have to take standard tests</summary>

https://www.gmu.edu/international/english-language-requirements
</details>

<img class="section-img" src="https://roars.dev/files/gmu.jpg" alt="GMU">

</div>

</div>

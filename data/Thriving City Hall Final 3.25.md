**Thriving City Hall Pillar**

**Summary of Targeted Problem Statement Discussion**

Participants reviewed three draft targeted problem statements focused on improving how City Hall functions internally and how residents experience City services. The discussion emphasized ensuring that hackathon challenges are both clear and feasible for outside participants, while still addressing meaningful operational challenges.

**Resident Access to City Services**

Participants discussed the difficulty residents face when trying to determine how to interact with City services. Residents often struggle to determine:

- Which department handles their issue

- Whether their problem requires submitting a service request

- Which request category to select within the 311 system

This frequently leads to incorrectly categorized requests, additional manual routing by staff, and frustration for residents. Several participants noted that the underlying issue is not that residents submit unnecessary requests, but that the City's information architecture is department-centric rather than citizen-centric. The website and service request systems reflect internal organizational structures rather than how residents think about problems.

Participants also noted that:

- Website search functions are often ineffective

- Information can be outdated or difficult to locate

- Request categories overlap, making them difficult for residents to interpret

- Citizens often submit requests even when no clear category fits their issue

The group suggested that better front-end tools, guidance systems, or search capabilities could help residents understand the appropriate next step before submitting a request.

**Identifying the Best Procurement Contracts**

The third targeted problem statement addressed procurement and purchasing. City staff must evaluate contracts from multiple sources, including:

- City contracts

- State (VITA) contracts

- Federal (GSA) contracts

- Cooperative purchasing agreements

Determining the best purchasing option often requires extensive manual analysis of contract documents. Much of the relevant information exists within PDF documents, making it difficult to compare contracts or identify better purchasing options.

Participants noted that staff must manually evaluate:

- Contract validity

- expiration dates

- compliance with procurement rules

- cost competitiveness

Technology could potentially assist by extracting contract data from documents, identifying expiring agreements, and highlighting alternative purchasing options. However, participants emphasized that final determinations regarding legal compliance would still require human review.

While technically complex, this challenge could produce significant financial savings and operational efficiencies if addressed successfully.

**Summary of Blue Sky Discussion**

**Fragmented Systems Create Burdens for Residents**

Participants repeatedly noted that many City systems operate independently, requiring residents to navigate multiple platforms and departments to solve a single problem. This fragmentation places the burden of coordination on residents as well as the City.

Many resident frustrations stem from the City's technology environment consisting of numerous disconnected systems that do not easily share information. Internally, there are 47+ systems with multiple logins, disconnected tools, and siloed processes.

**Inconsistent Customer Experience**

Participants shared examples of everyday interactions with City services that can be confusing or frustrating. These included:

- malfunctioning payment kiosks

- complex service request processes

- multiple steps required to resolve simple issues

- inconsistent communication about service outcomes

Even small failures in service systems can significantly impact residents' perception of government effectiveness.

**Internal Silos Limit Problem-Solving**

Participants also noted that City staff often work within department-specific processes and tools, which can reinforce siloed operations. This can limit cross-department collaboration and make it harder to solve problems that span multiple City functions. Several participants suggested that better tools and systems could help staff focus more on solving problems rather than navigating internal procedures.

**Transparency and Civic Understanding**

Another theme was the difficulty residents face in understanding how City decisions are made and how public funds are used. Participants suggested that improved communication tools and clearer information could help residents:

- better understand policy decisions

- follow issues that affect their neighborhoods

- see how City resources are being used

Improved transparency could help strengthen civic trust and engagement.

**Training and Internal Tools**

Some participants noted that internal operational tools and training practices vary widely across departments. Inconsistent use of basic tools such as job descriptions, performance metrics, and standardized workflows can make it difficult to maintain accountability and consistent service delivery.

Technology could potentially help standardize some of these processes and improve internal management practices.

**Participants**

- Danny Avula --- Mayor of Richmond, City of Richmond

- Michael Kolbe --- Policy Advisor, Mayor's Office

- Doug Gernat --- Sr. Deputy Director for Strategy, City of Richmond

- Pete Breil --- Director, Citizen Service and Response (311)

- Ryan Shriver --- CTO, Commonwealth Savers

- Ankit Mathur --- CTO, UNOS

- Marcus Thoreson --- Data Scientist, UNOS

**\**

**PILLAR: THRIVING CITY HALL**

**Revised Targeted Statement 1: Helping Residents Find the Right City Service or Next Step**

**Problem Statement\**
How might we use technology to help Richmond residents quickly determine the right next step when interacting with City services---whether finding information or submitting a request---so that issues are routed correctly the first time while working within existing City systems and minimizing additional staff workload?

**Context**\
Residents often come to rva.gov or RVA311 with a real need, but they may not know which department handles the issue, which request type applies, or whether they need information, a form, or a service request. At the same time, City information is spread across multiple pages and systems, and residents may struggle to tell what is current, relevant, or authoritative. When people cannot easily find the right path, they may submit the wrong request type, contact staff directly, or abandon the process entirely. This creates extra work for City teams and a frustrating experience for residents. Improving this front-end experience would support the MAP's goals of providing white glove service, making systems easier to use, and improving resident trust in City government.

Richmond residents currently interact with City services through several primary channels including rva.gov, RVA311 (web and mobile), and phone-based 311 service requests. The RVA311 platform organizes requests into dozens of service categories that route issues to different departments. However, residents must often select the correct category themselves, and the website's search and navigation structure reflects internal departments rather than how residents describe problems.

**Constraints**

- Must work with existing City systems such as rva.gov and RVA311

- Must rely on verified City information only

- Must avoid confidently answering when information is unclear, outdated, or conflicting

- Must reduce staff burden rather than increase it

- Must respect current system and data limitations

**Success Would Mean**

- Residents can describe their issue in plain language and get the right next step

- More requests are routed correctly the first time

- Fewer residents are forced to guess which category or department applies

- Staff spend less time redirecting routine inquiries

- The City gains better insight into where website content and service pathways are failing

**Possible Datasets**

- rva.gov and RVA311 websites

- RVA311 Service Request Categories

- Anonymized 311 Service Requests

- City Department Directory

- 311 Agent Job Aids (optional)

**Example ideas a hackathon group might create**

- City Services Copilot: a plain-language assistant that guides residents to the right department, form, or request type

- Smart Request Router: a front-end workflow that asks a few simple questions and routes users to the correct service path

- Content Gap Detector: a tool that analyzes common resident questions and flags where rva.gov content is outdated, unclear, or missing

**PILLAR: THRIVING CITY HALL**

**PILLAR: THRIVING CITY HALL**

**Revised Targeted Statement 2: Helping City Staff Review Upcoming Procurement Risks & Opps**

**Problem Statement**

How might we use technology to help Richmond staff identify valid, compliant, and cost-effective purchasing contracts across City, state, and federal sources so that procurement decisions require less manual review while maintaining legal compliance and transparency?

**Context\**

City staff rely on multiple contract sources and contract documents to make procurement decisions, but important details such as expiration dates, renewal windows, pricing terms, and contract conditions are often buried in PDFs or spread across different systems. Reviewing this information manually takes significant staff time and makes it harder to consistently spot what is expiring, what needs action, and what may no longer be the best option. In the workshop, this broader procurement challenge felt too large as originally framed, but participants saw clear value in narrowing the problem to a more specific use case that could be both hackable and useful. Improving this process would support the MAP's goals of improving core operations, stewarding public resources effectively, and increasing procurement compliance.

City procurement contracts are stored in document repositories and public procurement records. These documents typically include expiration dates, renewal terms, pricing language, and vendor information, but this information is often embedded in PDF documents rather than structured datasets. As a result, staff must manually review documents to identify contract risks or upcoming renewal windows.

**Constraints**

- Must comply with procurement law and City procurement policies

- Must support staff judgment rather than replace it

- Must work with existing contract repositories and document formats

- Must use publicly available or City-accessible contract information

- Must be scoped tightly enough for a weekend prototype

**Success Would Mean**

- Staff can more easily see which contracts are expiring or need review

- Key procurement details are easier to extract from existing contract documents

- Departments spend less time manually scanning PDFs and databases

- The City reduces the risk of missed renewals or outdated contract use

- Procurement teams have a clearer early-warning view of upcoming decisions

**Possible Datasets**

- Sample Richmond procurement contracts

- Contract metadata

- VITA/GSA contract listings

- Cooperative purchasing catalogs

**Example ideas a hackathon group might create**

- **Contract Renewal Radar:** a dashboard that identifies upcoming contract end dates and renewal windows

- **Procurement PDF Extractor:** a tool that pulls key fields like expiration date, pricing language, and terms from contract documents

- **Contract Review Triage Tool:** a system that flags contracts for follow-up based on timing, missing fields, or likely risk indicators

**Possible Blue Sky Statements**

1.  **Unified Digital Front Door**

How might we use technology to create a unified digital front door to City Hall so that residents experience government as one coordinated system rather than a collection of departments?

2.  **Better Communication Between City and Residents**

How might we use technology to improve communication between Richmond residents and City Hall so that people feel informed, heard, and guided at every step?

3.  **Aligning Employee Tools With City Mission**

How might we use technology to improve the daily tools and interfaces City employees use so that their work feels more connected to problem-solving, service, and the mission of the City?

4.  **Making Fiscal Responsibility More Visible**

How might we use technology to help residents understand how City resources are being used and what public investment leads to so that government feels more transparent and trustworthy?

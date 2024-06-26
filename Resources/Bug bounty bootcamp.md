# PART I: THE INDUSTRY
## Chapter 1: picking a bug bounty program
- Bug bounty programs: are they all the same? Finding the right program to target is the first step to becoming a successful bug bounty hunter. Many programs have emerged within the past few years, and it’s difficult to figure out which ones will provide the best monetary rewards, experience, and learning opportunities. 
### The state of the industry
- In 1995, Netscape launched the first-ever bug bounty program. The company encouraged users to report bugs found in its brand-new browser, the Netscape Navigator 2.0, introducing the idea of crowdsourced security testing to the internet world. Mozilla launched the next corporate bug bounty program nine years later, in 2004, inviting users to identify bugs in the Firefox browser
- But it was not until the 2010s that offering bug bounties become a popular practice. That year, Google launched its program, and Facebook followed suit in 2011. These two programs kick-started the trend of using bug bounties to augment a corporation’s in-house security infrastructure.
- The two largest of these platforms, HackerOne and Bugcrowd, both launched in 2012.
### Asset types
- In the context of a bug bounty program, an asset is an application, website, or product that you can hack.
- There are different types of assets, each with its own characteristics, requirements, and pros and cons. After considering these differences, you should choose a program with assets that play to your strengths, based on your skill set, experience level, and preferences.
#### Social sites and applications
- Anything labeled social has a lot of potential for vulnerabilities, because these applications tend to be complex and involve a lot of interaction among users, and between the user and the server. That’s why the first type of bug bounty program we’ll talk about targets social websites and applications. The term social application refers to any site that allows users to interact with each other. Many programs belong to this category: examples include the bug bounty program for HackerOne and programs for Facebook, Twitter, GitHub, and LINE.

- Social applications need to manage interactions among users, as well as each user’s roles, privileges, and account integrity. They are typically full of potential for critical web vulnerabilities such as insecure direct object references (IDORs), info leaks, and account takeovers. These vulnerabilities occur when many users are on a platform, and when applications mismanage user information; when the application does not validate a user’s identity properly, malicious users can assume the identity of others.

- These complex applications also often provide a lot of user input opportunities. If input validation is not performed properly, these applications are prone to injection bugs, like SQL injection (SQLi) or cross-site scripting (XSS). If you are a newcomer to bug bounties, I recommend that you start with social sites. The large number of social applications nowadays means that if you target social sites, you’ll have many programs to choose from.

- Also, the complex nature of social sites means that you’ll encounter a vast attack surface with which to experiment. (An application’s attack surface refers to all of the application’s different points that an attacker can attempt to exploit.) Finally, the diverse range of vulnerabilities that show up on these sites means that you will be able to quickly build a deep knowledge of web security.

- The skill set you need to hack social programs includes the ability to use a proxy, like the Burp Suite proxy introduced in Chapter 4, and knowledge about web vulnerabilities such as XSS and IDOR. You can learn more about these in Chapters 6 and 10. It’s also helpful to have some JavaScript programming skills and knowledge about web development. 
- However, these skills aren’t required to succeed as a hacker. But these programs have a major ***DOWNSIDE***. Because of the popularity of their products and the low barrier of entry, they’re often very competitive and have many hackers hunting on them. Social media platforms such as Facebook and Twitter are some of the most targeted programs.
#### General web applications
- General web applications are also a good target for beginners. Here, I am referring to any web applications that do not involve user-to-user interaction. Instead, users interact with the server to access the application’s features. Targets that fall into these categories can include static websites, cloud applications, consumer services like banking sites, and web portals of Internet of Things (IoT) devices or other connected hardware.

- That said, in my experience, they tend to be a little more difficult to hack than social applications, and their attack surface is smaller. If you’re looking for account takeovers and info leak vulnerabilities, you won’t have as much luck because there aren’t a lot of opportunities for users to interact with others and potentially steal their information

- You’ll need to look for server-side vulnerabilities and vulnerabilities specific to the application’s technology stack. You could also look for commonly found network vulnerabilities, like subdomain takeovers. This means you’ll have to know about both client-side and server-side web vulnerabilities, and you should have the ability to use a proxy. It’s also helpful to have some knowledge about web development and programming. These programs can range in popularity. However, most of them have a low barrier of entry, so you can most likely get started hacking right away!

#### Mobile Applications (Android, iOS, and Windows)
- After you get the hang of hacking web applications, you may choose to specialize in mobile applications. Mobile programs are becoming prevalent; after all, most web apps have a mobile equivalent nowadays. They include programs for Facebook Messenger, the Twitter app, the LINE mobile app, the Yelp app, and the Gmail app. 

- Hacking mobile applications requires the skill set you’ve built from hacking web applications, as well as additional knowledge about the structure of mobile apps and programming techniques related to the platform. You should understand attacks and analysis strategies like certificate pinning bypass, mobile reverse engineering, and cryptography. 

- Hacking mobile applications also requires a little more setup than hacking web applications, as you’ll need to own a mobile device that you can experiment on. A good mobile testing lab consists of a regular device, a rooted device, and device emulators for both Android and iOS. 
	- A rooted device is one for which you have admin privileges. It will allow you to experiment more freely, because you can bypass the mobile system’s safety constraints. An emulator is a virtual simulation of mobile environments that you run on your computer. It allows you to run multiple device versions and operating systems without owning a device for each setup. 
- For these reasons, mobile applications are less popular among bug bounty hunters than web applications. However, the higher barrier of entry for mobile programs is an advantage for those who do participate. These programs are less competitive, making it relatively easy to find bugs.
#### APIs
- Application programming interfaces (APIs) are specifications that define how other applications can interact with an organization’s assets, such as to retrieve or alter their data. For example, another application might be able to retrieve an application’s data via Hypertext Transfer Protocol (HTTP) messages to a certain endpoint, and the application will return data in the format of Extensible Markup Language (XML) or JavaScript Object Notation (JSON) messages. 
- Some programs put a heightened focus on API bugs in their bug bounty programs if they’re rolling out a new version of their API. A secure API implementation is key to preventing data breaches and protecting customer data. Hacking APIs requires many of the same skills as hacking web applications, mobile applications, and IoT applications. But when testing APIs, you should focus on common API bugs like data leaks and injection flaws.
#### Source Code and Executables
- If you have more advanced programming and reversing skills, you can give source code and executable programs a try. These programs encourage hackers to find vulnerabilities in an organization’s software by directly providing hackers with an open source codebase or the binary executable. Examples include the Internet Bug Bounty, the program for the PHP language, and the WordPress program.
- Hacking these programs can entail analyzing the source code of open source projects for web vulnerabilities and fuzzing binaries for potential exploits. You usually have to understand coding and computer science concepts to be successful here. You’ll need knowledge of web vulnerabilities, programming skills related to the project’s codebase, and code analysis skills. Cryptography, software development, and reverse engineering skills are helpful. 
- Source code programs may sound intimidating, but keep in mind that they’re diverse, so you have many to choose from. You don’t have to be a master programmer to hack these programs; rather, aim for a solid understanding of the project’s tech stack and underlying architecture. Because these programs tend to require more skills, they are less competitive, and only a small proportion of hackers will ever attempt them.
#### Hardware IoT
- Last but not least are hardware and IoT programs. These programs ask you to hack devices like cars, smart televisions, and thermostats. Examples include the bug bounty programs of Tesla and Ford Motor Company. You’ll need highly specific skills to hack these programs: 
	- you’ll often have to acquire a deep familiarity with the type of device that you’re hacking, in addition to understanding common IoT vulnerabilities. You should know about web vulnerabilities, programming, code analysis, and reverse engineering. Also, study up on IoT concepts and industry standards such as digital signing and asymmetric encryption schemes. Finally, cryptography, wireless hacking, and software development skills will be helpful too.
-  Since these programs require specialized skills and a device, they tend to be the least competitive.
### Bug Bounty Platforms
- Bug bounty platforms are websites through which many companies host their programs. Usually, the platform directly awards hackers with reputation points and money for their results. Some of the largest bug bounty platforms are HackerOne, Bugcrowd, Intigriti, Synack, and Cobalt.
- From the hacker’s perspective, bug bounty platforms provide a centralized place to submit reports. They also offer a seamless way to get recognized and paid for your findings. On the other hand, many organizations host and manage their bug bounty programs without the help of platforms. Companies like Google, Facebook, Apple, and Medium do this. You can find their bug bounty policy pages by visiting their websites, or by searching “CompanyName bug bounty program” online.
#### PROS
- The best thing about bug bounty platforms is that they provide a lot of transparency into a company’s process, because they post disclosed reports, metrics about the programs’ triage rates, payout amounts, and response times. Independently hosted programs often lack this type of transparency. In the bug bounty world, triage refers to the confirmation of vulnerability
- Bug bounty programs also often have reputation systems that allow you to showcase your experience so you can gain access to invite-only bug bounty programs. Another pro of bug bounty platforms is that they often step in to provide conflict resolution and legal protection as a third party. If you submit a report to a non-platform program, you have no recourse in the final bounty decision.
- Ultimately, you can’t always expect companies to pay up or resolve reports in the current state of the industry, but the hacker-to-hacker feedback system that platforms provide is helpful.
#### CONS
- However, some hackers avoid bug bounty platforms because they dislike how those platforms deal with reports. Reports submitted to platformmanaged bug bounty programs often get handled by triagers, third-party employees who often aren’t familiar with all the security details about a company’s product. Complaints about triagers handling reports improperly are common.
- Programs on platforms also break the direct connection between hackers and developers. With a direct program, you often get to discuss the vulnerability with a company’s security engineers, making for a great learning experience.
- Finally, public programs on bug bounty platforms are often crowded, because the platform gives them extra exposure. On the other hand, many privately hosted programs don’t get as much attention from hackers and are thus less competitive. And for the many companies that do not contract with bug bounty platforms, you have no choice but to go off platforms if you want to participate in their programs.
### Scope, Payouts, and Response Times
- you consider when picking a program, besides its asset types and platform? On each bug bounty program’s page, metrics are often listed to help you assess the program. These metrics give insight into how easily you might be able to find bugs, how much you might get paid, and how well the program operates.
#### Scope
- Program Scope First, consider the scope. A program’s scope on its policy pages specifies what and how you are allowed to hack. There are two types of scopes: asset and vulnerability. The asset scope tells you which subdomain, products, and applications you can hack. And the vulnerability scope specifies which vulnerabilities the company will accept as valid bugs.
- Any program with large asset and vulnerability scopes is a good place to start for a beginner. The larger the asset scope, the larger the number of target applications and web pages you can look at. When a program has a big asset scope, you can often find obscure applications that are overlooked by other hackers. 
	- This typically means less competition when reporting bugs. The larger the vulnerability scope, the more types of bugs the organization is willing to hear reports about. These programs are a lot easier to find bugs in, because you have more opportunities, and so can play to your strengths.
#### Payouts
- The next metric you should consider is the program’s payout amounts. There are two types of payment programs: 
	- vulnerability disclosure programs (VDPs) and bug bounty programs. VDPs are reputation-only programs, meaning they do not pay for findings but often offer rewards such as reputation points and swag. They are a great way to learn about hacking if making money is not your primary objective. Since they don’t pay, they’re less competitive, and so easier to find bugs in. You can use them to practice finding common vulnerabilities and communicating with security engineers.
#### Response Time
- Finally, consider the program’s average response time. Some companies will handle and resolve your reports within a few days, while others take weeks or even months to finalize their fixes. Delays often happen because of the security team’s internal constraints, like a lack of personnel to handle reports, a delay in issuing security patches, and a lack of funds to timely reward researchers. Sometimes, delays happen because researchers have sent bad reports without clear reproduction steps. Prioritize programs with fast response times. Waiting for responses from companies can be a frustrating experience, and when you first start, you’re going to make a lot of mistakes. You might misjudge the severity of a bug, write an unclear explanation, or make technical mistakes in the report. Rapid feedback from security teams will help you improve, and turn you into a competent hacker faster.
### Private Programs
- Most bug bounty platforms distinguish between public and private programs. Public programs are those that are open to all; anyone can hack and submit bugs to these programs, as long as they abide by the laws and the bug bounty program’s policies. 
- On the other hand, private programs are open to only invited hackers. For these, companies ask hackers with a certain level of experience and a proven track record to attack the company and submit bugs to it. Private programs are a lot less competitive than public ones because of the limited number of hackers participating. Therefore, it’s much easier to find bugs in them. Private programs also often have a much faster response time, because they receive fewer reports on average.
- Different bug bounty platforms will have different algorithms to determine who gets the invites, but here are some tips to help you get there. First, submit a few bugs to public programs. To get private invites, you often need to gain a certain number of reputation points on a platform, and the only way to begin earning these is to submit valid bugs to public programs. You should also focus on submitting high-impact vulnerabilities. These vulnerabilities will often reward you with higher reputation points and help you get private invites faster.
- Finally, be polite and courteous when communicating with security teams. Being rude or abusive to security teams will probably get you banned from the program and prevent you from getting private invites from other companies.
### Choosing the right program
- Bug bounties are a great way to gain experience in cybersecurity and earn extra bucks. But the industry has been getting more competitive. As more people are discovering these programs and getting involved in hacking on them, it’s becoming increasingly difficult for beginners to get started. That’s why it’s important to pick a program that you can succeed in from the very start.
- Before you develop a bug hunter’s intuition, you often have to rely on low-hanging fruit and well-known techniques. This means many other hackers will be able to find the same bugs, often much faster than you can. It’s therefore a good idea to pick a program that more experienced bug hunters pass over to avoid competition. You can find these underpopulated programs in two ways: look for unpaid programs or go for programs with big scopes.
- Try going for vulnerability disclosure programs first. Unpaid programs are often ignored by experienced bug hunters, since they don’t pay monetary rewards. But they still earn you points and recognition! And that recognition might be just what you need to get an invite to a private, paid program.
- Picking a program with a large scope means you’ll be able to look at a larger number of target applications and web pages. This dilutes the competition, as fewer hackers will report on any single asset or vulnerability type. Go for programs with fast response times to prevent frustration and get feedback as soon as possible.
- One last thing that you can incorporate into your decision process is the reputation of the program. If you can, gather information about a company’s process through its disclosed reports and learn from other hackers’ experiences. Does the company treat its reporters well? Are they respectful and supportive? Do they help you learn? Pick programs that will be supportive while you are still learning, and programs that will reward you for the value that you provide. Choosing the right program for your skill set is crucial if you want to break into the world of bug bounties.
### A Quick Comparison of Popular Programs
- After you’ve identified a few programs that you are interested in, you could list the properties of each one to compare them. In Table 1-1, let’s compare a few of the popular programs introduced in this chapter.
- Table 1-1: A Comparison of Three Bug Bounty Programs: HackerOne, Facebook, and GitHub
- ***P39/418***

## Chapter 2: sustaining your success
- Even if you understand the technical information in this book, you may have difficulty navigating the nuances of bug bounty programs. Or you might be struggling to actually locate legitimate bugs and aren’t sure why you’re stuck. In this chapter, we’ll explore some of the factors that go into making a successful bug bounty hunter. We’ll cover how to write a report that properly describes your findings to the security team, build lasting relationships with the organizations you work with, and overcome obstacles during your search for bugs.
### [[Writing a Good Report ]]
#writeup #writing #report-writing 
- A bug bounty hunter’s job isn’t just finding vulnerabilities; it’s also explaining them to the organization’s security team. If you provide a well-written report, you’ll help the team you’re working with reproduce the exploit, assign it to the appropriate internal engineering team, and fix the issue faster. The faster a vulnerability is fixed, the less likely malicious hackers are to exploit it.
#### Step 1: Craft a Descriptive Title
- The first part of a great vulnerability report is always a descriptive title. Aim for a title that sums up the issue in one sentence. Ideally, it should allow the security team to immediately get an idea of what the vulnerability is, where it occurred, and its potential severity. To do so, it should answer the following questions: What is the vulnerability you’ve found? Is it an instance of a well-known vulnerability type, such as IDOR or XSS? Where did you find it on the target application?
	- For example, instead of a report title like `“IDOR on a Critical Endpoint,”` use one like `“IDOR on https://example.com/change_password Leads to Account Takeover for All Users.”` 
- Your goal is to give the security engineer reading your report a good idea of the content you’ll discuss in the rest of it.
#### Step 2: Provide a Clear Summary
- Next, provide a report summary. This section includes all the relevant details you weren’t able to communicate in the title, like the HTTP request parameters used for the attack, how you found it, and so on. 
	- Here’s an example of an effective report summary: `The https://example.com/change_password endpoint takes two POST body parameters: user_id and new_password. A POST request to this endpoint would change the password of user user_id to new_password. This endpoint is not validating the user_id parameter, and as a result, any user can change anyone else’s password by manipulating the user_id parameter. `
- A good report summary is clear and concise. It contains all the information needed to understand a vulnerability, including what the bug is, where the bug is found, and what an attacker can do when it’s exploited.
#### Step 3: Include a Severity Assessment
- Your report should also include an honest assessment of the bug’s severity. In addition to working with you to fix vulnerabilities, security teams have other responsibilities to tend to. Including a severity assessment will help them prioritize which vulnerabilities to fix first, and ensure that they take care of critical vulnerabilities right away.
- You could use the following scale to communicate severity: 
	- Low severity The bug doesn’t have the potential to cause a lot of damage. For example, an open redirect that can be used only for phishing is a low-severity bug. 
	- Medium severity The bug impacts users or the organization in a moderate way, or is a high-severity issue that’s difficult for a malicious hacker to exploit. The security team should focus on high- and critical-severity bugs first. For example, a cross-site request forgery (CSRF) on a sensitive action such as password change is often considered a medium-severity issue. 
	- High severity The bug impacts a large number of users, and its consequences can be disastrous for these users. The security team should fix a high-security bug as soon as possible. For example, an open redirect that can be used to steal OAuth tokens is a high-severity bug. 
	- Critical severity The bug impacts a majority of the user base or endangers the organization’s core infrastructure. The security team should fix a critical-severity bug right away. For example, a SQL injection leading to remote code execution (RCE) on the production server will be considered a critical issue. 
- Study the Common Vulnerability Scoring System (CVSS) at https://www.first.org/cvss/ for a general idea of how critical each type of vulnerability is. The CVSS scale takes into account factors such as how a vulnerability impacts an organization, how hard the vulnerability is to exploit, and whether the vulnerability requires any special privileges or user interaction to exploit. Then, try to imagine what your client company cares about, and which vulnerabilities would present the biggest business impact. Customize your assessment to fit the client’s business priorities. 
	- For example, a dating site might find a bug that exposes a user’s birth date as inconsequential, since a user’s age is already public information on the site, while a job search site might find a similar bug significant, because an applicant’s age should be confidential in the job search process. On the other hand, leaks of users’ banking information are almost always considered a high-severity issue.
- You could list the severity in a single line, as follows: 
	- ***Severity of the issue: High***
#### Step 4: Give Clear Steps to Reproduce 
- Next, provide step-by-step instructions for reproducing the vulnerability. Include all relevant setup prerequisites and details you can think of. It’s best to assume the engineer on the other side has no knowledge of the vulnerability and doesn’t know how the application works.
- ***EXAMPLE IS FOUND ON P44/418***
	- For example, a merely okay report might include the following `steps to reproduce: 1. Log in to the site and visit https://example.com/change_password. 2. Click the Change Password button. 3. Intercept the request, and change the user_id parameter to another user’s ID.` Notice that these steps aren’t comprehensive or explicit. They don’t specify that you need two test accounts to test for the vulnerability. They also assume that you have enough knowledge about the application and the format of its requests to carry out each step without more instructions. 
	- Now, here is an example from a better report: `1. Make two accounts on example.com: account A and account B. 2. Log in to example.com as account A, and visit https://example.com/ change_password. 3. Fill in the desired new password in the New password field, located at the top left of the page. 4. Click the Change Password button located at the top right of the page. 5. Intercept the POST request to https://example.com/change_password and change the user_id POST parameter to the user ID of account B. 6. You can now log in to account B by using the new password you’ve chosen.`
- Although the security team will probably still understand the first report, the second report is a lot more specific. By providing many relevant details, you can avoid any misunderstanding and speed up the mitigation process.
#### Step 5: Provide a Proof of Concept
- For simple vulnerabilities, the steps you provide might be all that the security team needs to reproduce the issue. But for more complex vulnerabilities, it’s helpful to include a video, screenshots, or photos documenting your exploit, called a proof-of-concept (POC) file.
	- For example, for a CSRF vulnerability, you could include an HTML file with the CSRF payload embedded. This way, all the security team needs to do to reproduce the issue is to open the HTML file in their browser. 
	- For an XML external entity attack, include the crafted XML file that you used to execute the attack. And for vulnerabilities that require multiple complicated steps to reproduce, you could film a screen-capture video of you walking through the process. POC files like these save the security team time because they won’t have to prepare the attack payload themselves. You can also include any crafted URLs, scripts, or upload files you used to attack the application.
#### Step 6: Describe the Impact and Attack Scenarios
- To help the security team fully understand the potential impact of the vulnerability, you can also illustrate a plausible scenario in which the vulnerability could be exploited. Note that this section is not the same as the severity assessment I mentioned earlier. 
- The severity assessment describes the severity of the consequences of an attacker exploiting the vulnerability, whereas the attack scenario explains what those consequences would actually look like.
- Scenario explains what those consequences would actually look like. If hackers exploited this bug, could they take over user accounts? Or could they steal user information and cause large-scale data leaks? Put yourself in a malicious hacker’s shoes and try to escalate the impact of the vulnerability as much as possible. Give the client company a realistic sense of the worst-case scenario. This will help the company prioritize the fix internally and determine if any additional steps or internal investigations are necessary.
- `Using this vulnerability, all that an attacker needs in order to change a user’s password is their user_id. Since each user’s public profile page lists the account’s user_id, anyone can visit any user’s profile, find out their user_id, and change their password. And because user_ids are simply sequential numbers, a hacker can even enumerate all the user_ids and change the passwords of all users! This bug will let attackers take over anyone’s account with minimal effort`
- A good impact section illustrates how an attacker can realistically exploit a bug. It takes into account any mitigating factors as well as the maximum impact that can be achieved. It should never overstate a bug’s impact or include any hypotheticals.
#### Step 7: Recommend Possible Mitigations
- You can also recommend possible steps the security team can take to mitigate the vulnerability. This will save the team time when it begins researching mitigations. Often, since you’re the security researcher who discovered the vulnerability, you’ll be familiar with the particular behavior of that application feature, and thus in a good position to come up with a comprehensive fix.
- However, don’t propose fixes unless you have a good understanding of the root cause of the issue.
- You don’t have to go into the technical details of the fix, since you don’t have knowledge of the application’s underlying codebase. But as someone who understands the vulnerability class, you can provide a direction for mitigation. 
#### Step 8: Validate the Report
Finally, always validate your report. Go through your report one last time to make sure that there are no technical errors, or anything that might prevent the security team from understanding it. Follow your own Steps to Reproduce to ensure that they contain enough details. Examine all of your POC files and code to make sure they work. By validating your reports, you can minimize the possibility of submitting an invalid report.

#### Additional Tips for Writing Better Reports
##### Don’t Assume Anything
- First, don’t assume that the security team will be able to understand everything in your report. Remember that you might have been working with this vulnerability for a week, but to the security team receiving the report, it’s all new information. They have a whole host of other responsibilities on their plates and often aren’t as familiar with the feature as you. 
- Additionally, reports are not always assigned to security teams. Newer programs, open source projects, and startups may depend on developers or technical support personnel to handle bug reports instead of having a dedicated security team. Help them understand what you’ve discovered. 
- Be as verbose as possible, and include all the relevant details you can think of. It’s also good to include links to references explaining obscure security knowledge that the security team might not be familiar with.
- The worst thing that can happen if you’re too wordy is that your report will take two extra minutes to read. But if you leave out important details, the remediation of the vulnerability might get delayed, and a malicious hacker might exploit the bug.
##### Be Clear and Concise
- On the other hand, don’t include any unnecessary information, such as wordy greetings, jokes, or memes. A security report is a business document, not a letter to your friend. It should be straightforward and to the point. Make your report as short as possible without omitting the key details.
##### Write What You Want to Read
- Always put your reader in mind when writing, and try to build a good reading experience for them. Write in a conversational tone and don’t use leetspeak, slang, or abbreviations.
##### Be Professional
- Finally, always communicate with the security team with respect and professionalism. Provide clarifications regarding the report patiently and promptly. You’ll probably make mistakes when writing reports, and miscommunication will inevitably happen. But remember that as the security researcher, you have the power to minimize that possibility by putting time and care into your writing. By honing your reporting skills in addition to your hacking skills, you can save everyone’s time and maximize your value as a hacker.
### Building a Relationship with the Development Team
- Your job as a hacker doesn’t stop the moment you submit the report. As the person who discovered the vulnerability, you should help the company fix the issue and make sure the vulnerability is fully patched. 
- Building a strong relationship with the security team will help get your reports resolved more quickly and smoothly. It might even lead to bigger bug bounty payouts if you can consistently contribute to the security of the organization. Some bug bounty hunters have even gotten interviews or job offers from top tech firms because of their bug bounty findings!
#### Understanding Report States
- Once you’ve submitted your report, the security team will classify it into a report state, which describes the current status of your report. The report state will change as the process of mitigation moves forward. You can find the report state listed on the bug bounty platform’s interface, or in the messages you receive from security teams.
##### Need More Information 
- One of the most common report states you’ll see is need more information. This means the security team didn’t fully understand your report, or couldn’t reproduce the issue by using the information you’ve provided. 
- The security team will usually follow up with questions or requests for additional information about the vulnerability. In this case, you should revise your report, provide any missing information, and address the security team’s additional concerns. 
##### Informative 
- If the security team marks your report as informative, they won’t fix the bug. This means they believe the issue you reported is a security concern but not significant enough to warrant a fix. Vulnerabilities that do not impact other users, such as the ability to increase your own scores on an online game, often fall into this category. 
- Another type of bug often marked as informative is a missing security best practice, like allowing users to reuse passwords. 
- ***In this case, there’s nothing more you can do for the report!*** The company won’t pay you a bounty, and you don’t have to follow up, unless you believe the security team made a mistake. However, I do recommend that you keep track of informative issues and try to chain them into bigger, more impactful bugs.
##### Duplicate 
- A duplicate report status means another hacker has already found the bug, and the company is in the process of remediating the vulnerability. Unfortunately, since companies award bug bounties to only the first hacker who finds the bug, you won’t get paid for duplicates. 
- There’s nothing more to do with the report besides helping the company resolve the issue. You can also try to escalate or chain the bug into a more impactful bug. That way, the security team might see the new report as a separate issue and reward you.
##### N/A 
- A not applicable (N/A) status means your report doesn’t contain a valid security issue with security implications. This might happen when your report contains technical errors, or if the bug is intentional application behavior. N/A reports don’t pay. 
- There is nothing more for you to do here besides move on and continue hacking! 
##### Triaged 
- Security teams triage a report when they’ve validated the report on their end. This is great news for you, because this usually means the security team is going to fix the bug and reward you with a bounty. Once the report has been triaged, you should help the security team fix the issue. Follow up with their questions promptly, and provide any additional information they ask for.
##### Resolved 
- When your report is marked as resolved, the reported vulnerability has been fixed. At this point, pat yourself on the back and rejoice in the fact that you’ve made the internet a little safer. If you are participating in a paid bug bounty program, you can also expect to receive your payment at this point! There’s nothing more to do with the report besides celebrate and continue hacking.
#### Dealing with Conflict 
- Not all reports can be resolved quickly and smoothly. Conflicts inevitably happen when the hacker and the security team disagree on the validity of the bug, the severity of the bug, or the appropriate payout amount. Even so, conflicts could ruin your reputation as a hacker, so handling them professionally is key to a successful bug hunting career.
- When you disagree with the security team about the validity of the bug, first make sure that all the information in your initial report is correct. Often, security teams mark reports as informative or N/A because of a technical or writing mistake. For example, if you included incorrect URLs in your POC, the security team might not be able to reproduce the issue.
	- If this caused the disagreement, send over a follow-up report with the correct information as soon as possible.
- On the other hand, if you didn’t make a mistake in your report but still believe they’ve labeled the issue incorrectly, send a follow-up explaining why you believe that the bug is a security issue. If that still doesn’t resolve the misunderstanding, you can ask for mediation by the bug bounty platform or other security engineers on the team.
- Most of the time, it is difficult for others to see the impact of a vulnerability if it doesn’t belong to a well-known bug class. If the security team dismisses the severity of the reported issue, you should explain some potential attack scenarios to fully illustrate its impact. 
- Finally, if you’re unhappy with the bounty amount, communicate that without resentment. Ask for the organization’s reasoning behind assigning that bounty, and explain why you think you deserve a higher reward. For example, if the person in charge of your report underestimated the severity of the bug, you can elaborate on the impact of the issue when you ask for a higher reward. Whatever you do, always avoid asking for more money without explanation. 
- Remember, we all make mistakes. If you believe the person handling your report mishandled the issue, ask for reconsideration courteously. Once you’ve made your case, respect the company’s final decision about the fix and bounty amount.
#### Building a Partnership
- The bug bounty journey doesn’t stop after you’ve resolved a report. You should strive to form long-term partnerships with organizations. This can help get your reports resolved more smoothly and might even land you an interview or job offer. You can form good relationships with companies by respecting their time and communicating with professionalism.
- First, gain respect by always submitting validated reports. Don’t break a company’s trust by spamming, pestering them for money, or verbally abusing the security team.
- Also learn the communication style of each organization you work with. 
	- How much detail do they expect in their reports?
	- Do they expect lots of photos and videos to document the bug? 
	- Customize your reports to make your reader’s job easier.
- Finally, make sure you support the security team until they resolve the issue. Many organizations will pay you a bounty upon report triage, but please don’t bail on the security team after you receive the reward! 
- If it’s requested, provide advice to help mitigate the vulnerability, and help security teams confirm that the issue has been fixed. 
	- Sometimes organizations will ask you to perform retests for a fee. Always take that opportunity if you can. You’ll not only make money, but also help companies resolve the issue faster.
### Understanding Why You’re Failing
#### Why You’re Not Finding Bugs
- If you spend a lot of time in bug bounties and still have trouble finding bugs, here are some possible reasons.
##### You Participate in the Wrong Programs 
- You might have been targeting the wrong programs all along. Bug bounty programs aren’t created equally, and picking the right one is essential. Some programs delay fixing bugs because they lack the resources to deal with reports. 
- Some programs downplay the severity of vulnerabilities to avoid paying hackers. Finally, other programs restrict their scope to a small subset of their assets. They run bug bounty programs to gain positive publicity and don’t intend to actually fix vulnerabilities.
	- Avoid these programs to save yourself the headache.
- You can identify these programs by reading publicly disclosed reports, analyzing program statistics on bug bounty platforms, or by talking with other hackers. A program’s stats listed on bug bounty platforms provide a lot of information on how well a program is executed.
	- Avoid programs with long response times and programs with low average bounties.
##### You Don’t Stick to a Program 
- How long should you target a program? If your answer is a few hours or days, that’s the reason you’re not finding anything. Jumping from program to program is another mistake beginners often make. Every bug bounty program has countless bug bounty hunters hacking it. 
- Differentiate yourself from the competition, or risk not finding anything! 
	- You can differentiate yourself in two ways: 
		- dig deep or search wide. 
		- For example, dig deep into a single functionality of an application to search for complex bugs. Or discover and hack the lesser-known assets of the company. Doing these things well takes time. Don’t expect to find bugs right away when you’re starting fresh on a program. And don’t quit a program if you can’t find bugs on the first day.
##### You Don’t Recon 
- Jumping into big public programs without performing reconnaissance is another way to fail at bug bounties
##### You Go for Only Low-Hanging Fruit 
- Another mistake that beginners often make is to rely on vulnerability scanners. Companies routinely scan and audit their applications, and other bug bounty hunters often do the same, so this approach won’t give you good results.
- avoid looking for only the obvious bug types. Simplistic bugs on big targets have probably already been found. Many bug bounty programs were private before companies opened them to the public.
- This isn’t to say that you shouldn’t look for low-hanging fruit at all. Just don’t get discouraged if you don’t find anything that way. Instead, strive to gain a deeper understanding of the application’s underlying architecture and logic. From there, you can develop a unique testing methodology that will result in more unique and valuable bugs.
##### You Don’t Get into Private Programs 
- It becomes much easier to find bugs after you start hacking on private programs.
- Many successful hackers say that most of their findings come from private programs. Private programs are a lot less crowded than public ones, so you’ll have less competition, and less competition usually means more easy finds and fewer duplicates.
#### Why Your Reports Get Dismissed
##### You Don’t Read the Bounty Policy 
- One of the most common reasons reports get marked as N/A is that they’re out of scope.
- Respect these boundaries, and don’t submit bugs that are out of scope. If you do accidentally find a critical issue that is out of scope, report it if you think it’s something that the organization has to know about! You might not get rewarded, but you can still contribute to the company’s security.
##### You Don’t Put Yourself in the Organization’s Shoes 
- Informative reports are much harder to prevent than N/As. Most of the time, you’ll get informative ratings because the company doesn’t care about the issue you’re reporting.
- Imagine yourself as a security engineer. If you’re busy safeguarding millions of users’ data every day, would you care about an open redirect that can be used only for phishing? Although it’s a valid security flaw, you probably wouldn’t. You have other responsibilities to tend to, so fixing a low-severity bug is at the bottom of your to-do list. If the security team does not have the extra staff to deal with these reports, they will sometimes ignore it and mark it as informative. 
- I’ve found that the most helpful way to reduce informatives is to put myself in the organization’s shoes. Learn about the organization so you can identify its product, the data it’s protecting, and the parts of its application that are the most important. Once you know the business’s priorities, you can go after the vulnerabilities that the security team cares about.
- And remember, different companies have different priorities. An informative report to one organization could be a critical one to another. Like the dating site versus job search site example mentioned earlier in this chapter, everything is relative. Sometimes, it’s difficult to figure out how important a bug will be to an organization. Some issues I’ve reported as critical ended up being informative. And some vulnerabilities I classified as low impact were rewarded as critical issues. 
	- This is where trial and error can pay off. Every time the security team classifies your report as informative, take note for future reference. The next time you find a bug, ask yourself: did this company care about issues like this in the past? Learn what each company cares about, and tailor your hacking efforts to suit their business priorities. You’ll eventually develop an intuition about what kinds of bugs deliver the most impact.
##### You Don’t Chain Bugs 
- You might also be getting informatives because you always report the first minor bug you find. But minor bugs classified as informative can become big issues if you learn to chain them. When you find a low-severity bug that might get dismissed, don’t report it immediately. Try to use it in future bug chains instead. For example, instead of reporting an open redirect, use it in a server-side request forgery (SSRF) attack!
##### You Write Bad Reports 
- Another mistake beginners often make is that they fail to communicate the bug’s impact in their report. Even when a vulnerability is impactful, if you can’t communicate its implications to the security team, they’ll dismiss the report.
##### What About Duplicates? 
- Unfortunately, sometimes you can’t avoid duplicates. But you could lower your chances of getting duplicates by hunting on programs with large scopes, hacking on private programs, performing recon extensively, and developing your unique hunting methodology.
#### What To Do When You Are Stuck?
##### Step 1: Take a Break! 
- First, take a break. Hacking is hard work. Unlike what they show in the movies, hunting for vulnerabilities is tedious and difficult. It requires patience, persistence, and an eye for detail, so it can be very mentally draining. 
- Before you keep hacking away, ask yourself: am I tired? A lack of inspiration could be your brain’s way of telling you it has reached its limits. 
	- In this case, your best course of action would be to rest it out. Go outside. Meet up with friends. Have some ice cream. Or stay inside. Make some tea. And read a good book. There is more to life than SQL injections and XSS payloads. If you take a break from hacking, you’ll often find that you’re much more creative when you come back.
##### Step 2: Build Your Skill Set 
- Use your hacking slump as an opportunity to improve your skills. Hackers often get stuck because they get too comfortable with certain familiar techniques, and when those techniques don’t work anymore, they mistakenly assume there’s nothing left to try. Learning new skills will get you out of your comfort zone and strengthen your hacker skills for the future.
- ***Learn a new hacking technique***, whether it’s a new web exploitation technique, a new recon angle, or a different platform, such as Android. 
	- Focus on a specific skill you want to build, read about it, and apply it to the targets you’re hacking. Who knows? You might uncover a whole new way to approach the target application! You can also take this opportunity to catch up with what other hackers are doing by reading the many hacker blogs and write-up sites out there. Understanding other hackers’ approaches can provide you with a refreshing new perspective on engaging with your target. 
- ***Next, play Capture the Flags (CTFs).***
##### Step 3: Gain a Fresh Perspective 
- When you’re ready to hack live targets again, here are some tips to help you keep your momentum.
	- First, hacking on a single target can get boring, so diversify your targets instead of focusing on only one. I’ve always found it helpful to have a few targets to alternate between. When you’re getting tired of one application, switch to another, and come back to the first one later
	- Second, make sure you’re looking for specific things in a target instead of wandering aimlessly, searching for anything. Make a list of the new skills you’ve learned and try them out. Look for a new kind of bug, or try out a new recon angle. Then, rinse and repeat until you find a suitable new workflow.
	- Finally, remember that hacking is not always about finding a single vulnerability but combining several weaknesses of an application into something critical. In this case, it’s helpful to specifically look for weird behavior instead of vulnerabilities. Then take note of these weird behaviors and weaknesses, and see if you can chain them into something worth reporting.
#### Lastly, a Few Words of Experience 
- Bug bounty hunting is difficult. When I started hunting for bugs, I’d sometimes go months without finding one. And when I did find one, it’d be something trivial and low severity. The key to getting better at anything is practice. If you’re willing to put in the time and effort, your hacking skills will improve, and you’ll soon see yourself on leaderboards and private invite lists! If you get frustrated during this process, remember that everything gets easier over time. Reach out to the hacker community if you need help. And good luck!

# PART II: GETTING STARTED
## Chapter 3: HOW THE INTERNET WORKS
### The Client-Server Model 
- The internet is composed of two kind of devices: clients and servers. 
- Clients request resources or services, and servers provide those resources and services. When you visit a website with your browser, it acts as a client and requests a web page from a web server. The web server will then send your browser the web page
### The Domain Name System 
- How do your browser and other web clients know where to find these resources? Well, every device connected to the internet has a unique Internet Protocol (IP) address that other devices can use to find it. However, IP addresses are made up of numbers and letters that are hard for humans to remember. 
	- For example, the older format of IP addresses, IPv4, looks like this: 123.45.67.89. The new version, IPv6, looks even more complicated: 2001:db8::ff00:42:8329.
- This is where the Domain Name System (DNS) comes in. A DNS server functions as the phone book for the internet, translating domain names into IP addresses (Figure 3-2). When you enter a domain name in your browser, a DNS server must first convert the domain name into an IP address. Our browser asks the DNS server, “Which IP address is this domain located at?”
### Internet Ports 
- After your browser acquires the correct IP address, it will attempt to connect to that IP address via a port. A port is a logical division on devices that identifies a specific network service. We identify ports by their port numbers, which can range from 0 to 65,535. Ports allow a server to provide multiple services to the internet at the same time. Because conventions exist for the traffic received on certain ports, port numbers also allow the server to quickly forward arriving internet messages to a corresponding service for processing
	- For example, if an internet client connects to port 80, the web server understands that the client wishes to access its web services (Figure 3-3)
### HTTP Requests and Responses 
#HTTP #HTTP-REQUEST #HTTP-RESPONSE #HTTP-METHOD
- Once a connection is established, the browser and server communicate via the HyperText Transfer Protocol (HTTP). HTTP is a set of rules that specifies how to structure and interpret internet messages, and how web clients and web servers should exchange information. When your browser wants to interact with a server, it sends the server an HTTP request.

```
GET / HTTP/1.1
Host: www.google.com 
User-Agent: Mozilla/5.0 
Accept: text/html,application/xhtml+xml,application/xml 
Accept-Language: en-US 
Accept-Encoding: gzip, deflate 
Connection: close
```
- All HTTP requests are composed of a request line, request headers, and an optional request body. The preceding example contains only the request line and headers. 
- The request line is the first line of the HTTP request. It specifies the request method, the requested URL, and the version of HTTP used. Here, you can see that the client is sending an HTTP GET request to the home page of www.google.com using HTTP version 1.1. 
- The rest of the lines are HTTP request headers. These are used to pass additional information about the request to the server. This allows the server to customize results sent to the client. In the preceding example, the Host header specifies the hostname of the request. 
- The User-Agent header contains the operating system and software version of the requesting software, such as the user’s web browser. 
- The Accept, Accept-Language, and Accept-Encoding headers tell the server which format the responses should be in. And the Connection header tells the server whether the network connection should stay open after the server responds. 
- You might see a few other common headers in requests. 
	- The Cookie header is used to send cookies from the client to the server. The Referer header specifies the address of the previous web page that linked to the current page. And the Authorization header contains credentials to authenticate a user to a server.
- After the server receives the request, it will try to fulfill it. The server will return all the resources used to construct your web page by using HTTP responses. An HTTP response contains multiple things: an HTTP status code to indicate whether the request succeeded; HTTP headers, which are bits of information that browsers and servers use to communicate with each other about authentication, content format, and security policies; and the HTTP response body, or the actual web content that you requested. The web content could include HTML code, CSS style sheets, JavaScript code, images, and more.
- As a bug bounty hunter, you should always keep an eye on these status codes, because they can tell you a lot about how the server is operating. For example, a status code of 403 means that the resource is forbidden to you. This might mean that sensitive data is hidden on the page that you could reach if you can bypass the access controls.
- In addition to these, you might encounter a few other common response headers. The Set-Cookie header is sent by the server to the client to set a cookie. The Location header indicates the URL to which to redirect the page. The Access-Control-Allow-Origin header indicates which origins can access the page’s content. (We will talk about this more in Chapter 19.) Content-Security-Policy controls the origin of the resources the browser is allowed to load, while the X-Frame-Options header indicates whether the page can be loaded within an iframe (discussed further in Chapter 8).
Internet Security Controls Now that you have a high-level understanding of how information is communicated over the internet, let’s dive into some fundamental security controls that protect it from attackers. To hunt for bugs effectively, you will often need to come up with creative ways to bypass these controls, so you’ll first need to understand how they work.
### Internet Security Controls 
- Now that you have a high-level understanding of how information is communicated over the internet, let’s dive into some fundamental security controls that protect it from attackers. To hunt for bugs effectively, you will often need to come up with creative ways to bypass these controls, so you’ll first need to understand how they work.
#### Content Encoding 
- Data transferred in HTTP requests and responses isn’t always transmitted in the form of plain old text. Websites often encode their messages in different ways to prevent data corruption. Data encoding is used as a way to transfer binary data reliably across machines that have limited support for different content types. 
- Characters used for encoding are common characters not used as controlled characters in internet protocols. So when you encode content using common encoding schemes, you can be confident that your data is going to arrive at its destination uncorrupted. In contrast, when you transfer your data in its original state, the data might be screwed up when internet protocols misinterpret special characters in the message. 
- ***Base64 encoding is one of the most common ways of encoding data***. It’s often used to transport images and encrypted information within web messages.
- Base64 encoding’s character set includes the uppercase alphabet characters A to Z, the lowercase alphabet characters a to z, the number characters 0 to 9, the characters + and /, and finally, the = character for padding. Base64url encoding is a modified version of base64 used for the URL format. It’s similar to base64, but uses different non-alphanumeric characters and omits padding
- Another popular encoding method is hex encoding. Hexadecimal encoding, or hex, is a way of representing characters in a base-16 format, where characters range from 0 to F. Hex encoding takes up more space and is less efficient than base64 but provides for a more human-readable encoded string
- URL encoding is a way of converting characters into a format that is more easily transmitted over the internet. Each character in a URL-encoded string can be represented by its designated hex number preceded by a % symbol.
- You can use Burp Suite’s decoder to decode encoded content. We’ll cover how to do this in the next chapter. Alternatively, you can use CyberChef (https://gchq.github.io/CyberChef/) to decode both base64 content and other types of encoded content.
#### Session Management and HTTP Cookies 
- Why is it that you don’t have to re-log in every time you close your email tab? It’s because the website remembers your session. Session management is a process that allows the server to handle multiple requests from the same user without asking the user to log in again. Websites maintain a session for each logged-in user, and a new session starts when you log in to the website (Figure 3-4). The server will assign an associated session ID for your browser that serves as proof of your identity. The session ID is usually a long and unpredictable sequence designed to be unguessable. When you log out, the server ends the session and revokes the session ID. The website might also end sessions periodically if you don’t manually log out.
- Most websites use cookies to communicate session information in HTTP requests. HTTP cookies are small pieces of data that web servers send to your browser. When you log in to a site, the server creates a session for you and sends the session ID to your browser as a cookie. After receiving a cookie, your browser stores it and includes it in every request to the same server (Figure 3-5).
- That’s how the server knows it’s you! After the cookie for the session is generated, the server will track it and use it to validate your identity. Finally, when you log out, the server will invalidate the session cookie so that it cannot be used again. The next time you log in, the server will create a new session and a new associated session cookie for you.
#### Token-Based Authentication 
- In session-based authentication, the server stores your information and uses a corresponding session ID to validate your identity, whereas a token-based authentication system stores this info directly in some sort of token. Instead of storing your information server-side and querying it using a session ID, tokens allow servers to deduce your identity by decoding the token itself. This way, applications won’t have to store and maintain session information server-side.
- This system comes with a risk: if the server uses information contained in the token to determine the user’s identity, couldn’t users modify the information in the tokens and log in as someone else? To prevent token forgery attacks like these, some applications encrypt their tokens, or encode the token so that it can be read by only the application itself or other authorized parties. If the user can’t understand the contents of the token, they probably can’t tamper with it effectively either. Encrypting or encoding a token does not prevent token forgery completely.
- Another more reliable way applications protect the integrity of a token is by signing the token and verifying the token signature when it arrives at the server. Signatures are used to verify the integrity of a piece of data. They are special strings that can be generated only if you know a secret key. Since there is no way of generating a valid signature without the secret key, and only the server knows what the secret key is, a valid signature suggests that the token is probably not altered by the client or any third party.
- Although the implementations by applications can vary, token-based authentication works like this: 
	1. The user logs in with their credentials. 
	2. The server validates those credentials and provides the user with a signed token. How the Internet Works   
	3. The user sends the token with every request to prove their identity. 
	4. Upon receiving and validating the token, the server reads the user’s identity information from the token and responds with confidential data.
#### JSON Web Tokens 
- The JSON Web Token (JWT) is one of the most commonly used types of authentication tokens. It has three components: a header, a payload, and a signature. 
	- The header identifies the algorithm used to generate the signature. It’s a base64url-encoded string containing the algorithm name. Here’s what a JWT header looks like: `eyBhbGcgOiBIUzI1NiwgdHlwIDogSldUIH0K`. 
	- The payload section contains information about the user’s identity. This section, too, is base64url encoded before being used in the token.
	- Finally, the signature section validates that the user hasn’t tampered with the token. It’s calculated by concatenating the header with the payload, then signing it with the algorithm specified in the header, and a secret key.
	- The complete token concatenates each section (the header, payload, and signature), separating them with a period (.)

```
NOTE FROM EXTERNAL SOURCE(NOT THE BOOK)
Here's how the verification process works:

1. Token Reception: The server receives the JWT from the client, typically included in the `Authorization` header of an HTTP request.
    
2. Signature Verification: The server decodes the JWT to access its payload, which contains the claims and the signature. Then, it performs signature verification using the algorithm specified in the header of the JWT (e.g., HMAC, RSA). This verification process involves recalculating the signature using the received payload and the server's secret key. If the recalculated signature matches the signature included in the JWT, it indicates that the token hasn't been tampered with.
    
3. Validation: After verifying the signature, the server checks the claims within the token to ensure they meet its requirements. This could include checking the token's expiration time, ensuring it's issued by a trusted authority, or validating other custom claims relevant to the application's logic.
```
- When implemented correctly, JSON web tokens provide a secure way to identify the user.
- But if implemented incorrectly, there are ways that an attacker can bypass the security mechanism and forge arbitrary tokens.
##### Manipulating the alg Field
- One way that attackers can forge their own tokens is by tampering with the alg field of the token header, which lists the algorithm used to encode the signature. If the application does not restrict the algorithm type used in the JWT, an attacker can specify which algorithm to use, which could compromise the security of the token. JWT supports a none option for the algorithm type. If the alg field is set to none, even tokens with empty signature sections would be considered valid.
- Another way attackers can exploit the alg field is by changing the type of algorithm used. The two most common types of signing algorithms used for JWTs are HMAC and RSA. HMAC requires the token to be signed with a key and then later verified with the same key. When using RSA, the token would first be created with a private key, then verified with the corresponding public key, which anyone can read. It is critical that the secret key for HMAC tokens and the private key for RSA tokens be kept a secret.
- Now let’s say that an application was originally designed to use RSA tokens. The tokens are signed with a private key A, which is kept a secret from the public. Then the tokens are verified with public key B, which is available to anyone. This is okay as long as the tokens are always treated as RSA tokens. Now if the attacker changes the alg field to HMAC, they might be able to create valid tokens by signing the forged tokens with the RSA public key, B. When the signing algorithm is switched to HMAC, the token is still verified with the RSA public key B, but this time, the token can be signed with the same public key too.
##### Brute-Forcing the Key 
- It could also be possible to guess, or brute-force, the key used to sign a JWT. The attacker has a lot of information to start with: the algorithm used to sign the token, the payload that was signed, and the resulting signature. If the key used to sign the token is not complex enough, they might be able to brute-force it easily. If an attacker is not able to brute-force the key, they might try leaking the secret key instead. If another vulnerability, like a directory traversal, external entity attack (XXE), or SSRF exists that allows the attacker to read the file where the key value is stored, the attacker can steal the key and sign arbitrary tokens of their choosing.
##### Reading Sensitive Information 
- Since JSON web tokens are used for access control, they often contain information about the user. If the token is not encrypted, anyone can base64-decode the token and read the token’s payload. If the token contains sensitive information, it might become a source of information leaks. A properly implemented signature section of the JSON web token provides data integrity, not confidentiality. 
- These are just a few examples of JWT security issues. For more examples of JWT vulnerabilities, use the search term JWT security issues. The security of any authentication mechanism depends not only on its design, but also its implementation. JWTs can be secure, but only if implemented properly.
#### The Same-Origin Policy 
- The same-origin policy (SOP) is a rule that restricts how a script from one origin can interact with the resources of a different origin. In one sentence, the SOP is this: a script from page A can access data from page B only if the pages are of the same origin. This rule protects modern web applications and prevents many common web vulnerabilities.
- Two URLs are said to have the same origin if they share the same protocol, hostname, and port number. 
	- Let’s look at some examples. Page A is at this URL: https://medium.com/@vickieli
	- It uses HTTPS, which, remember, uses port 443 by default. Now look at the following pages to determine which has the same origin as page A, 
		- according to the SOP: 
		- https://medium.com/ 
		- http://medium.com/ 
		- https://twitter.com/@vickieli7 
		- https://medium.com:8080/@vickieli 
		- The https://medium.com/ URL is of the same origin as page A, because the two pages share the same origin, protocol, hostname, and port number. The other three pages do not share the same origin as page A.
- Now let’s consider an example to see how SOP protects us. 
	- Imagine that you’re logged in to your banking site at onlinebank.com. Unfortunately, you click on a malicious site, attacker.com, in the same browser. The malicious site issues a GET request to onlinebank.com to retrieve your personal information. Since you’re logged into the bank, your browser automatically includes your cookies in every request you send to onlinebank.com, even if the request is generated by a script on a malicious site. Since the request contains a valid session ID, the server of onlinebank .com fulfills the request by sending the HTML page containing your info. The malicious script then reads and retrieves the private email addresses, home addresses, and banking information contained on the page. 
	- Luckily, the SOP will prevent the malicious script hosted on attacker.com from reading the HTML data returned from onlinebank.com. This keeps the malicious script on page A from obtaining sensitive information embedded within page B.
### Learn to Program 
- You should now have a solid background to help you understand most of the vulnerabilities we will cover. Before you set up your hacking tools, I recommend that you learn to program. Programming skills are helpful, because hunting for bugs involves many repetitive tasks, and by learning a programming language such as Python or shell scripting, you can automate these tasks to save yourself a lot of time. 
- You should also learn to read JavaScript, the language with which most sites are written. Reading the JavaScript of a site can teach you about how it works, giving you a fast track to finding bugs. Many top hackers say that their secret sauce is that they read JavaScript and search for hidden endpoints, insecure programming logic, and secret keys. I’ve also found many vulnerabilities by reading JavaScript source code. 
- Codecademy is a good resource for learning how to program. If you prefer to read a book instead, Learn Python the Hard Way by Zed Shaw (Addison-Wesley Professional, 2013) is a great way to learn Python. And reading Eloquent JavaScript, Third Edition, by Marijn Haverbeke (No Starch Press, 2019) is one of the best ways to master JavaScript.

## Chapter 4: ENVIRONMENTAL SETUP AND TRAFFIC INTERCEPTION
## Chapter 5: Web Hacking Reconnaissance
#recon
- If an application doesn’t use PHP, for instance, there’s no reason to test it for PHP vulnerabilities, and if the organization doesn’t use Amazon Web Services (AWS), you shouldn’t waste time trying to crack its buckets. By understanding how a target works, you can set up a solid foundation for finding vulnerabilities. Recon skills are what separate a good hacker from an ineffective one.
### Manually Walking Through the Target
- Before we dive into anything else, it will help to first manually walk through the application to learn more about it. Try to uncover every feature in the application that users can access by browsing through every page and clicking every link. Access the functionalities that you don’t usually use.
- This should give you a rough idea of what the attack surface (all of the different points at which an attacker can attempt to exploit the application) looks like, where the data entry points are, and how different users interact with each other. Then you can start a more in-depth recon process: finding out the technology and structure of an application.
### Google Dorking
- When hunting for bugs, you’ll often need to research the details of a vulnerability. If you’re exploiting a potential cross-site scripting (XSS) vulnerability, you might want to find a particular payload you saw on GitHub. Advanced search-engine skills will help you find the resources you need quickly and accurately.

- In fact, advanced Google searches are a powerful technique that hackers often use to perform recon. Hackers call this Google dorking. For the average Joe, Google is just a text search tool for finding images, videos, and web pages. But for the hacker, Google can be a means of discovering valuable information such as hidden admin portals, unlocked password files, and leaked authentication keys.

- Google’s search engine has its own built-in query language that helps you filter your searches. Here are some of the most useful operators that can be used with any Google search:
#### site 
- Tells Google to show you results from a certain site only. This will help you quickly find the most reputable source on the topic that you are researching. For example, if you wanted to search for the syntax of Python’s print() function, you could limit your results to the official Python documentation with this search: print site:python.org.
#### inurl 
- Searches for pages with a URL that match the search string. It’s a powerful way to search for vulnerable pages on a particular website. Let’s say you’ve read a blog post about how the existence of a page called /course/jumpto.php on a website could indicate that it’s vulnerable to remote code execution. You can check if the vulnerability exists on your target by searching inurl:"/course/jumpto.php" site:example.com.
#### intitle 
- Finds specific strings in a page’s title. This is useful because it allows you to find pages that contain a particular type of content. For example, file-listing pages on web servers often have index of in their titles. You can use this query to search for directory pages on a website: intitle:"index of" site:example.com.
#### link 
- Searches for web pages that contain links to a specified URL. You can use this to find documentation about obscure technologies or vulnerabilities. For example, let’s say you’re researching the uncommon regular expression denial-of-service (ReDoS) vulnerability. You’ll easily pull up its definition online but might have a hard time finding examples. The link operator can discover pages that reference the vulnerability’s Wikipedia page to locate discussions of the same topic: link:"https:// en.wikipedia.org/wiki/ReDoS".
#### filetype 
- Searches for pages with a specific file extension. This is an incredible tool for hacking; hackers often use it to locate files on their target sites that might be sensitive, such as log and password files. For example, this query searches for log files, which often have the .log file extension, on the target site: filetype:log site:example.com.
#### Wildcard (`*`) 
- You can use the wildcard operator (`*`) within searches to mean any character or series of characters. For example, the following query will return any string that starts with how to hack and ends with using Google. It will match with strings like how to hack websites using Google, how to hack applications using Google, and so on: "how to hack `*` using Google".
#### Quotes (" ") 
- Adding quotation marks around your search terms forces an exact match. For example, this query will search for pages that contain the phrase how to hack: "how to hack". And this query will search for pages with the terms how, to, and hack, although not necessarily together: how to hack.
#### Or (|) 
- The or operator is denoted with the pipe character (|) and can be used to search for one search term or the other, or both at the same time. The pipe character must be surrounded by spaces. 
	- For example, this query will search for how to hack on either Reddit or Stack Overflow: "how to hack" site:(reddit.com | stackoverflow.com).
#### Minus (-) 
- The minus operator (-) excludes certain search results. For example, let’s say you’re interested in learning about websites that discuss hacking, but not those that discuss hacking PHP. This query will search for pages that contain how to hack websites but not php: "how to hack websites" -php.
---
#### others(title by me)
- You can use advanced search engine options in many more ways to make your work more efficient. You can even search for the term Google search operators to discover more. These operators can be more useful than you’d expect. For example, look for all of a company’s subdomains by searching as follows: `site:*.example.com`
- You can also look for special endpoints that can lead to vulnerabilities. Kibana is a data visualization tool that displays server operation data such as server logs, debug messages, and server status. 
	- A compromised Kibana instance can allow attackers to collect extensive information about a site’s operation. Many Kibana dashboards run under the path app/kibana, so this query will reveal whether the target has a Kibana dashboard. You can then try to access the dashboard to see if it’s unprotected:
	- `site:example.com inurl:app/kibana`
- Look for special extensions that could indicate a sensitive file. In addition to .log, which often indicates log files, search for .php, cfm, asp, .jsp, and .pl, the extensions often used for script files:
```
site:example.com ext:php
site:example.com ext:log
```
- Finally, you can also combine search terms for a more accurate search. For example, this query searches the site example.com for text files that contain password:
	- `site:example.com ext:txt password`
- In addition to constructing your own queries, check out the Google Hacking Database (https://www.exploit-db.com/google-hacking-database/), a website that hackers and security practitioners use to share Google search queries for finding security-related information. It contains many search queries that could be helpful to you during the recon process #LINK 
- While you are performing recon using Google search, keep in mind that if you’re sending a lot of search queries, Google will start requiring CAPTCHA challenges for visitors from your network before they can perform more searches. This could be annoying to others on your network, so I don’t recommend Google dorking on a corporate or shared network.
### Scope discovery
- First, always verify the target’s scope. A program’s scope on its policy page specifies which subdomains, products, and applications you’re allowed to attack. Carefully verify which of the company’s assets are in scope to avoid overstepping boundaries during the recon and hacking process.
#### WHOIS and REVERSE WHOIS
- When companies or individuals register a domain name, they need to supply identifying information, such as their mailing address, phone number, and email address, to a domain registrar. Anyone can then query this information by using the whois command, which searches for the registrant and owner information of each known domain. 
- You might be able to find the associated contact information, such as an email, name, address, or phone number
- This information is not always available, as some organizations and individuals use a service called domain privacy, in which a third-party service provider replaces the user’s information with that of a forwarding service.
- You could then conduct a reverse WHOIS search, searching a database by using an organization name, a phone number, or an email address to find domains registered with it. This way, you can find all the domains that belong to the same owner. Reverse WHOIS is extremely useful for finding obscure or internal domains not otherwise disclosed to the public.
- Use a public reverse WHOIS tool like ViewDNS.info (https://viewdns.info/reversewhois/) to conduct this search. WHOIS and reverse WHOIS will give you a good set of top-level domains to work with. #LINK
#### IP Addresses
- IP Addresses Another way of discovering your target’s top-level domains is to locate IP addresses. Find the IP address of a domain you know by running the nslookup command.
- Once you’ve found the IP address of the known domain, perform a reverse IP lookup. Reverse IP searches look for domains hosted on the same server, given an IP or domain. 
- You can also use ViewDNS.info for this. Also run the whois command on an IP address, and then see if the target has a dedicated IP range by checking the NetRange field. An IP range is a block of IP addresses that all belong to the same organization.
- Another way of finding IP addresses in scope is by looking at autonomous systems, which are routable networks within the public internet. Autonomous system numbers (ASNs) identify the owners of these networks. By checking if two IP addresses share an ASN, you can determine whether the IPs belong to the same owner. 
- To figure out if a company owns a dedicated IP range, run several IP-toASN translations to see if the IP addresses map to a single ASN. If many addresses within a range belong to the same ASN, the organization might have a dedicated IP range
#### Certificate Parsing 
- Another way of finding hosts is to take advantage of the Secure Sockets Layer (SSL) certificates used to encrypt web traffic. An SSL certificate’s Subject Alternative Name field lets certificate owners specify additional hostnames that use the same certificate, so you can find those hostnames by parsing this field. Use online databases like crt.sh, Censys, and Cert Spotter to find certificates for a domain. #TOOLS #recon #LINK 
- The crt.sh website also has a useful utility that lets you retrieve the information in JSON format, rather than HTML, for easier parsing. Just add the URL parameter output=json to the request URL: https://crt.sh/ ?q=facebook.com&output=json. #LINK 
#### Subdomain Enumeration 
- After finding as many domains on the target as possible, locate as many subdomains on those domains as you can. Each subdomain represents a new angle for attacking the network. The best way to enumerate subdomains is to use automation. 
- Tools like Sublist3r, SubBrute, Amass, and Gobuster can enumerate subdomains automatically with a variety of wordlists and strategies. 
	- For example, Sublist3r works by querying search engines and online subdomain databases, while SubBrute is a brute-forcing tool that guesses possible subdomains until it finds real ones. Amass uses a combination of DNS zone transfers, certificate parsing, search engines, and subdomain databases to find subdomains. #TOOLS #recon 
- To use many subdomain enumeration tools, you need to feed the program a wordlist of terms likely to appear in subdomains. You can find some good wordlists made by other hackers online. 
	- Daniel Miessler’s SecLists at https://github.com/danielmiessler/SecLists/ is a pretty extensive one. 
	- You can also use a wordlist generation tool like Commonspeak2 (https://github.com/ assetnote/commonspeak2/) to generate wordlists based on the most current internet data
- Finally, you can combine several wordlists found online or that you generated yourself for the most comprehensive results. Here’s a simple command to remove duplicate items from a set of two wordlists.
	- `sort -u wordlist1.txt wordlist2.txt`
		- The sort command line tool sorts the lines of text files. When given multiple files, it will sort all files and write the output to the terminal. The -u option tells sort to return only unique items in the sorted list.
	- `gobuster dns -d target_domain -w wordlist` `for detail P95/418`
	- Once you’ve found a good number of subdomains, you can discover more by identifying patterns. 
		- For example, if you find two subdomains of example .com named 1.example.com and 3.example.com, you can guess that 2.example.com is probably also a valid subdomain. 
		- A good tool for automating this process is Altdns (https://github.com/infosec-au/altdns/), which discovers subdomains with names that are permutations of other subdomain names. #TOOLS #recon
- In addition, you can find more subdomains based on your knowledge about the company’s technology stack. 
	- For example, if you’ve already learned that example.com uses Jenkins, you can check if jenkins.example.com is a valid subdomain. 
- Also look for subdomains of subdomains. After you’ve found, say, dev.example .com, you might find subdomains like 1.dev.example.com. You can find subdomains of subdomains by running enumeration tools recursively: add the results of your first run to your Known Domains list and run the tool again.
#### Service Enumeration 
- Next, enumerate the services hosted on the machines you’ve found. Since services often run on default ports, a good way to find them is by port-scanning the machine with either active or passive scanning.
- In active scanning, you directly engage with the server. Active scanning tools send requests to connect to the target machine’s ports to look for open ones. You can use tools like Nmap or Masscan for active scanning. #TOOLS #recon 
- On the other hand, in passive scanning, you use third-party resources to learn about a machine’s ports without interacting with the server. Passive scanning is stealthier and helps attackers avoid detection. 
	- To find services on a machine without actively scanning it, you can use Shodan, a search engine that lets the user find machines connected to the internet. #TOOLS #recon 
	- Alternatives to Shodan include Censys and Project Sonar. Combine the information you gather from different databases for the best results. With these databases, you might also find your target’s IP addresses, certificates, and software versions.
#### Directory Brute-Forcing 
- The next thing you can do to discover more of the site’s attack surface is brute-force the directories of the web servers you’ve found. Finding directories on servers is valuable, because through them, you might discover hidden admin panels, configuration files, password files, outdated functionalities, database copies, and source code files. Directory brute-forcing can sometimes allow you to directly take over a server! 
- Even if you can’t find any immediate exploits, directory information often tells you about the structure and technology of an application. For example, a pathname that includes phpmyadmin usually means that the application is built with PHP.
- You can use Dirsearch or Gobuster for directory brute-forcing. These tools use wordlists to construct URLs, and then request these URLs from a web server. #TOOLS #recon 
- Manually visiting all the pages you’ve found through brute-forcing can be time-consuming. 
	- Instead, use a screenshot tool like EyeWitness (https://github .com/FortyNorthSecurity/EyeWitness/) or Snapper (https://github.com/dxa4481/ Snapper/) to automatically verify that a page is hosted on each location. EyeWitness accepts a list of URLs and takes screenshots of each page. #TOOLS #recon 
- Keep an eye out for hidden services, such as developer or admin panels, directory listing pages, analytics pages, and pages that look outdated and illmaintained. These are all common places for vulnerabilities to manifest.
#### Spidering the Site 
- Another way of discovering directories and paths is through web spidering, or web crawling, a process used to identify all pages on a site. A web spider tool starts with a page to visit. It then identifies all the URLs embedded on the page and visits them. By recursively visiting all URLs found on all pages of a site, the web spider can uncover many hidden endpoints in an application. 
	- OWASP Zed Attack Proxy (ZAP) at https://www.zaproxy.org/ has a built-in web spider you can use (Figure 5-2). This open source security tool includes a scanner, proxy, and many other features. Burp Suite has an equivalent tool called the crawler, but I prefer ZAP’s spider. #TOOLS #recon 
	- `for details and steps to do it, check P98/412`
- 
# P95/418
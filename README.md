# transcription


1. Introduction 

Hello everyone! My name is Antonina. I'm a student of the RS School's Front-end / JS course. And this presentation is made as a part of the course. The topic of my presentation is OWASP Top 10 Security Risks

2. Importance of websites
First of all, I would like to notice that the importance of the Internet in modern life is absolutely undeniable. 5.3 billion people out of total number of 8.1 billion people in the world are active Internet users today.  
And almost all aspects of our lives are covered by the Internet. 

Based on the statistic today there are 1.09 billion websites in the World. And every second 3 new websites are created. 

Everyday billions of us use these websites and web-applications to search for information, connect with our friends, family and colleagues, buy and sell products and services, etc. 

And using these web-applications we leave so called digital footprints such as our personal data, bank accounts information, our home addresses, phone numbers and other important information. And this leads to certain security risks when our information gets into the hands of scammers.

That is why security is taken very seriously in web development. The Open Worldwide Application Security Project (OWASP) plays crucial role in making the Internet more secure place. 

2. OWASP as an organisation

OWASP is a nonprofit international foundation that was launched in 2001. Its main goal is improvement of the software's security. The materials they offer include documentation, tools, videos, and forums. And their best-known project is the OWASP Top 10.

3. OWASP Top 10

The OWASP Top 10 is a regularly-updated report outlining concerns for web application security, focusing on the 10 most critical risks. The report is made by a team of security experts from all over the world. OWASP refers to the Top 10 as an ‘awareness document’ and they recommend that all companies incorporate the report into their processes in order to minimize and/or mitigate security risks. 

Their last report was published in 2021. The previous one was published in 2017 and the next one is planned to be published at the end of 2024.

In this slide we can see the list of categories that were included in 2021 report and the comparison with 2017 report.

As we limited in time let's discuss three categories out of 10:

1. Insecure Design

Let's start from the very new category for 2021 report which is called Insecure design. It's important to note that insecure design and insecure implementation are not the same. An insecure design cannot be fixed by a perfect implementation. 

The main idea of this category is that all software developer have a responsibility to write secure applications that do not put its users at risks. That's why it's very important to keep security in mind from the very beginning of the development process. Otherwise the users' data will be at risks and the app will require updates and fixes to prevent these risks. And eventually it leads to unpredictable large monetary and reputational losses for the business. 

###### Examples of Insecure Design

1. A credential recovery workflow might include “questions and answers”.  Questions and answers cannot be trusted as evidence of identity as more than one person can know the answers, which is why they are prohibited. Such code should be removed and replaced with a more secure design.
2. Most CMS platforms, including WordPress, do not limit the number of failed logins on the administrator panel. This renders them particularly vulnerable to [brute force attacks](https://en.wikipedia.org/wiki/Brute-force_attack) and requires the installation of third-party security extensions to mitigate.
###### How to prevent

The report provides us with list of prescriptions that might help the developer to prevent the insecure design risks. There are some of them:

- Establish and use a secure development lifecycle with AppSec professionals to help evaluate and design security and privacy-related controls
- Use threat modeling for critical authentication, access control, business logic, and key flows
- Write unit and integration tests to validate that all critical flows are resistant to the threat model. Compile use-cases _and_ misuse-cases for each tier of your application
- etc

2. Vulnerable and outdated components

Today all of the web-sites even the simplest one have a lot of dependencies, plugins, extensions and third party code. Failing to update every piece of software on the backend and frontend of a website will introduce heavy security risks. Attackers actively seek out websites using vulnerable components and aggressively exploit them to spread malware, spam and phishing. 

Components typically run with the same privileges as the application itself, so flaws in any component can result in serious impact. 

There are automated tools to help attackers find unpatched or misconfigured systems. For example, the Shodan IoT search engine can help you find devices that still suffer from vulnerability patched in April 2014.

###### How to prevent

There should be a patch management process in place to:

- Remove unused dependencies, unnecessary features, components, files, and documentation.
- Only obtain components from official sources over secure links.
- Monitor for libraries and components that are unmaintained or do not create security patches for older versions. If patching is not possible, consider deploying a virtual patch to monitor, detect, or protect against the discovered issue.
- etc

3. Injection 

A code injection happens when an attacker sends invalid data to the web application with the intention of making it do something that the application is not designed/programmed to do.

Access control enforces policy such that users cannot act outside of their intended permissions. Failures typically lead to unauthorized information disclosure, modification, or destruction of all data or performing a business function outside the user's limits. Common access control vulnerabilities include:

- Violation of the principle of least privilege or deny by default, where access should only be granted for particular capabilities, roles, or users, but is available to anyone.
- Permitting viewing or editing someone else's account, by providing its unique identifier (insecure direct object references).
- Accessing API with missing access controls for POST, PUT and DELETE.
- and others.

You can see some examples of attack scenarios on the screen. 

###### How to prevent

Access control is only effective in trusted server-side code or server-less API, where the attacker cannot modify the access control check or metadata.

- Implement access control mechanisms once and re-use them throughout the application, including minimizing Cross-Origin Resource Sharing (CORS) usage.
- Disable web server directory listing and ensure file metadata (e.g., .git) and backup files are not present within web roots.
- Log access control failures, alert admins when appropriate (e.g., repeated failures).
- and others.

You can find other secure risks on the OWASP web-site.


So, I think that it's clear that today's internet is pretty insecure place. And all the organisations and self-employed developers must take all the risk in account very seriously. 



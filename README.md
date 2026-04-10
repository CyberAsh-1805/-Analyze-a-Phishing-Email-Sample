# -Analyze-a-Phishing-Email-Sample
1. Executive Summary:-
   
I have analyzed a suspicious email claiming to be from "OneCasino" regarding a "Welcome gift" of 50 spins. Based on header analysis and external threat intelligence (VirusTotal), I have classified this email as a Phishing Attack. The sender infrastructure and embedded links show clear malicious intent.
2. Sender Information & Header Analysis:- 

• Display Name: OneCasino

• Actual Sender Address: 132784@534617.vav.proo55.us.com

• Source IP Address: 141.95.0.46

• Geographic Origin: France (EU), registered under the domain ovh.net.

Technical Findings (IP Reputation):-

I performed a reputation check on the source IP (141.95.0.46) using VirusTotal. The results confirm the infrastructure is compromised or being used for attacks:

• One security vendor explicitly flagged the IP for Phishing.

• Two security vendors flagged the IP as Malicious.

3. Link & Social Engineering Analysis:- 
The email uses a financial incentive (free spins) to create interest. The technical analysis of the embedded call-to-action link reveals significant risks:

• Original Link: https://tinyurl.com/mrymsuhv (Shortened to hide the destination).

• VirusTotal Result (Short Link): Two security vendors flagged this as a Phishing link.

• Unshortened Destination: https://tinyurl.com/app/nospam/tinyurl.com/mrymsuhv (Note: This appears to be a nested redirect attempt).

• VirusTotal Result (Destination): One security vendor flagged the final destination as Phishing.

4. Phishing Indicators Found:- 
Based on my investigation, the following red flags were identified:

1. Spoofed Identity: The sender's email domain does not match the official "OneCasino" brand.
2. Suspicious Infrastructure: The mail was sent from a generic VPS in France rather than a corporate mail server.
3. URL Masking: Use of a shortened TinyURL to hide a destination that is flagged by multiple security engines.
4. Inconsistent Authentication: While the email passed basic SPF checks, the lack of a DMARC record and the mismatched "From" address indicate a "Pass" on a fraudulent domain.
5. Conclusion:- 
The combination of malicious IP reputation, flagged URLs, and impersonation tactics confirms this is a phishing attempt. I recommend that such emails be blocked at the gateway and the associated IP/URL be added to the organization's blocklist.

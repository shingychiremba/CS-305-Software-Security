# CS-305-Software-Security

Journal – Portfolio Submission

Artemis Financial is a financial consulting company that develops individualized financial plans for savings, retirement, investments, and insurance for their patrons. The goal is to modernize its operations and, as a crucial part of the success of its custom software, they want to implement and apply the most current and effective software security. Artemis Financial has a RESTful web application programming interface (API) and is seeking expertise in taking steps to protect the organization from external threats. 

Secure coding helps us to protect against hostile, misbehaving, or unsafe code. According to an online article by Oracle, “following secure coding best practices is still necessary to avoid bugs that could weaken security and even inadvertently open the very holes that Java's security features were intended to protect against” (2012). These bugs, if left unchecked can be the root cause of data breaches, information leaks, and injection attacks. Sticking to recommended coding guidelines is a good way for programmers to avoid errors that could be catastrophic.

The biggest challenge with the vulnerability assessment check was insertion of the correct dependencies in the correct format. Any of the slightest mistakes caused the code not to build in the pom.xml file. This was indeed vey frustrating. After researching, I managed to tackle the problem by inserting each new dependency within the configurations section of each maven check. The same had to be done with the suppression.xml file as well. Suppression code was meant to be added to the configurations section of the maven check. Lastly the versions of maven changed 3 times during this course from 4.2.0 to 5.3.0 to the most recent one used 7.0.4. This posed challenges when trying to use the same code for different assignments. Its an easy fix but at first glance that is the last thing one would think of.

The need to increase layers of security is brought about by the need to prevent system breaches by hackers. During this course, we approached the need for adding layers of security by using algorithm ciphers to create a checksum verification. This produced a hash value that was used to secure communications between a business and its clients. An example of a checksum below: 
	  @RequestMapping("/hash")
   public String bytesToHex(byte[] sha256){
           BigInteger hex = new BigInteger(1, sha256);
           StringBuilder checksum = new StringBuilder(hex.toString(16));
          if (checksum.length() < 32){
               checksum.insert(0, '0');
               return checksum.toString();
     
To ensure that the code was secure and functional, manually reviewing code for syntactical, logical, and security vulnerabilities was the best way to check the code. After refactoring the code, several new vulnerabilities were discovered. I had to work on the design and kept retesting until no new vulnerabilities were found.
  
The resources used include:
-	Manico, J., & Detlefsen, A. (2014, September). Iron-clad Java. O'Reilly Online Learning. Retrieved April 2, 2022, from https://learning.oreilly.com/library/view/iron-clad-java/9780071835886/ch06.html
-	Walker, J., Kounavis, M., Gueron, S., & Graunke, G. (2009). Recent Contributions to Cryptographic Hash Functions. Intel Technology Journal, 13(2), 80–95.
-	OWASP SCP quick reference guide V1. (n.d.). Retrieved April 19, 2022, from https://owasp.org/www-pdf-archive/OWASP_SCP_Quick_Reference_Guide_v1.pdf 
Some of the tools used: 
-	Eclipse IDE (Java)
-	Maven Dependency Check Tool
-	Vulnerability Assessment Process Flow Diagram (VAPFD)
-	Java Keytool
The coding practices used through this course include documentation. Theres was a lot of documentation on security information – practices, suggestions, revisions, implementations, and so on. We avoided duplicating the code to minimize errors. We established trust boundaries by creating a secure server connection with tomcat server. The most helpful asset for future assignments is the maven dependency check and the suppression of false positives to avoid unnecessary alarms.

This assignment had its challenges but the one thing I would like to showcase is  the completed Artemis Financial Vulnerability Assessment Report. The document was well researched and reported as accurately as possible giving a clear analysis of the threats at hand and how to mitigate them. 

References
Oracle. (2012). Secure Coding Guidelines for Java SE. Secure coding guidelines for java SE. 
	https://www.oracle.com/java/technologies/javase/seccodeguide.html 

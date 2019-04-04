# Spring Security Core.
**in web.xml**

<filter>
  <filter-name>springSecurityFilterChain</filter-name>
  <filter-class>org.springframework.web.filter.DeligatFilterProxy</filter-class>
</filter>  

<filter-mapping>
  <filter-name>springSecurityFilterChain </filter-name>
    <url-mapping> /*</url-mapping>
</filter-mapping>

**in spring-security.xml**


we have to configure Authentication Manager, Security context(contains user information)







# SpringSecurity

5.2.1  SecurityContextHolder, SecurityContext and Authentication Objects
The most fundamental object is SecurityContextHolder. This is where we store details of the present security context of the application, which includes details of the principal currently using the application. By default the SecurityContextHolder uses a ThreadLocal to store these details, which means that the security context is always available to methods in the same thread of execution, even if the security context is not explicitly passed around as an argument to those methods. Using a ThreadLocal in this way is quite safe if care is taken to clear the thread after the present principal's request is processed. Of course, Spring Security takes care of this for you automatically so there is no need to worry about it.

Some applications aren't entirely suitable for using a ThreadLocal, because of the specific way they work with threads. For example, a Swing client might want all threads in a Java Virtual Machine to use the same security context. SecurityContextHolder can be configured with a strategy on startup to specify how you would like the context to be stored. For a standalone application you would use the SecurityContextHolder.MODE_GLOBAL strategy. Other applications might want to have threads spawned by the secure thread also assume the same security identity. This is achieved by using SecurityContextHolder.MODE_INHERITABLETHREADLOCAL. You can change the mode from the default SecurityContextHolder.MODE_THREADLOCAL in two ways. The first is to set a system property, the second is to call a static method on SecurityContextHolder. Most applications won't need to change from the default, but if you do, take a look at the JavaDocs for SecurityContextHolder to learn more.

https://docs.spring.io/spring-security/site/docs/3.0.x/reference/technical-overview.html


JWT Introduction - https://www.youtube.com/watch?v=oXxbB5kv9OA

https://www.techrepublic.com/article/understanding-and-selecting-authentication-methods/

https://www.incapsula.com/web-application-security/csrf-cross-site-request-forgery.html

https://www.hacker101.com/sessions/introduction

# JSESSIONID

https://javarevisited.blogspot.com/2012/08/what-is-jsessionid-in-j2ee-web.html

# CSFR 

https://docs.spring.io/spring-security/site/docs/3.2.5.RELEASE/reference/htmlsingle/#csrf-attacks

https://stackoverflow.com/questions/16322067/csrf-generate-token-for-every-request/16360119#16360119


https://medium.com/@gtommee97/rest-authentication-with-spring-security-and-mongodb-28c06da25fb1

# HTTP/2 

http://qnimate.com/what-is-multiplexing-in-http2/


# sealyr-security

https://spring.io/projects/spring-security

Spring security 是一个强大的和高度可定制的身份验证和访问控制框架。这里有一份中文文档可以参考：https://springcloud.cc/spring-security-zhcn.html

Spring Security 提供强大的安全验证支持：

- HTTP BASIC authentication headers (an IETF RFC-based standard)
- HTTP Digest authentication headers (an IETF RFC-based standard)
- HTTP X.509 client certificate exchange (an IETF RFC-based standard)
- LDAP (a very common approach to cross-platform authentication needs, especially in large environments)
- Form-based authentication (for simple user interface needs)
- OpenID authentication
- Authentication based on pre-established request headers (such as Computer Associates Siteminder)
- Jasig Central Authentication Service (otherwise known as CAS, which is a popular open source single sign-on system)
- Transparent authentication context propagation for Remote Method Invocation (RMI) and HttpInvoker (a Spring remoting protocol)
- Automatic "remember-me" authentication (so you can tick a box to avoid re-authentication for a predetermined period of time)
- Anonymous authentication (allowing every unauthenticated call to automatically assume a particular security identity)
- Run-as authentication (which is useful if one call should proceed with a different security identity)
- Java Authentication and Authorization Service (JAAS)
- Java EE container authentication (so you can still use Container Managed Authentication if desired)
- Kerberos
- Java Open Source Single Sign-On (JOSSO) *
- OpenNMS Network Management Platform *
- AppFuse *
- AndroMDA *
- Mule ESB *
- Direct Web Request (DWR) *
- Grails *
- Tapestry *
- JTrac *
- Jasypt *
- Roller *
- Elastic Path *
- Atlassian Crowd *
- Your own authentication systems (see below)

项目模块：

- Core - spring-security-core.jar
- Remoting - spring-security-remoting.jar
- Web - spring-security-web.jar
- Config - spring-security-config.jar
- LDAP - spring-security-ldap.jar
- OAuth 2.0 Core - spring-security-oauth2-core.jar
- OAuth 2.0 Client - spring-security-oauth2-client.jar
- OAuth 2.0 JOSE - spring-security-oauth2-jose.jar
- ACL - spring-security-acl.jar
- CAS - spring-security-cas.jar
- OpenID - spring-security-openid.jar
- Test - spring-security-test.jar

_关于项目模块有不明白的地方，请查看官方文档了解详情。_

## 快速开始

本项目基于 Spring Boot 2.0.3 版本构建。在你的 Spring Boot 项目中添加 Spring Security 的依赖：

```
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-security</artifactId>
</dependency>
```

经检查发现，spring-boot-starter-security 模块仅仅包含了 Spring Security 的最小依赖：

```
<!-- Spring Security 5.0.6.RELEASE -->
<dependency>
	<groupId>org.springframework.security</groupId>
	<artifactId>spring-security-web</artifactId>
</dependency>
<dependency>
	<groupId>org.springframework.security</groupId>
	<artifactId>spring-security-config</artifactId>
</dependency>
```

如果你想要使用额外的功能，比如：LDAP 、OpenID 等等，你需要添加对应的模块。不过，使用 spring-boot-starter-security 模块的好处是：spring-boot-authconfigure 模块已经为我们提供了相关的默认配置。
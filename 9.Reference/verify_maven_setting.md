# Maven settings.xml Verification Guide

This guide provides steps to verify that your Maven `settings.xml` is correctly configured and working as expected.

## 1. Validate XML Syntax

Maven will usually complain if the XML is malformed, but you can explicitly check it by running any Maven command. A clean way to check without running a full build is:

```bash
mvn help:effective-settings
```

If the XML is malformed, Maven will fail with a `ParseException` or a similar error pointing to the line number.

## 2. Inspect Merged Configuration

Maven uses a hierarchy of settings (Global vs. User). To see the final configuration that Maven actually uses:

```bash
mvn help:effective-settings -Ddetail=true
```

> [!TIP]
> Use this to verify if your `<mirrors>`, `<proxies>`, or `<profiles>` are correctly merged and active.

## 3. Verify Repository Connectivity

To test if Maven can successfully reach a repository and download artifacts using your current settings (including authentication and mirrors), try to download a specific dependency:

```bash
mvn dependency:get -Dartifact=org.apache.maven:maven-core:3.9.1 -Dtransitive=false
```

If this succeeds, your connection to the central/mirrored repository is working.

## 4. Verify Credentials (Server Authentication)

If you have configured `<servers>` with credentials, Maven won't show the password in `effective-settings` for security reasons. To verify authentication for a private repository:

1. Check the `id` in your `settings.xml` matches the `id` in your project's `pom.xml` (`<repository>` or `<distributionManagement>`).
2. Attempt a `mvn deploy` (for publishing) or `mvn dependency:get` (for private artifacts) and check for `401 Unauthorized` or `403 Forbidden` errors.

## 5. Troubleshooting Common Issues

### HTTP Blocking

Since Maven 3.8.1, external HTTP repositories are blocked by default.
> [!WARNING]
> If you see an error about `maven-default-http-blocker`, ensure your repository URLs use `https://`.

### SSL Certificate Issues

If you are behind a corporate proxy or using a custom repository with an untrusted certificate:

- Run Maven with `-Djavax.net.ssl.trustStore=/path/to/truststore`.
- Or, for debugging only, use `-Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true`.

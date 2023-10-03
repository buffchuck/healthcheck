# healthcheck
Simple java healthcheck servlet for website

# web.xml
<?xml version="1.0" encoding="UTF-8"?>
<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xmlns="http://xmlns.jcp.org/xml/ns/javaee"
         xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/web-app_3_1.xsd"
         version="3.1">
  <servlet>
    <servlet-name>HealthCheckServlet</servlet-name>
    <servlet-class>HealthCheckServlet</servlet-class>
  </servlet>
  <servlet-mapping>
    <servlet-name>HealthCheckServlet</servlet-name>
    <url-pattern>/health</url-pattern>
  </servlet-mapping>
</web-app>

# web.xml needs to be inside the WEB-INF directory 
# typical structure for java web applications packaged as WAR
# healthcheck/
# ├── WEB-INF/
# │   ├── classes/
# │   │   └── (your package structure, if any)
# │   │       └── YourHealthCheckClass.class
# │   └── web.xml
# └── ... (any other resources or JSP files)

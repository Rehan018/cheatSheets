# Spring
<p><b>Step.1 :</b> Creating a Spring Project</p>
<p><b>Step.2 :</b> Add Dependencies to XML file</p>

```
<dependencies>
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter</artifactId>
  </dependency>
  <dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
    <scope>test</scope>
  </dependency>
  <dependency>
    <groupId>javax.annotation</groupId>
    <artifactId>javax.annotation-api</artifactId>
    <version>1.3.2</version>
  </dependency>
</dependencies>
```

<p><b>Step.3 :</b> Create Java Bean class</p>
<ul>
  <li>Generate Variables and Methods</li>
  <li>Generate Getter & Setter methods</li>
  <li>Generate Deafault & Parameterise constructor</li>
  <li>Generate toString() method</li>
</ul>

<p><b>Step.4 :</b> Create config.xml file</p>
<ul>
  <li>Add Beans tag</li>
  
  ```
  <beans  
    xmlns="http://www.springframework.org/schema/beans"  
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"  
    xmlns:p="http://www.springframework.org/schema/p"  
    xmlns:c="http://www.springframework.org/schema/c"  
    xmlns:context="http://www.springframework.org/schema/context"
    xsi:schemaLocation="http://www.springframework.org/schema/beans  
            http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
            http://www.springframework.org/schema/context
            http://www.springframework.org/schema/context/spring-context-3.0.xsd">
               
               <!-- <context:annotation-config/> -->
               <!-- Here is the Bean tag -->
               
  </beans>
  ```
  
  <li>Create Bean & Property tag</li>
  
  ```
  <bean class = "com.example.demo.student" name="student1">
        <property name="studentName">
            <value>seraj khan</value>
        </property>
  </bean>
  ```
  
  <p align="center">OR</p>
  
  ```
  <bean class = "com.example.demo.student" name="student2">
        <property name="studentName" value="seraj Alam"></property>
  </bean>
  ```
  
  <p align="center">OR</p>
  
  ```
  // property schema
  <bean class="com.example.demo.student" name="student3" p:studentName="Rehan Alam" p:studentId="505" p:studentCity="Lucknow" />
  ```

</ul>
<hr />
<p><b>Bean tag for collection type data</p>
<ul>
  <li>List</li>
  
  ```
  <bean>
    <property name="">
      <list>
        <value>10</value>
        <value>20</value>
        <value>20</value>
        <null />
      </list>
    </property>
  </bean>
  ```
  
  <li>Set</li>
  
  ```
  <bean>
    <property name="">
      <set>
        <value>10</value>
        <value>20</value>
        <value>30</value>
      </set>
    </property>
  </bean>
  ```
  
  <li>Map</li>
  
  ```
  <bean>
    <property name="">
      <map>
        <entry key="java" value="12 Months" />
        <entry key="python" value="2 Months" />
      </map>
    </property>
  </bean>
  ```
  
  <li>Properties</li>
  
  ```
  <bean>
    <property name="">
      <props>
        <prop key="java">12 Months</prop>
        <prop key="python">2 Months</prop>
      </props>
    </property>
  </bean>
  ```
  
  <li>Reference Type</li>
  
  ```
  <bean>
    <property name="">
      <props>
        <ref bean="name1" />
        <ref bean="name2" />
      </props>
    </property>
  </bean>
  ```
  
  <li>Constructor Injection</li>
  
  ```
  <bean>
    <constructor-args value="abc" />
    <constructor-args value="123" type="int" />
  </bean>
  ```

  <p align="center">OR</p>
  
  ```
  // constructor schema
  <bean class="com.example.demo.student" name="student3" c:studentName="Seraj" c:studentId="502" />
  ```
  
</ul>
<hr />

## Init && Destroy Method
<ul>
  <li><b>Using XML (Bean Tag)</b></li>
  
  ```
  <bean class="com.example.demo" name="__" init-method="init" destroy-method="destroy" />
  // add some Line to main class
  // Replace
  ApplicationContext => AbstractApplicationContext
  // Then Add
  context.registerShutdownHook();
  ```
  
  <li><b>Using Interfaces</b></li>
  
  ```
  implements InitializingBean, DisposableBean{
    public void afterPropertiesSet() throws Exception{
      // Init codes
    }
    
    public void destroy() throws Exception{
      // Destroy codes
    }
  }
  ```
  
  <li><b>Using Annotation</b></li>
  
  ```
  @PostConstruct
  public void init(){
    // Init codes
  }
  
  @PreDestroy
  public void destroy(){
    // Destroy codes
  }
  ```
  
</ul>
  
## AutoWiring

<ul>
  <li><b>Using XML</b></li>
  
  ```
  <bean class="com.example.demo" name="__" autowired="byName" />
  // OR
  <bean class="com.example.demo" name="__" autowired="byType" />
  // OR
  <bean class="com.example.demo" name="__" autowired="constructor" />
  ```
  
  <li><b>Using Annotation</b></li>
  
  ```
  @Autowired
  @Qualifier("beanName")
  ```
  

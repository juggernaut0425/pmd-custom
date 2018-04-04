# 代码检查

使用pmd maven插件分析java代码
    
    
## 规则地址

java，android
    
    https://pmd.github.io/pmd-6.2.0/pmd_rules_java.html
    
## maven配置


***如果原有配置中已经有<build>tag,注意合并***

 
    <build>
        <plugins>
            <plugin>
                 <groupId>org.apache.maven.plugins</groupId>
                 <artifactId>maven-pmd-plugin</artifactId>
                 <version>3.9</version>
                 <configuration>
                     <rulesets>
                         <ruleset>pmd/java_ruleset.xml</ruleset>
                     </rulesets>
                     <printFailingErrors>true</printFailingErrors>
                     <linkXRef>false</linkXRef>
                 </configuration>
                 <executions>
                     <execution>
                         <goals>
                             <goal>check</goal>
                         </goals>
                     </execution>
                 </executions>
                 <dependencies>
                     <dependency>
                         <groupId>org.tiggerlee</groupId>
                         <artifactId>pmd-custom</artifactId>
                         <version>6.2.0</version>
                     </dependency>
                 </dependencies>
             </plugin>
        </plugins>
    </build>
        
        


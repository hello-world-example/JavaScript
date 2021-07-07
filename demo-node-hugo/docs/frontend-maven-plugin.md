# frontend-maven-plugin

>- 官网 ： https://github.com/eirslett/frontend-maven-plugin

## NPM 示例

```xml
<!-- https://github.com/eirslett/frontend-maven-plugin#usage -->
<plugin>
    <groupId>com.github.eirslett</groupId>
    <artifactId>frontend-maven-plugin</artifactId>
    <version>1.8.0</version>

    <configuration>
        <workingDirectory>${project.basedir}/src/main/resources/node</workingDirectory>
        <!-- Latest LTS Version: 12.13.0 (includes npm 6.12.0) -->
        <!-- 文档 : http://npm.taobao.org/mirrors/node/v12.13.0/docs/api/index.html -->
        <nodeVersion>v12.13.0</nodeVersion>
        <!-- 默认 : https://nodejs.org/dist/ -->
        <nodeDownloadRoot>https://npm.taobao.org/mirrors/node/</nodeDownloadRoot>
        <!-- 包下载地址，默认：https://registry.npmjs.org/npm/-/ -->
        <npmDownloadRoot>https://registry.npm.taobao.org/</npmDownloadRoot>
    </configuration>

    <executions>
        <!-- 安装 node 和 npm -->
        <execution>
            <id>install node and npm</id>
            <goals>
                <goal>install-node-and-npm</goal>
            </goals>
        </execution>

        <!-- Install all project dependencies -->
        <execution>
            <id>npm install</id>
            <phase>prepare-package</phase>
            <goals>
                <goal>npm</goal>
            </goals>
            <configuration>
                <arguments>install</arguments>
            </configuration>
        </execution>

        <!-- Build and minify static files -->
        <execution>
            <id>npm run build</id>
          	<phase>prepare-package</phase>
            <goals>
                <goal>npm</goal>
            </goals>
            <configuration>
                <arguments>run build</arguments>
            </configuration>
        </execution>

    </executions>
</plugin>

```


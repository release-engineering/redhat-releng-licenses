
Introduction
============

This is a wrapper project to deploy custom license templates that can be used with the license-maven-plugin ( See [here](http://code.mycila.com/license-maven-plugin) ).

Formats
=======

Apache 2
--------
An alternative format for the Apache 2 license is available by specifiying

    <plugin>
        <groupId>com.mycila</groupId>
        <artifactId>license-maven-plugin</artifactId>
        <configuration>
           <header>APACHE-2-SIMPLIFIED-COPYRIGHT.txt</header>
        </configuration>
    </plugin>

in the project configuration. The allows `Copyright (C) ${project.inceptionYear} ${owner}` instead of `Copyright (C) ${project.inceptionYear} ${owner} (${email})` which is available from the default Apache 2 configuration.

JBoss
-----

An alternative format using the JBoss Apache 2 license is available by specifiying

    <plugin>
        <groupId>com.mycila</groupId>
        <artifactId>license-maven-plugin</artifactId>
        <configuration>
           <header>JBOSS-COPYRIGHT.txt</header>
        </configuration>
    </plugin>

in the project configuration. It is recommended to use [license-maven-plugin-git](https://github.com/mycila/license-maven-plugin/tree/master/license-maven-plugin-git) in conjunction with the license-maven-plugin as it automatically provides the correct information for `license.git.copyrightYears`. This extra configuration is automatic if the [redhat-releng-tools](https://github.com/release-engineering/redhat-releng-tools) is being used as a parent pom.

This provides a copyright message of:

    JBoss, Home of Professional Open Source.
    Copyright ${license.git.copyrightYears} Red Hat, Inc., and individual contributors
    as indicated by the @author tags.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

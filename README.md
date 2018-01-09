
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

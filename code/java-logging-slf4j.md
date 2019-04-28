---
layout: post
title: SLF4J - Logging Basics
bigimg: /img/4.jpg
categories: blogging
tags: slf4j logging
comments: false
analytics: false
---




## SLF4J Logging ##

> The Simple Logging Facade for Java (SLF4J) serves as a simple facade or abstraction for various logging frameworks (e.g. java.util.logging,
> logback, log4j) allowing the end user to plug in the desired logging
> framework at deployment time.

How to Declare
--------------

    import org.slf4j.Logger;
    import org.slf4j.LoggerFactory;
    
    1.private static final Logger LOGGER = LoggerFactory.getLogger(Test.class)
    2.private final Logger logger = LoggerFactory.getLogger(getClass())


**Logger should be final & private 
static or non static ?**

 1. PMD recommends static  (“LoggerIsNotStaticFinal” rule)
 2. SIF4 recommends non static http://www.slf4j.org/faq.html#declared_static
 3. 
Naming convention of variable LOGGER/logger is a matter of preference - PMD and SONAR recommends LOGGER(uppercase)

How to Log
----------
<br>
First of all there shouldn't be any concatenation operation


Use SLF4J expressions , It will delay the construction of the message.

Do:

    LOGGER.debug(“Some Object={}”,obj);

If debug is disabled  - the message will never be constructed


Just that you are passing two variables to the debug method.


1. Some Object={}
2. obj


Implementation of debug method takes care of constructing the message only if the debug is enabled.

Dont:

    LOGGER.debug(“Some Object=" + obj)

Even If debug is disabled  - the message will be constructed.
Here debug method is called with one argument.
`obj.toString()` is evaluated and concatenated.
The message is constructed even before calling the method.


What to Log
-----------

In case of exceptions , brief the issue


Always log the stack trace


Say if IOException occurred while reading a file

Do:

    LOGGER.error(“Error occurred - Unable to read the file {}”,absoluteFilePath,ex)

Last argument to the error method should be throwable.

Dont:

    LOGGER.error(“Error occurred”,ex)
    LOGGER.error(“Error occurred {}”,ex.getMessage())

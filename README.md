Zabbix.NET
===================


**Zabbix.NET** is .NET Zabbix API library which is incredible easy to use thanks to C# dynamic objects. 
There is no need for special classes for zabbix API methods. You can pass parameters via the anonymous objects. Or just your regular objects.

Usage:
```
Zabbix zabbix = new Zabbix(user, pass, zabbixUrl);
zabbix.Login();
string resultStr = zabbix.jsonRespopnse("host.get", new {output: "extend"});
Response reusultObj = zabbix.objectResponse("host.get", new {output: "extend"});
zabbix.Logout();
```
Note that you pass API method to Zabbix.jsonRespopnse (objectResponse) method as a string.

> **Note:**

> - Zabbix.NET uses Newtonsoft.Json library for json serialization and deserialization
> - .NET 4.0, but you can compile to any version of .NET as long as it supports ExpandoObject and Newtonsoft.Json 
> - Now available on NuGET **PM> Install-Package Zabbix.NET**
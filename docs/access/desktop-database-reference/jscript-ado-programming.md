---
title: JScript ADO-Programmierung
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 88a84f6fa3604286ca27651cefc999c96ff41d0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708971"
---
# <a name="jscript-ado-programming"></a>JScript ADO-Programmierung


**Betrifft**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Erstellen eines ADO-Projekts

Da von Microsoft JScript keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in JScript nicht definiert.

In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit JScript verwendet werden können:

- Verwenden, Sie für serverseitiges Skripting Datei Adojavas.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Ado\\ Ordner standardmäßig.

- Verwenden, Sie für clientseitiges Skripting Datei Adcjavas.inc ist das Laufwerk c: installiert\\Program Files\\gemeinsame Dateien\\System\\Msdac\\ Ordner standardmäßig.

Sie können entweder kopieren und Konstantendefinitionen aus diesen Dateien in ASP-Seiten einfügen, oder, wenn Sie serverseitiges Skripting, kopieren Sie die Datei Adojavas.inc-Datei in einen Ordner auf Ihrer Website, und es von der ASP verweist:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Erstellen von ADO-Objekten in JScript

Sie müssen stattdessen den **CreateObject** -Funktionsaufruf verwenden:

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>JScript (Beispiel)

Der folgende Code ist ein allgemeines Beispiel für die serverseitige JScript-Programmierung in einer ASP-Datei (Active Server Page), durch die ein **Recordset** -Objekt geöffnet wird:

```javascript 
 
<%  @LANGUAGE="JScript" %> 
<!--#include File="adojavas.inc"--> 
<HTML> 
<BODY BGCOLOR="White" topmargin="10" leftmargin="10"> 
<% 
var Source = "SELECT * FROM Authors"; 
var Connect =  "Provider=sqloledb;Data Source=srv;" + 
    "Initial Catalog=Pubs;Integrated Security=SSPI;" 
var Rs1 = Server.CreateObject( "ADODB.Recordset.2.5" ); 
Rs1.Open(Source,Connect,adOpenForwardOnly); 
Response.Write("Success!"); 
%> 
</BODY> 
</HTML> 
```


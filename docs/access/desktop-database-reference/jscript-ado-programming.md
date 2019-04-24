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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290891"
---
# <a name="jscript-ado-programming"></a>JScript ADO-Programmierung


**Gilt für**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Erstellen eines ADO-Projekts

Da von Microsoft JScript keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in JScript nicht definiert.

In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit JScript verwendet werden können:

- Für die serverseitige Skripterstellung verwenden Sie Datei adojavas. Inc, die standardmäßig im Ordner\\c:\\Program Files\\Common\\Files\\ System ADO installiert ist.

- Für die clientseitige Skripterstellung verwenden Sie Adcjavas. Inc, die standardmäßig im Ordner\\c:\\Program Files\\Common\\Files\\ System msdac installiert ist.

Sie können entweder kopieren und Einfügen von Konstanten Definitionen aus diesen Dateien in Ihre ASP-Seiten oder, wenn Sie serverseitige Skripterstellung durchführen, kopieren Sie die Datei Datei adojavas. Inc in einen Ordner auf Ihrer Website, und verweisen Sie auf Ihre ASP-Seite wie folgt:

```javascript  
 
<!--#include File="adojavas.inc"--> 
```

## <a name="creating-ado-objects-in-jscript"></a>Erstellen von ADO-Objekten in JScript

Sie müssen stattdessen den **CreateObject**-Funktionsaufruf verwenden:

```javascript  
 
var Rs1; 
Rs1 = Server.CreateObject("ADODB.Recordset"); 
```

## <a name="jscript-example"></a>JScript (Beispiel)

Der folgende Code ist ein allgemeines Beispiel für die serverseitige JScript-Programmierung in einer ASP-Datei (Active Server Page), durch die ein **Recordset**-Objekt geöffnet wird:

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


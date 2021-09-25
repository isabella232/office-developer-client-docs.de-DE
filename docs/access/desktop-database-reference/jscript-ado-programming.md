---
title: JScript ADO-Programmierung
TOCTitle: JScript ADO programming
ms:assetid: 2254f111-e6c2-1ad7-eb65-ee0550056d89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249002(v=office.15)
ms:contentKeyID: 48543706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0587f2d07342d97695524859ebca10248e70d931
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562601"
---
# <a name="jscript-ado-programming"></a>JScript ADO-Programmierung


**Gilt für**: Access 2013, Office 2013


## <a name="creating-an-ado-project"></a>Erstellen eines ADO-Projekts

Da von Microsoft JScript keine Typbibliotheken unterstützt werden, müssen Sie im Projekt nicht auf ADO verweisen. Daher werden keine zugehörigen Features wie die Vervollständigung der Befehlszeile unterstützt. Außerdem sind ADO-Aufzählungskonstanten standardmäßig in JScript nicht definiert.

In ADO werden jedoch zwei Includedateien bereitgestellt, die die folgenden Definitionen enthalten, die mit JScript verwendet werden können:

- Verwenden Sie für serverseitiges Skripting standardmäßig "Adojavas.inc", das im Ordner "c: \\ Program Files Common Files System \\ \\ \\ ado" installiert \\ ist.

- Verwenden Sie für clientseitige Skripts Adcjavas.inc, das standardmäßig im Ordner "c: \\ Program Files Common Files System \\ \\ \\ msdac" installiert \\ ist.

Sie können konstanten Definitionen aus diesen Dateien kopieren und in Ihre ASP-Seiten einfügen oder, wenn Sie serverseitige Skripts ausführen, die Datei "Adojavas.inc" in einen Ordner auf Ihrer Website kopieren und wie folgt von Ihrer ASP-Seite darauf verweisen:

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


---
title: 'Schritt 4: Empfangen und Anzeigen der Daten'
TOCTitle: 'Step 4: Receive and Display the Data'
ms:assetid: a27cc1d8-0ee0-95a5-ad70-88c454c10485
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249749(v=office.15)
ms:contentKeyID: 48546764
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2a447b68b8c0eeb18d18050ba8dbbb6f09786ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475344"
---
# <a name="step-4-receive-and-display-the-data"></a>Schritt 4: Empfangen und Anzeigen der Daten


**Betrifft**: Access 2013 | Office 2013

## <a name="step-4-receive-and-display-the-data"></a>Schritt 4: Empfangen und Anzeigen der Daten

In diesem Schritt erstellen Sie zum Abrufen des Recordset-Objekts eine HTML-Datei mit einem eingebetteten RDS.DataControl-Objekt, das auf die Datei XMLResponse.asp verweist. Öffnen Sie default.htm in einem Text-Editor, z. B. dem Editor von Windows, und fügen Sie den folgenden Code ein. Ersetzen Sie dabei "sqlserver" in der URL durch den Namen Ihres Servercomputers.

```html 
 
<HTML> 
<HEAD><TITLE>ADO Recordset Persistence Sample</TITLE></HEAD> 
<BODY> 
 
<TABLE DATASRC="#RDC1" border="1"> 
  <TR> 
<TD><SPAN DATAFLD="title"></SPAN></TD> 
<TD><SPAN DATAFLD="price"></SPAN></TD> 
  </TR> 
</TABLE> 

<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="RDC1"> 
   <PARAM NAME="URL" VALUE="XMLResponse.asp"> 
</OBJECT> 
 
</BODY> 
</HTML> 
```

Schließen Sie die Datei ' default.htm ', und speichern Sie sie im gleichen Ordner, in dem Sie XMLResponse.asp gespeichert. Mithilfe von InternetExplorer 4.0 oder höher, öffnen Sie die URL https://*Sqlserver*/XMLPersist/default.htm und zeigen Sie die Ergebnisse. Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt. Jetzt öffnen Sie die URL https://*Sqlserver*/XMLPersist/XMLResponse.asp, und zeigen Sie die Ergebnisse. Der XML-Code wird angezeigt.


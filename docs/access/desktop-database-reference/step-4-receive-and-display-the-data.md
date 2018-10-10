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
# <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="19b00-102">Schritt 4: Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="19b00-102">Step 4: Receive and Display the Data</span></span>


<span data-ttu-id="19b00-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="19b00-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-4-receive-and-display-the-data"></a><span data-ttu-id="19b00-104">Schritt 4: Empfangen und Anzeigen der Daten</span><span class="sxs-lookup"><span data-stu-id="19b00-104">Step 4: Receive and Display the Data</span></span>

<span data-ttu-id="19b00-p101">In diesem Schritt erstellen Sie zum Abrufen des Recordset-Objekts eine HTML-Datei mit einem eingebetteten RDS.DataControl-Objekt, das auf die Datei XMLResponse.asp verweist. Öffnen Sie default.htm in einem Text-Editor, z. B. dem Editor von Windows, und fügen Sie den folgenden Code ein. Ersetzen Sie dabei "sqlserver" in der URL durch den Namen Ihres Servercomputers.</span><span class="sxs-lookup"><span data-stu-id="19b00-p101">In this step you will create an HTML file with an embedded [RDS.DataControl](datacontrol-object-rds.md) object that points at the XMLResponse.asp file to get the **Recordset**. Open default.htm with a text editor, such as Windows Notepad, and add the code below. Replace "sqlserver" in the URL with the name of your server computer.</span></span>

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

<span data-ttu-id="19b00-108">Schließen Sie die Datei ' default.htm ', und speichern Sie sie im gleichen Ordner, in dem Sie XMLResponse.asp gespeichert.</span><span class="sxs-lookup"><span data-stu-id="19b00-108">Close the default.htm file and save it to the same folder where you saved XMLResponse.asp.</span></span> <span data-ttu-id="19b00-109">Mithilfe von InternetExplorer 4.0 oder höher, öffnen Sie die URL https://*Sqlserver*/XMLPersist/default.htm und zeigen Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="19b00-109">Using Internet Explorer 4.0 or later, open the URL https://*sqlserver*/XMLPersist/default.htm and observe the results.</span></span> <span data-ttu-id="19b00-110">Die Daten werden in einer gebundenen DHTML-Tabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19b00-110">The data is displayed in a bound DHTML table.</span></span> <span data-ttu-id="19b00-111">Jetzt öffnen Sie die URL https://*Sqlserver*/XMLPersist/XMLResponse.asp, und zeigen Sie die Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="19b00-111">Now open the URL https://*sqlserver*/XMLPersist/XMLResponse.asp and observe the results.</span></span> <span data-ttu-id="19b00-112">Der XML-Code wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="19b00-112">The XML is displayed.</span></span>


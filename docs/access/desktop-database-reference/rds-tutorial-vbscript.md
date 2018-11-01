---
title: RDS-Lernprogramm (VBScript)
TOCTitle: RDS Tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 449a752d4ab9e1680a3cf318e73802d39d7033fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884200"
---
# <a name="rds-tutorial-vbscript"></a>RDS-Lernprogramm (VBScript)


**Betrifft**: Access 2013, Office 2013

Hier handelt es sich um das in Microsoft Visual Basic Scripting Edition geschriebene RDS-Lernprogramm. Eine Beschreibung des Zweckes des Lernprogramms finden Sie unter [RDS-Lernprogramm](chapter-12-rds-tutorial.md).

In diesem Lernprogramm [RDS. DataControl](datacontrol-object-rds.md) und [RDS. DataSpace](dataspace-object-rds.md) werden zur Entwurfszeit erstellt – d. h., sie sind mit Object-Tags, wie folgt definiert:. Alternativ können diese Objekte auch zur Laufzeit mit der **Server.CreateObject** -Methode erstellt werden. Sie können das **RDS.DataControl** -Objekt beispielsweise folgendermaßen erstellen:

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

**Schritt 1- Angeben eines Serverprogramms**

VBScript kann es ausgeführt wird, durch Zugreifen auf die Active Server Pages verfügbare VBScript **Request.ServerVariables** -Methode den Namen der IIS-Webserver ermitteln:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Verwenden Sie für dieses Lernprogramm jedoch den imaginären Server "yourServer".


> [!NOTE]
> <P>Achten Sie auf den Datentyp von ByRef-Argumenten. In VBScript können Sie den Variablentyp nicht angeben, weshalb Sie immer einen Variant-Wert übergeben müssen. Bei Verwendung von HTTP lässt RDS das Übergeben eines Variant-Werts an eine Methode zu, die einen Nicht-Variant-Wert erwartet. Dazu müssen Sie die Variable jedoch mit der CreateObject-Methode des RDS.DataSpace-Objekts aufrufen. Wenn Sie DCOM oder einen In-Process-Server verwenden, müssen Sie die Parametertypen auf dem Client und dem Server angleichen, weil andernfalls ein Typenkonfliktfehler auftritt.</P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

**Schritt 2a - Aufrufen des Serverprogramms mit "RDS.DataControl"**

Das folgende Beispiel dient lediglich zur Veranschaulichung, dass das Standardverhalten des **RDS.DataControl** -Objekts im Ausführen der angegebenen Abfrage besteht.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

**Schritt 2b - Aufrufen des Serverprogramms mit "RDSServer.DataFactory "**

**Schritt 3 - Abrufen eines Recordset-Objekts durch den Server**

**Schritt 4 - Zurückgeben des Recordset-Objekts durch den Server**

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

**Schritt 5 - Verwendbarmachen des DataControl-Objekts durch visuelle Steuerelemente**

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

**Schritt 6a - Senden von Änderungen an den Server mithilfe von "RDS.DataControl"**

Das folgende Beispiel dient lediglich zur Veranschaulichung, wie das **RDS.DataControl** -Objekt Aktualisierungen ausführt.

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

**Schritt 6a - Senden von Änderungen an den Server mithilfe von "RDSServer.DataFactory"**

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Dies ist das Ende des Lernprogramms.**


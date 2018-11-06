---
title: RDS-Lernprogramm (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 996c0adf8c883de5c73174d726cf5bd11fc42457
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996881"
---
# <a name="rds-tutorial-vbscript"></a>RDS-Lernprogramm (VBScript)

**Betrifft**: Access 2013, Office 2013

Dies ist die in Microsoft Visual Basic Scripting Edition geschriebene RDS-Lernprogramm. Eine Beschreibung des Zwecks dieses Lernprogramm finden Sie im [RDS-Lernprogramm](chapter-12-rds-tutorial.md).

In diesem Lernprogramm [RDS. DataControl](datacontrol-object-rds.md) und [RDS. DataSpace](dataspace-object-rds.md) zur Entwurfszeit; erstellt werden d. h., werden sie mit der Object-Tags definiert. Alternativ können diese Objekte auch zur Laufzeit mit der **Server.CreateObject** -Methode erstellt werden. 

Sie können das **RDS.DataControl** -Objekt beispielsweise folgendermaßen erstellen:

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

## <a name="step-1--specify-a-server-program"></a>Schritt 1- Angeben eines Serverprogramms

VBScript kann es ausgeführt wird, durch Zugreifen auf die Active Server Pages verfügbare VBScript **Request.ServerVariables** -Methode den Namen der IIS-Webserver ermitteln:

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

Verwenden Sie für dieses Lernprogramm jedoch den imaginären Server "YourServer".

> [!NOTE]
> Achten Sie auf den Datentyp von ByRef-Argumenten. In VBScript können Sie den Variablentyp nicht angeben, weshalb Sie immer einen Variant-Wert übergeben müssen. Bei Verwendung von HTTP lässt RDS das Übergeben eines Variant-Werts an eine Methode zu, die einen Nicht-Variant-Wert erwartet. Dazu müssen Sie die Variable jedoch mit der CreateObject-Methode des RDS.DataSpace-Objekts aufrufen. Wenn Sie DCOM oder einen In-Process-Server verwenden, müssen Sie die Parametertypen auf dem Client und dem Server angleichen, weil andernfalls ein Typenkonfliktfehler auftritt.

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a>Schritt 2a - Aufrufen des Serverprogramms mit "RDS.DataControl"

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a>Schritt 2b - Aufrufen des Serverprogramms mit "RDSServer.DataFactory "

## <a name="step-3--server-obtains-a-recordset"></a>Schritt 3 - Abrufen eines Recordset-Objekts durch den Server

## <a name="step-4--server-returns-the-recordset"></a>Schritt 4 - Zurückgeben des Recordset-Objekts durch den Server

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a>Schritt 5 - Verwendbarmachen des DataControl-Objekts durch visuelle Steuerelemente

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a>Schritt 6a – Änderungen an den Server mit RDS. gesendet werden DataControl *

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a>Schritt 6a - Senden von Änderungen an den Server mithilfe von "RDSServer.DataFactory"

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

**Dies ist das Ende des Lernprogramms.**


---
title: RDS-Lernprogramm (VBScript)
TOCTitle: RDS tutorial (VBScript)
ms:assetid: 7a6596fd-00b9-a637-7d00-fb55a621305f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249506(v=office.15)
ms:contentKeyID: 48545792
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1c6b42d9560a30b45fb777bb4fd1de4351830a4
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936294"
---
# <a name="rds-tutorial-vbscript"></a><span data-ttu-id="796d4-102">RDS-Lernprogramm (VBScript)</span><span class="sxs-lookup"><span data-stu-id="796d4-102">RDS tutorial (VBScript)</span></span>

<span data-ttu-id="796d4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="796d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="796d4-104">Dies ist die in Microsoft Visual Basic Scripting Edition geschriebene RDS-Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="796d4-104">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="796d4-105">Eine Beschreibung des Zwecks dieses Lernprogramm finden Sie im [RDS-Lernprogramm](chapter-12-rds-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="796d4-105">For a description of the purpose of this tutorial, see the [RDS tutorial](chapter-12-rds-tutorial.md).</span></span>

<span data-ttu-id="796d4-106">In diesem Lernprogramm [RDS. DataControl](datacontrol-object-rds.md) und [RDS. DataSpace](dataspace-object-rds.md) zur Entwurfszeit; erstellt werden d. h., werden sie mit der Object-Tags definiert.</span><span class="sxs-lookup"><span data-stu-id="796d4-106">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="796d4-107">Alternativ können diese Objekte auch zur Laufzeit mit der **Server.CreateObject** -Methode erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="796d4-107">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="796d4-108">Sie können das **RDS.DataControl** -Objekt beispielsweise folgendermaßen erstellen:</span><span class="sxs-lookup"><span data-stu-id="796d4-108">For example, the **RDS.DataControl** object could be created like this:</span></span>

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

## <a name="step-1--specify-a-server-program"></a><span data-ttu-id="796d4-109">Schritt 1- Angeben eines Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="796d4-109">Step 1 — Specify a server program</span></span>

<span data-ttu-id="796d4-110">VBScript kann es ausgeführt wird, durch Zugreifen auf die Active Server Pages verfügbare VBScript **Request.ServerVariables** -Methode den Namen der IIS-Webserver ermitteln:</span><span class="sxs-lookup"><span data-stu-id="796d4-110">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="796d4-111">Verwenden Sie für dieses Lernprogramm jedoch den imaginären Server "YourServer".</span><span class="sxs-lookup"><span data-stu-id="796d4-111">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <P><span data-ttu-id="796d4-p103">Achten Sie auf den Datentyp von ByRef-Argumenten. In VBScript können Sie den Variablentyp nicht angeben, weshalb Sie immer einen Variant-Wert übergeben müssen. Bei Verwendung von HTTP lässt RDS das Übergeben eines Variant-Werts an eine Methode zu, die einen Nicht-Variant-Wert erwartet. Dazu müssen Sie die Variable jedoch mit der CreateObject-Methode des RDS.DataSpace-Objekts aufrufen. Wenn Sie DCOM oder einen In-Process-Server verwenden, müssen Sie die Parametertypen auf dem Client und dem Server angleichen, weil andernfalls ein Typenkonfliktfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="796d4-p103">Pay attention to the data type of <STRONG>ByRef</STRONG> arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the <STRONG>RDS.DataSpace</STRONG> object <A href="createobject-method-rds.md">CreateObject</A> method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span></P>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

## <a name="step-2a--invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="796d4-116">Schritt 2a - Aufrufen des Serverprogramms mit "RDS.DataControl"</span><span class="sxs-lookup"><span data-stu-id="796d4-116">Step 2a — Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="796d4-117">Das folgende Beispiel dient lediglich zur Veranschaulichung, dass das Standardverhalten des **RDS.DataControl** -Objekts im Ausführen der angegebenen Abfrage besteht.</span><span class="sxs-lookup"><span data-stu-id="796d4-117">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

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

## <a name="step-2b--invoke-the-server-program-with-rdsserverdatafactory"></a><span data-ttu-id="796d4-118">Schritt 2b - Aufrufen des Serverprogramms mit "RDSServer.DataFactory "</span><span class="sxs-lookup"><span data-stu-id="796d4-118">Step 2b — Invoke the server program with RDSServer.DataFactory</span></span>

## <a name="step-3--server-obtains-a-recordset"></a><span data-ttu-id="796d4-119">Schritt 3 - Abrufen eines Recordset-Objekts durch den Server</span><span class="sxs-lookup"><span data-stu-id="796d4-119">Step 3 — Server obtains a Recordset</span></span>

## <a name="step-4--server-returns-the-recordset"></a><span data-ttu-id="796d4-120">Schritt 4 - Zurückgeben des Recordset-Objekts durch den Server</span><span class="sxs-lookup"><span data-stu-id="796d4-120">Step 4 — Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

## <a name="step-5--datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="796d4-121">Schritt 5 - Verwendbarmachen des DataControl-Objekts durch visuelle Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="796d4-121">Step 5 — DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

## <a name="step-6a--changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="796d4-122">Schritt 6a – Änderungen an den Server mit RDS. gesendet werden DataControl \*</span><span class="sxs-lookup"><span data-stu-id="796d4-122">Step 6a — Changes are sent to the server with RDS.DataControl\*</span></span>

<span data-ttu-id="796d4-123">Das folgende Beispiel dient lediglich zur Veranschaulichung, wie das **RDS.DataControl** -Objekt Aktualisierungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="796d4-123">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

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

## <a name="step-6b--changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="796d4-124">Schritt 6a - Senden von Änderungen an den Server mithilfe von "RDSServer.DataFactory"</span><span class="sxs-lookup"><span data-stu-id="796d4-124">Step 6b — Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

<span data-ttu-id="796d4-125">**Dies ist das Ende des Lernprogramms.**</span><span class="sxs-lookup"><span data-stu-id="796d4-125">**This is the end of the tutorial.**</span></span>


---
title: 'Schritt 2: Abrufen der Daten'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80dae05dc691343b3c89ce8fd3ccfe72b776984c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860329"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="22a50-102">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="22a50-102">Step 2: Get the Data</span></span>


<span data-ttu-id="22a50-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="22a50-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="22a50-104">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="22a50-104">Step 2: Get the Data</span></span>

<span data-ttu-id="22a50-p101">In diesem Schritt schreiben Sie Code, mit dem ein ADO-Objekt Recordset geöffnet wird, und bereiten dessen Senden an den Client vor. Öffnen Sie die Datei XMLResponse.asp in einem Text-Editor, z. B. dem Editor von Windows, und fügen Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="22a50-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="22a50-107">Achten Sie darauf, dass Sie den Wert des Parameters Datenquelle im Parameter StrCon auf den Namen des Microsoft SQL Server-Computers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="22a50-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="22a50-108">Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="22a50-108">Keep the file open and go on to the next step.</span></span>

### <a name="next-step"></a><span data-ttu-id="22a50-109">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="22a50-109">Next step</span></span>

[<span data-ttu-id="22a50-110">Schritt 3: Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="22a50-110">Step 3: Send the Data</span></span>](step-3-send-the-data.md)


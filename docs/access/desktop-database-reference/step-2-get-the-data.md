---
title: 'Schritt 2: Abrufen der Daten'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4b93eb3e3679fdbc235f4406b0480ad2597d25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472908"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="1e0fd-102">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="1e0fd-102">Step 2: Get the Data</span></span>


<span data-ttu-id="1e0fd-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e0fd-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="1e0fd-104">Schritt 2: Abrufen der Daten</span><span class="sxs-lookup"><span data-stu-id="1e0fd-104">Step 2: Get the Data</span></span>

<span data-ttu-id="1e0fd-p101">In diesem Schritt schreiben Sie Code, mit dem ein ADO-Objekt Recordset geöffnet wird, und bereiten dessen Senden an den Client vor. Öffnen Sie die Datei XMLResponse.asp in einem Text-Editor, z. B. dem Editor von Windows, und fügen Sie den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="1e0fd-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

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

<span data-ttu-id="1e0fd-107">Achten Sie darauf, dass Sie den Wert des Parameters Datenquelle im Parameter StrCon auf den Namen des Microsoft SQL Server-Computers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1e0fd-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="1e0fd-108">Lassen Sie die Datei geöffnet, und wechseln Sie zum nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="1e0fd-108">Keep the file open and go on to the next step.</span></span>

<span data-ttu-id="1e0fd-109">**Nächste** [Schritt 3: Senden der Daten](step-3-send-the-data.md)</span><span class="sxs-lookup"><span data-stu-id="1e0fd-109">**Next** [Step 3: Send the Data](step-3-send-the-data.md)</span></span>


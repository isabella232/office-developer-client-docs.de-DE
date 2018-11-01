---
title: 'Schritt 3: Senden der Daten'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5af9b24ac7edb77ceb6dea9ceb5ae8e628fa5e3b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889707"
---
# <a name="step-3-send-the-data"></a><span data-ttu-id="408a3-102">Schritt 3: Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="408a3-102">Step 3: Send the Data</span></span>


<span data-ttu-id="408a3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="408a3-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-3-send-the-data"></a><span data-ttu-id="408a3-104">Schritt 3: Senden der Daten</span><span class="sxs-lookup"><span data-stu-id="408a3-104">Step 3: Send the Data</span></span>

<span data-ttu-id="408a3-p101">Sie besitzen nun ein Recordset-Objekt und müssen es an den Client senden, indem Sie es im XML-Format im ASP-Objekt Response speichern. Fügen Sie am Ende von XMLResponse.asp den folgenden Code hinzu:</span><span class="sxs-lookup"><span data-stu-id="408a3-p101">Now that you have a **Recordset**, you need to send it to the client by saving it as XML to the ASP **Response** object. Add the following code to the bottom of XMLResponse.asp:</span></span>

```vb 
 
  Response.ContentType = "text/xml" 
  Response.Expires = 0 
  Response.Buffer = False 
 
 
  Response.Write "<?xml version='1.0'?>" & vbNewLine 
  adoRec.save Response, adPersistXML 
  adoRec.Close 
  Set adoRec=Nothing 
%> 
```

<span data-ttu-id="408a3-107">Beachten Sie, dass das ASP- **Response** -Objekt als Ziel für die **Recordset-Objekt** [Speichern](save-method-ado.md) -Methode angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="408a3-107">Notice that the ASP **Response** object is specified as the destination for the **Recordset** [Save](save-method-ado.md) method.</span></span> <span data-ttu-id="408a3-108">Das Ziel des **Save** -Methode kann jedes Objekt sein, die unterstützt die **IStream** -Schnittstelle, wie ein ADO- [Stream](stream-object-ado.md) -Objekt oder einen Dateinamen ein, der den vollständigen Pfad enthält, wird das **Recordset-Objekt** gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="408a3-108">The destination of the **Save** method can be any object that supports the **IStream** interface, such as an ADO [Stream](stream-object-ado.md) object, or a file name that includes the complete path to which the **Recordset** is to be saved.</span></span>

<span data-ttu-id="408a3-109">Speichern Sie und schließen Sie XMLResponse.asp, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="408a3-109">Save and close XMLResponse.asp before going to the next step.</span></span> <span data-ttu-id="408a3-110">Kopieren Sie die Datei adovbs.inc-Datei auch von C:\\Program Files\\gemeinsame Dateien\\System\\Ado-Ordner im gleichen Ordner, in dem Sie die Datei XMLResponse.asp verfügen.</span><span class="sxs-lookup"><span data-stu-id="408a3-110">Also copy the adovbs.inc file from C:\\Program Files\\Common Files\\System\\Ado folder to the same folder where you have the XMLResponse.asp file.</span></span>

### <a name="next-step"></a><span data-ttu-id="408a3-111">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="408a3-111">Next step</span></span>

[<span data-ttu-id="408a3-112">Schritt 4: Empfangen der Daten</span><span class="sxs-lookup"><span data-stu-id="408a3-112">Step 4: Receive the Data</span></span>](step-4-receive-and-display-the-data.md)


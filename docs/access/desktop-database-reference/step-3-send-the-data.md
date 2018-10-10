---
title: 'Schritt 3: Senden der Daten'
TOCTitle: 'Step 3: Send the Data'
ms:assetid: d22ffe59-179b-fd1a-1211-be1a0d76b02f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250049(v=office.15)
ms:contentKeyID: 48547878
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed3e6bfd6fe3b6727055eb264b1261b13d7a5a0b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472858"
---
# <a name="step-3-send-the-data"></a>Schritt 3: Senden der Daten


**Betrifft**: Access 2013 | Office 2013

## <a name="step-3-send-the-data"></a>Schritt 3: Senden der Daten

Sie besitzen nun ein Recordset-Objekt und müssen es an den Client senden, indem Sie es im XML-Format im ASP-Objekt Response speichern. Fügen Sie am Ende von XMLResponse.asp den folgenden Code hinzu:

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

Beachten Sie, dass das ASP- **Response** -Objekt als Ziel für die **Recordset-Objekt** [Speichern](save-method-ado.md) -Methode angegeben wird. Das Ziel des **Save** -Methode kann jedes Objekt sein, die unterstützt die **IStream** -Schnittstelle, wie ein ADO- [Stream](stream-object-ado.md) -Objekt oder einen Dateinamen ein, der den vollständigen Pfad enthält, wird das **Recordset-Objekt** gespeichert werden soll.

Speichern Sie und schließen Sie XMLResponse.asp, bevor Sie mit dem nächsten Schritt fortfahren. Kopieren Sie die Datei adovbs.inc-Datei auch von C:\\Program Files\\gemeinsame Dateien\\System\\Ado-Ordner im gleichen Ordner, in dem Sie die Datei XMLResponse.asp verfügen.

**Nächste** [Schritt 4: Empfangen der Daten](step-4-receive-and-display-the-data.md)


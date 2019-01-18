---
title: Speichern von hierarchische Recordsets
TOCTitle: Persisting hierarchical Recordsets
ms:assetid: 28f48d4a-1c32-7b60-cd65-51fb87c5380e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249048(v=office.15)
ms:contentKeyID: 48543872
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1964d207f2b35eaeaf51b409adc12a41eac6438f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718609"
---
# <a name="persisting-hierarchical-recordsets"></a><span data-ttu-id="16eb2-102">Speichern von hierarchische Recordsets</span><span class="sxs-lookup"><span data-stu-id="16eb2-102">Persisting hierarchical Recordsets</span></span>

<span data-ttu-id="16eb2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16eb2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16eb2-p101">Sie können ein hierarchisches **Recordset** durch Aufrufen der [Save](save-method-ado.md)-Methode im ADTG- oder im XML-Format speichern. Beim Speichern hierarchischer **Recordset**-Objekte im XML-Format gelten jedoch zwei Einschränkungen: Das Speichern im XML-Format ist nicht möglich, wenn das hierarchische **Recordset**-Objekt ausstehende Aktualisierungen enthält, und es kann kein parametrisiertes hierarchisches **Recordset**-Objekt gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="16eb2-p101">You can save a hierarchical **Recordset** to a file in either ADTG or XML format by calling the [Save](save-method-ado.md) method. However, two limitations apply when saving hierarchical **Recordset**s in XML format: You cannot save in XML if the hierarchical **Recordset** contains pending updates, and you cannot save a parameterized hierarchical **Recordset**.</span></span>

<span data-ttu-id="16eb2-106">Weitere Informationen zum Datenstrukturierungsanbieter finden Sie unter Microsoft Data Shaping Dienst für OLE DB (ADO) und Der Data Shaping Dienst für OLE DB (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="16eb2-106">For more information about the Data Shaping provider, see [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) (ADO) and The Data Shaping Service for OLE DB(OLE DB).</span></span>


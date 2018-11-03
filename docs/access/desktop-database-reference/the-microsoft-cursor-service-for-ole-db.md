---
title: Microsoft Cursor Service für OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fece7aea728e1c98ac290c23172ce351cc38f342
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947189"
---
# <a name="microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="f9378-102">Microsoft Cursor Service für OLE DB</span><span class="sxs-lookup"><span data-stu-id="f9378-102">Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="f9378-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9378-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9378-p101">Wenn Sie einen clientseitigen Cursor auswählen oder die **CursorLocation** -Eigenschaft auf **adUseClient** festlegen, wird der Microsoft Cursor Service für OLE DB aufgerufen. Möglicherweise werden auch Verweise auf "Client Cursor Engine" angezeigt, wobei es sich im Prinzip um die Entsprechung im ADO-Kontext handelt. Dieser Dienst ergänzt die Cursorunterstützungsfunktionen von Datenprovidern. Sie erhalten daher relativ einheitliche Funktionalität von allen Datenprovidern.</span><span class="sxs-lookup"><span data-stu-id="f9378-p101">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB. You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO. This service supplements the cursor-support functions of data providers. As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="f9378-p102">Der Microsoft Cursor Service für OLE DB stellt dynamische Eigenschaften bereit und optimiert das Verhalten bestimmter Methoden. Beispielsweise können mit der dynamischen Eigenschaft **Optimize** temporäre Indizes erstellt werden, um bestimmte Vorgänge zu ermöglichen, wie z. B. die **Find** -Methode.</span><span class="sxs-lookup"><span data-stu-id="f9378-p102">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods. For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="f9378-p103">Der Microsoft Cursor Service für OLE DB ermöglicht die Unterstützung der Batchaktualisierung in allen Fällen. Er simuliert außerdem leistungsfähigere Cursortypen, wie z. B. dynamische Cursor, wenn ein Datenprovider nur weniger leistungsfähige Cursor bereitstellen kann, wie z. B. statische Cursor.</span><span class="sxs-lookup"><span data-stu-id="f9378-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>


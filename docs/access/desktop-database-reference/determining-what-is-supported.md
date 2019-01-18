---
title: Bestimmen, was unterstützt wird
TOCTitle: Determining what is supported
ms:assetid: 47b44dc9-e0fd-f204-0c68-e0de9247ee2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249221(v=office.15)
ms:contentKeyID: 48544602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abef84f05ad279edba1fcc753f0b412a807a7b9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712694"
---
# <a name="determining-what-is-supported"></a><span data-ttu-id="81d1c-102">Bestimmen, was unterstützt wird</span><span class="sxs-lookup"><span data-stu-id="81d1c-102">Determining what is supported</span></span>

<span data-ttu-id="81d1c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81d1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81d1c-p101">Mit der **Supports** -Methode bestimmen Sie, ob ein angegebenes **Recordset** -Objekt eine bestimmte Funktionalität unterstützt. Diese Methode weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="81d1c-p101">The **Supports** method is used to determine whether a specified **Recordset** object supports a particular type of functionality. It has the following syntax:</span></span>

`boolean = recordset.Supports( CursorOptions )`

<span data-ttu-id="81d1c-p102">**Supports** gibt einen booleschen Wert zurück, der anzeigt, ob alle vom Argument *CursorOptions* identifizierten Features vom Anbieter unterstützt werden. Mithilfe der **Supports**-Methode können Sie bestimmen, welche Funktionalität von einem **Recordset**-Objekt unterstützt wird. Falls das **Recordset**-Objekt die Features unterstützt, deren entsprechende Konstanten in *CursorOptions* vorhanden sind, gibt die **Supports**-Methode **True** zurück. Andernfalls wird **False** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="81d1c-p102">**Supports** returns a Boolean value that indicates whether all of the features identified by the *CursorOptions* argument are supported by the provider. You can use the **Supports** method to determine what types of functionality a **Recordset** object supports. If the **Recordset** object supports the features whose corresponding constants are in *CursorOptions*, the **Supports** method returns **True**. Otherwise, it returns **False**.</span></span>

<span data-ttu-id="81d1c-p103">Mithilfe der **Supports** -Methode können Sie überprüfen, ob Sie mit dem **Recordset** -Objekt neue Datensätze hinzufügen, Lesezeichen verwenden, die **Find** -Methode verwenden, den Fensterinhalt verschieben, die **Index** -Eigenschaft verwenden und Batchaktualisierungen ausführen können. Eine vollständige Liste der Konstanten und deren Bedeutung finden Sie unter [CursorOptionEnum](cursoroptionenum.md).</span><span class="sxs-lookup"><span data-stu-id="81d1c-p103">Using the **Supports** method, you can check for the ability of the **Recordset** object to add new records, use bookmarks, use the **Find** method, use scrolling, use the **Index** property, and to perform batch updates. For a complete list of constants and their meanings, see [CursorOptionEnum](cursoroptionenum.md).</span></span>

<span data-ttu-id="81d1c-p104">Die **Supports** -Methode kann zwar **True** für eine bestimmte Funktionalität zurückgeben, aber dies garantiert nicht, dass der Anbieter das Feature unter allen Umständen zur Verfügung stellen kann. Die **Supports** -Methode gibt einfach zurück, ob der Anbieter die angegebene Funktionalität unterstützen kann, vorausgesetzt bestimmte Bedingungen sind erfüllt. Beispielsweise kann die **Supports** -Methode angeben, dass ein **Recordset** -Objekt Aktualisierungen unterstützt, obwohl der Cursor auf einer Verknüpfung mehrerer Tabellen basiert , von denen manche Spalten nicht aktualisierbar sind.</span><span class="sxs-lookup"><span data-stu-id="81d1c-p104">Although the **Supports** method may return **True** for a given functionality, it does not guarantee that the provider can make the feature available under all circumstances. The **Supports** method simply returns whether the provider can support the specified functionality, assuming certain conditions are met. For example, the **Supports** method may indicate that a **Recordset** object supports updates, even though the cursor is based on a multiple table join — some columns of which are not updateable.</span></span>


---
title: Description-Eigenschaft (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc2a7706afbf69d9949e8b04122b144c6826ec40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882938"
---
# <a name="description-property-ado"></a><span data-ttu-id="c04fa-102">Description-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="c04fa-102">Description property (ADO)</span></span>


<span data-ttu-id="c04fa-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c04fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c04fa-104">Beschreibt ein [Error](error-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c04fa-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="c04fa-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c04fa-105">Return value</span></span>

<span data-ttu-id="c04fa-106">Gibt einen Wert vom Datentyp **String** zurück, der eine Beschreibung des Fehlers enthält.</span><span class="sxs-lookup"><span data-stu-id="c04fa-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c04fa-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c04fa-107">Remarks</span></span>

<span data-ttu-id="c04fa-p101">Verwenden Sie die **Description** -Eigenschaft, um eine kurze Beschreibung des Fehlers zu erhalten. Zeigen Sie diese Eigenschaft an, um den Benutzer auf einen Fehler hinzuweisen, den Sie nicht behandeln können oder möchten. Die Zeichenfolge stammt aus ADO oder von einem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="c04fa-p102">Die Anbieter sind für das Übergeben eines bestimmten Fehlertexts an ADO verantwortlich. ADO fügt für jeden Anbieterfehler oder jede erhaltene Warnung der [Errors](error-object-ado.md) -Auflistung ein **Error**-Objekt hinzu. Zeigen Sie die **Errors** -Auflistung an, um die vom Anbieter gemeldeten Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c04fa-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>


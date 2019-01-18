---
title: Description-Eigenschaft (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698932"
---
# <a name="description-property-ado"></a><span data-ttu-id="7dbb4-102">Description-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="7dbb4-102">Description property (ADO)</span></span>


<span data-ttu-id="7dbb4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7dbb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7dbb4-104">Beschreibt ein [Error](error-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7dbb4-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dbb4-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7dbb4-105">Return value</span></span>

<span data-ttu-id="7dbb4-106">Gibt einen Wert vom Datentyp **String** zurück, der eine Beschreibung des Fehlers enthält.</span><span class="sxs-lookup"><span data-stu-id="7dbb4-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dbb4-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7dbb4-107">Remarks</span></span>

<span data-ttu-id="7dbb4-p101">Verwenden Sie die **Description** -Eigenschaft, um eine kurze Beschreibung des Fehlers zu erhalten. Zeigen Sie diese Eigenschaft an, um den Benutzer auf einen Fehler hinzuweisen, den Sie nicht behandeln können oder möchten. Die Zeichenfolge stammt aus ADO oder von einem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="7dbb4-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="7dbb4-p102">Die Anbieter sind für das Übergeben eines bestimmten Fehlertexts an ADO verantwortlich. ADO fügt für jeden Anbieterfehler oder jede erhaltene Warnung der [Errors](error-object-ado.md) -Auflistung ein **Error**-Objekt hinzu. Zeigen Sie die **Errors** -Auflistung an, um die vom Anbieter gemeldeten Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7dbb4-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>


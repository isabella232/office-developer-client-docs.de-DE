---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf7b30021f030cff54f501250b7da4059e38c52a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944613"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="e81f8-102">Source-Eigenschaft (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="e81f8-102">Source property (ADO Error)</span></span>


<span data-ttu-id="e81f8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e81f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e81f8-104">Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="e81f8-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="e81f8-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e81f8-105">Return value</span></span>

<span data-ttu-id="e81f8-106">Gibt einen **String** -Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="e81f8-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="e81f8-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e81f8-107">Remarks</span></span>

<span data-ttu-id="e81f8-108">Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="e81f8-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="e81f8-109">Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln.</span><span class="sxs-lookup"><span data-stu-id="e81f8-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="e81f8-110">Bei Fehlern in ADO werden der Eigenschaftswert \**ADODB. \*\*\* ObjectName*, wobei *ObjectName* der Name des Objekts entspricht, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="e81f8-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="e81f8-111">Für ADO MD und ADOX werden der Wert \**ADOX. \*\*\* ObjectName* und \**ADOMD. \*\*\* ObjectName,* fest.</span><span class="sxs-lookup"><span data-stu-id="e81f8-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="e81f8-112">Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="e81f8-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="e81f8-113">Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e81f8-113">The **Source** property is read-only for **Error** objects.</span></span>


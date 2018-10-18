---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adeadcf4c467aabad7b486bd43c12e26d67ce302
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603865"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="bccf5-102">Source-Eigenschaft (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="bccf5-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="bccf5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bccf5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bccf5-104">Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="bccf5-104">Indicates the name of the object or application that originally generated an error.</span></span>

<span data-ttu-id="bccf5-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="bccf5-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="bccf5-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bccf5-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="bccf5-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bccf5-107">Return value</span></span>
>>>>>>> <span data-ttu-id="bccf5-108">master</span><span class="sxs-lookup"><span data-stu-id="bccf5-108">master</span></span>

<span data-ttu-id="bccf5-109">Gibt einen **String** -Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="bccf5-109">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="bccf5-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bccf5-110">Remarks</span></span>

<span data-ttu-id="bccf5-111">Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="bccf5-111">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="bccf5-112">Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln.</span><span class="sxs-lookup"><span data-stu-id="bccf5-112">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="bccf5-113">Bei Fehlern in ADO werden der Eigenschaftswert \**ADODB. \*\*\* ObjectName*, wobei *ObjectName* der Name des Objekts entspricht, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="bccf5-113">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="bccf5-114">Für ADO MD und ADOX werden der Wert \**ADOX. \*\*\* ObjectName* und \**ADOMD. \*\*\* ObjectName,* fest.</span><span class="sxs-lookup"><span data-stu-id="bccf5-114">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="bccf5-115">Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="bccf5-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="bccf5-116">Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="bccf5-116">The **Source** property is read-only for **Error** objects.</span></span>


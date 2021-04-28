---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061307"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="1e32b-102">Source-Eigenschaft (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="1e32b-102">Source property (ADO Error)</span></span>


<span data-ttu-id="1e32b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e32b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e32b-104">Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="1e32b-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e32b-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e32b-105">Return value</span></span>

<span data-ttu-id="1e32b-106">Gibt einen **String**-Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="1e32b-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e32b-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e32b-107">Remarks</span></span>

<span data-ttu-id="1e32b-108">Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="1e32b-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="1e32b-109">Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln.</span><span class="sxs-lookup"><span data-stu-id="1e32b-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="1e32b-110">Bei Fehlern in ADO lautet der Eigenschaftswert **ADODB.**</span><span class="sxs-lookup"><span data-stu-id="1e32b-110">For errors in ADO, the property value will be **ADODB.**</span></span> <span data-ttu-id="1e32b-111">*ObjectName*, wobei *ObjectName* der Name des Objekts ist, das den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="1e32b-111">*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="1e32b-112">Bei ADOX und ADO MD lautet der Wert jeweils **ADOX.**</span><span class="sxs-lookup"><span data-stu-id="1e32b-112">For ADOX and ADO MD, the value will be **ADOX.**</span></span> <span data-ttu-id="1e32b-113">*ObjectName* und **ADOMD.**</span><span class="sxs-lookup"><span data-stu-id="1e32b-113">*ObjectName* and **ADOMD.**</span></span> <span data-ttu-id="1e32b-114">*ObjectName*.</span><span class="sxs-lookup"><span data-stu-id="1e32b-114">*ObjectName,* respectively.</span></span>

<span data-ttu-id="1e32b-115">Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error**-Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="1e32b-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="1e32b-116">Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1e32b-116">The **Source** property is read-only for **Error** objects.</span></span>


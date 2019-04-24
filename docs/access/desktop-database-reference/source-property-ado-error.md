---
title: Source-Eigenschaft (ADO Error)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308596"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="08eea-102">Source-Eigenschaft (ADO Error)</span><span class="sxs-lookup"><span data-stu-id="08eea-102">Source property (ADO Error)</span></span>


<span data-ttu-id="08eea-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="08eea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08eea-104">Gibt den Namen des Objekts oder der Anwendung an, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="08eea-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="08eea-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08eea-105">Return value</span></span>

<span data-ttu-id="08eea-106">Gibt einen **String**-Wert zurück, der den Namen eines Objekts oder einer Anwendung angibt.</span><span class="sxs-lookup"><span data-stu-id="08eea-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="08eea-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08eea-107">Remarks</span></span>

<span data-ttu-id="08eea-108">Verwenden Sie die **Source** -Eigenschaft für ein [Error](error-object-ado.md)-Objekt, um den Namen des Objekts oder der Anwendung zu ermitteln, die einen Fehler ursprünglich generierte.</span><span class="sxs-lookup"><span data-stu-id="08eea-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="08eea-109">Dabei kann es sich um den Klassennamen oder die ProgID des Objekts handeln.</span><span class="sxs-lookup"><span data-stu-id="08eea-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="08eea-110">Bei Fehlern in ADO ist der Eigenschaftswert \**ADODB. \* \* \* ObjectName*, wobei \*\* ObjectName der Namen des Objekts ist, das den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="08eea-110">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="08eea-111">Für ADOX und ADO MD lautet der Wert \*\*ADOX. \* \*\* \* ObjectName und \**ADOMD. \* \* \* ObjectName* .</span><span class="sxs-lookup"><span data-stu-id="08eea-111">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="08eea-112">Anhand der Fehlerdokumentation der Eigenschaften **Source**, [Number](number-property-ado.md) und [Description](description-property-ado.md) von **Error** -Objekten können Sie Code schreiben, mit dem der Fehler ordnungsgemäß behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="08eea-112">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="08eea-113">Die **Source** -Eigenschaft ist für **Error** -Objekte schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="08eea-113">The **Source** property is read-only for **Error** objects.</span></span>


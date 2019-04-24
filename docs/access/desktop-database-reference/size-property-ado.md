---
title: Size-Eigenschaft (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306930"
---
# <a name="size-property-ado"></a><span data-ttu-id="236a1-102">Size-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="236a1-102">Size property (ADO)</span></span>


<span data-ttu-id="236a1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="236a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="236a1-104">Gibt die maximale Größe eines [Parameter](parameter-object-ado.md)-Objekts in Bytes oder Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="236a1-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="236a1-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="236a1-105">Settings and return values</span></span>

<span data-ttu-id="236a1-106">Legt einen **Long**-Wert fest, der die maximale Größe eines Werts in einem **Parameter**-Objekt in Bytes oder Zeichen angibt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="236a1-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="236a1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="236a1-107">Remarks</span></span>

<span data-ttu-id="236a1-108">Bestimmen Sie mit der **Size**-Eigenschaft die maximale Größe von Werten, die in die [Value](value-property-ado.md)-Eigenschaft eines **Parameter**-Objekts geschrieben oder daraus gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="236a1-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="236a1-109">Wenn Sie einen Datentyp variabler Länge für ein **Parameter**-Objekt angeben (beispielsweise einen beliebigen **String**-Typ wie z. B. **adVarChar**), müssen Sie die **Size**-Eigenschaft festlegen, bevor Sie sie der [Parameters](parameters-collection-ado.md)-Auflistung anfügen. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="236a1-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="236a1-110">Wenn Sie das **Parameter** -Objekt bereits der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts angefügt haben und seinen Typ in einen Datentyp variabler Länge ändern, müssen Sie die **Size** -Eigenschaft des **Parameter** -Objekts festlegen, bevor Sie das **Command** -Objekt ausführen. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="236a1-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="236a1-p101">Wenn Sie die [Refresh](refresh-method-ado.md)-Methode verwenden, um Parameterinformationen vom Anbieter zu erhalten, und ein oder mehrere **Parameter** -Objekte mit einem Datentyp variabler Länge zurückgegeben werden, reserviert ADO möglicherweise Speicher entsprechend der maximal möglichen Größe der Parameter. Das kann einen Fehler während der Ausführung verursachen. Damit kein Fehler auftritt, sollten Sie die **Size** -Eigenschaft für diese Parameter explizit festlegen, bevor Sie den Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="236a1-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="236a1-113">Die **Size** -Eigenschaft ist nicht schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="236a1-113">The **Size** property is read/write.</span></span>


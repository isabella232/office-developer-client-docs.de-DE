---
title: MaxRecords-Eigenschaft (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870086"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="59d9b-102">MaxRecords-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="59d9b-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="59d9b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59d9b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59d9b-104">Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="59d9b-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="59d9b-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="59d9b-105">Settings and return values</span></span>

<span data-ttu-id="59d9b-p101">Legt einen Long-Wert fest, der die maximale Anzahl von zurückgegebenen Datensätzen angibt, oder gibt den Wert zurück. Der Standardwert ist Null (kein Limit).</span><span class="sxs-lookup"><span data-stu-id="59d9b-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="59d9b-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="59d9b-108">Remarks</span></span>

<span data-ttu-id="59d9b-109">Verwenden Sie die **MaxRecords** -Eigenschaft zur Begrenzung der Anzahl von Datensätzen, die der Anbieter aus der Datenquelle zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="59d9b-109">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source.</span></span> <span data-ttu-id="59d9b-110">Die Standardeinstellung dieser Eigenschaft ist NULL und bedeutet, dass der Anbieter alle angeforderten Datensätze zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="59d9b-110">The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="59d9b-111">Die **MaxRecords** -Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset** -Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="59d9b-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>


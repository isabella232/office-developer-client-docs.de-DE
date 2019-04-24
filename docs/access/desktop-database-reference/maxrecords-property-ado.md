---
title: MaxRecords-Eigenschaft (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ed643ca3b1341d7f933901e15c20c84acb025f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289721"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="d9b7a-102">MaxRecords-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="d9b7a-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="d9b7a-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9b7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d9b7a-104">Gibt die maximale Anzahl von Datensätzen an, die von einer Abfrage an ein [Recordset](recordset-object-ado.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d9b7a-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d9b7a-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d9b7a-105">Settings and return values</span></span>

<span data-ttu-id="d9b7a-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span><span class="sxs-lookup"><span data-stu-id="d9b7a-106">Sets or returns a **Long** value that indicates the maximum number of records to return.</span></span> <span data-ttu-id="d9b7a-107">Default is zero (no limit).</span><span class="sxs-lookup"><span data-stu-id="d9b7a-107">Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="d9b7a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9b7a-108">Remarks</span></span>

<span data-ttu-id="d9b7a-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span><span class="sxs-lookup"><span data-stu-id="d9b7a-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="d9b7a-111">Die **MaxRecords**-Eigenschaft ist nicht schreibgeschützt, wenn das **Recordset**-Objekt geschlossen ist, und schreibgeschützt, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9b7a-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>


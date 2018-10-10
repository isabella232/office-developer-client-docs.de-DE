---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475521"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="9306f-102">ActiveCommand-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9306f-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="9306f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9306f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9306f-104">Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9306f-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9306f-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9306f-105">Return Value</span></span>

<span data-ttu-id="9306f-p101">Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command** -Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.</span><span class="sxs-lookup"><span data-stu-id="9306f-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="9306f-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9306f-108">Remarks</span></span>

<span data-ttu-id="9306f-109">Die **ActiveCommand** -Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9306f-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="9306f-110">Wenn kein **Command** -Objekt zum Erstellen des aktuellen **Recordset** -Objekts verwendet wurde, wird ein **NULL** -Objektverweis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9306f-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="9306f-111">Suchen Sie mit dieser Eigenschaft das zugeordnete **Command** -Objekt, wenn nur das resultierende **Recordset** -Objekt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9306f-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>


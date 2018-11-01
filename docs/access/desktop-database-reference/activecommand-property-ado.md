---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869561"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="124fe-102">ActiveCommand-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="124fe-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="124fe-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="124fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="124fe-104">Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="124fe-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="124fe-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="124fe-105">Return value</span></span>

<span data-ttu-id="124fe-p101">Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command** -Objekt enthält. Der Standard ist ein nullwertiger Objektverweis.</span><span class="sxs-lookup"><span data-stu-id="124fe-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="124fe-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="124fe-108">Remarks</span></span>

<span data-ttu-id="124fe-109">Die **ActiveCommand** -Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="124fe-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="124fe-110">Wenn ein **Command** -Objekt zum Erstellen des aktuellen **Recordset-Objekt**nicht verwendet wurde, wird ein **Null** -Objektverweis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="124fe-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="124fe-111">Suchen Sie mit dieser Eigenschaft das zugeordnete **Command** -Objekt, wenn nur das resultierende **Recordset** -Objekt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="124fe-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>


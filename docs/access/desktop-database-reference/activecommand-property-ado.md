---
title: ActiveCommand-Eigenschaft (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281929"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="9eb17-102">ActiveCommand-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="9eb17-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="9eb17-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9eb17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9eb17-104">Gibt das [Command](command-object-ado.md)-Objekt an, mit dem das zugeordnete [Recordset](recordset-object-ado.md)-Objekt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9eb17-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="9eb17-105">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eb17-105">Return value</span></span>

<span data-ttu-id="9eb17-106">Gibt einen Wert vom Datentyp **Variant** zurück, der ein **Command**-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="9eb17-106">Returns a **Variant** that contains a **Command** object.</span></span> <span data-ttu-id="9eb17-107">Der Standard ist ein nullwertiger Objektverweis.</span><span class="sxs-lookup"><span data-stu-id="9eb17-107">Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb17-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eb17-108">Remarks</span></span>

<span data-ttu-id="9eb17-109">Die **ActiveCommand**-Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9eb17-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="9eb17-110">Wenn kein **Command** -Objekt zum Erstellen des aktuellen **Recordset**-Objekts verwendet wurde, wird ein **null** -Objektverweis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9eb17-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="9eb17-111">Suchen Sie mit dieser Eigenschaft das zugeordnete **Command**-Objekt, wenn nur das resultierende **Recordset**-Objekt angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9eb17-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>


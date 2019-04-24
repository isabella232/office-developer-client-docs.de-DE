---
title: State-Eigenschaft (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308533"
---
# <a name="state-property-ado"></a><span data-ttu-id="14975-102">State-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="14975-102">State property (ADO)</span></span>


<span data-ttu-id="14975-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14975-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14975-104">Für alle entsprechenden Objekte wird angegeben, ob der Status des Objekts open oder closed entspricht.</span><span class="sxs-lookup"><span data-stu-id="14975-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="14975-105">Für alle entsprechenden Objekte, durch die eine asynchrone Methode ausgeführt wird, wird angegeben, ob der aktuelle Status des Objekts connecting, executing oder retrieving entspricht.</span><span class="sxs-lookup"><span data-stu-id="14975-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="14975-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14975-106">Return value</span></span>

<span data-ttu-id="14975-107">Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann.</span><span class="sxs-lookup"><span data-stu-id="14975-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="14975-108">Der Standardwert ist **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="14975-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="14975-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14975-109">Remarks</span></span>

<span data-ttu-id="14975-110">Mit der **State**-Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.</span><span class="sxs-lookup"><span data-stu-id="14975-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="14975-p102">Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="14975-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="14975-113">Die **State** -Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="14975-113">The **State** property is read-only.</span></span>


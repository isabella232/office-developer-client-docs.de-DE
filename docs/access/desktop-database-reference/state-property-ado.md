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
ms.openlocfilehash: d8ea3738465ed9bfc10cbabdf355036f7c160f66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886613"
---
# <a name="state-property-ado"></a><span data-ttu-id="56847-102">State-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="56847-102">State property (ADO)</span></span>


<span data-ttu-id="56847-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="56847-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="56847-104">Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.</span><span class="sxs-lookup"><span data-stu-id="56847-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="56847-105">Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).</span><span class="sxs-lookup"><span data-stu-id="56847-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="56847-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56847-106">Return value</span></span>

<span data-ttu-id="56847-p101">Gibt einen **Long** -Wert zurück, bei dem es sich um einen [ObjectStateEnum](objectstateenum.md)-Wert handeln kann. Der Standardwert ist **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="56847-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="56847-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56847-109">Remarks</span></span>

<span data-ttu-id="56847-110">Mit der **State** -Eigenschaft können Sie jederzeit den aktuellen Status eines bestimmten Objekts ermitteln.</span><span class="sxs-lookup"><span data-stu-id="56847-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="56847-p102">Die **State** -Eigenschaft des Objekts kann kombinierte Werte besitzen. Wenn beispielsweise eine Anweisung ausgeführt wird, besitzt die Eigenschaft einen aus **adStateOpen** und **adStateExecuting** bestehenden kombinierten Wert.</span><span class="sxs-lookup"><span data-stu-id="56847-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="56847-113">Die **State** -Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="56847-113">The **State** property is read-only.</span></span>


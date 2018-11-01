---
title: Recordset2.StillExecuting Property (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 702c4772afa6bb8b1011a04d6ac3d3bf4a970c90
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881118"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="12775-102">Recordset2.StillExecuting Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="12775-102">Recordset2.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="12775-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12775-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="12775-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12775-104">Syntax</span></span>

<span data-ttu-id="12775-105">*Ausdruck* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="12775-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="12775-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="12775-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="12775-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12775-107">Remarks</span></span>

<span data-ttu-id="12775-p101">Mit der **StillExecuting**-Eigenschaft können Sie feststellen, ob die zuletzt aufgerufene asynchrone **Execute**- oder **OpenConnection**-Methode (d. h. eine Methode, die mit der **dbRunAsync**-Option aufgerufen wurde) abgeschlossen wurde. Solange die **StillExecuting**-Eigenschaft **True** ist, kann nicht auf zurückgegebene Objekte zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="12775-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="12775-p102">Wenn die **StillExecuting**-Eigenschaft im Anschluss an den **OpenConnection**-Aufruf, der das zugeordnete **Connection**-Objekt zurückgibt, **False** zurückgibt, kann auf das Objekt verwiesen werden. Solange **StillExecuting** noch **True** ist, kann nicht auf das Objekt verwiesen werden. Die **StillExecuting**-Eigenschaft kann in diesem Fall nur gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="12775-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="12775-112">Mit der **[Cancel](connection-cancel-method-dao.md)** -Methode können Sie die Ausführung einer Aufgabe beenden.</span><span class="sxs-lookup"><span data-stu-id="12775-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>


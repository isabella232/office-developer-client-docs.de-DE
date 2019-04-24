---
title: Recordset2. StillExecuting-Eigenschaft (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa94622374990ce48c857e9ad45c3531975bb9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307217"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="299b4-102">Recordset2. StillExecuting-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="299b4-102">Recordset2.StillExecuting property (DAO)</span></span>


<span data-ttu-id="299b4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="299b4-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="299b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="299b4-104">Syntax</span></span>

<span data-ttu-id="299b4-105">*Ausdruck* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="299b4-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="299b4-106">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="299b4-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="299b4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="299b4-107">Remarks</span></span>

<span data-ttu-id="299b4-p101">Mit der **StillExecuting**-Eigenschaft können Sie feststellen, ob die zuletzt aufgerufene asynchrone **Execute**- oder **OpenConnection**-Methode (d. h. eine Methode, die mit der **dbRunAsync**-Option aufgerufen wurde) abgeschlossen wurde. Solange die **StillExecuting**-Eigenschaft **True** ist, kann nicht auf zurückgegebene Objekte zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="299b4-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="299b4-p102">Wenn die **StillExecuting**-Eigenschaft im Anschluss an den **OpenConnection**-Aufruf, der das zugeordnete **Connection**-Objekt zurückgibt, **False** zurückgibt, kann auf das Objekt verwiesen werden. Solange **StillExecuting** noch **True** ist, kann nicht auf das Objekt verwiesen werden. Die **StillExecuting**-Eigenschaft kann in diesem Fall nur gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="299b4-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="299b4-112">Mit der **[Cancel](connection-cancel-method-dao.md)** -Methode können Sie die Ausführung einer Aufgabe beenden.</span><span class="sxs-lookup"><span data-stu-id="299b4-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>


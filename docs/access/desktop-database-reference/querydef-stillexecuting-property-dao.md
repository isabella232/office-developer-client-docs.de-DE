---
title: QueryDef. StillExecuting-Eigenschaft (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 98e85d37-de50-afe1-dcca-01623546e0ad
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197953(v=office.15)
ms:contentKeyID: 48546505
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053584
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 60c0663eaa6857801555c6ce05f4256cfe4c290f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303416"
---
# <a name="querydefstillexecuting-property-dao"></a><span data-ttu-id="1ec0e-102">QueryDef. StillExecuting-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1ec0e-102">QueryDef.StillExecuting property (DAO)</span></span>


<span data-ttu-id="1ec0e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ec0e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec0e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ec0e-104">Syntax</span></span>

<span data-ttu-id="1ec0e-105">*Ausdruck* . StillExecuting</span><span class="sxs-lookup"><span data-stu-id="1ec0e-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="1ec0e-106">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1ec0e-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec0e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ec0e-107">Remarks</span></span>

<span data-ttu-id="1ec0e-p101">Mit der **StillExecuting**-Eigenschaft können Sie feststellen, ob die zuletzt aufgerufene asynchrone **[Execute](querydef-execute-method-dao.md)** - oder **[OpenConnection](dbengine-openconnection-method-dao.md)** -Methode (d. h. eine Methode, die mit der **dbRunAsync**-Option aufgerufen wurde) abgeschlossen wurde. Solange die **StillExecuting**-Eigenschaft **True** ist, kann nicht auf zurückgegebene Objekte zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="1ec0e-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **[Execute](querydef-execute-method-dao.md)** or **[OpenConnection](dbengine-openconnection-method-dao.md)** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="1ec0e-p102">Wenn die **StillExecuting**-Eigenschaft im Anschluss an den **OpenConnection**-Aufruf, der das zugeordnete [**Connection**](connection-object-dao.md) -Objekt zurückgibt, den Wert **False** zurückgibt, kann auf das Objekt verwiesen werden. Solange **StillExecuting** noch **True** ist, kann nicht auf das Objekt verwiesen werden. Die **StillExecuting**-Eigenschaft kann in diesem Fall nur gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="1ec0e-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **[Connection](connection-object-dao.md)** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="1ec0e-112">Mit der **[Cancel](connection-cancel-method-dao.md)** -Methode können Sie die Ausführung einer Aufgabe beenden.</span><span class="sxs-lookup"><span data-stu-id="1ec0e-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>


---
title: Recordset2.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5df46c36ff28bae1e48dfc8dc77443f707fc3e0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877534"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="2f44c-102">Recordset2.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f44c-102">Recordset2.Cancel Method (DAO)</span></span>


<span data-ttu-id="2f44c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f44c-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="2f44c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f44c-104">Syntax</span></span>

<span data-ttu-id="2f44c-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="2f44c-105">*expression* .Cancel</span></span>

<span data-ttu-id="2f44c-106">*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2f44c-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f44c-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f44c-107">Remarks</span></span>

<span data-ttu-id="2f44c-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="2f44c-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="2f44c-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="2f44c-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


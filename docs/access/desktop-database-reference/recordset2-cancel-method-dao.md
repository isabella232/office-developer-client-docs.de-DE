---
title: Recordset2. Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d203d1f1888539a4907da246e20ed711e61ee51f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307413"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="fe23d-102">Recordset2. Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe23d-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="fe23d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe23d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="fe23d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe23d-104">Syntax</span></span>

<span data-ttu-id="fe23d-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="fe23d-105">*expression* .Cancel</span></span>

<span data-ttu-id="fe23d-106">*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fe23d-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe23d-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe23d-107">Remarks</span></span>

<span data-ttu-id="fe23d-108">Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute** -oder OpenConnection-Methodenaufrufs zu beenden (das heißt, die Methode wurde mit der dbRunAsync-Option aufgerufen). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="fe23d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="fe23d-109">**Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fe23d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


---
title: QueryDef. Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 56a4ba804dba25eb0b4722bcf5396229ee003f43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301120"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="c0008-102">QueryDef. Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c0008-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="c0008-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c0008-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c0008-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0008-104">Syntax</span></span>

<span data-ttu-id="c0008-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="c0008-105">*expression* .Cancel</span></span>

<span data-ttu-id="c0008-106">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c0008-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0008-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0008-107">Remarks</span></span>

<span data-ttu-id="c0008-108">Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute** -oder OpenConnection-Methodenaufrufs zu beenden (das heißt, die Methode wurde mit der dbRunAsync-Option aufgerufen). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0008-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c0008-109">**Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c0008-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


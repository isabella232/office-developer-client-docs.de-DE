---
title: Recordset. Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300812"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="5592e-102">Recordset. Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="5592e-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="5592e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5592e-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="5592e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5592e-104">Syntax</span></span>

<span data-ttu-id="5592e-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="5592e-105">*expression* .Cancel</span></span>

<span data-ttu-id="5592e-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5592e-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5592e-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5592e-107">Remarks</span></span>

<span data-ttu-id="5592e-108">Verwenden Sie die **Cancel** -Methode, um die Ausführung eines asynchronen **Execute** -oder OpenConnection-Methodenaufrufs zu beenden (das heißt, die Methode wurde mit der dbRunAsync-Option aufgerufen). \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5592e-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="5592e-109">**Cancel** gibt einen Laufzeitfehler zurück, wenn dbRunAsync nicht in der Methode verwendet wurde, die Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="5592e-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


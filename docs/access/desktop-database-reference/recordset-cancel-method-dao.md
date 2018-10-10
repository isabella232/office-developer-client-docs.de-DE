---
title: Recordset.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1d7e77bd844385b9400449027312dacc02940e58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473358"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="6a1b9-102">Recordset.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="6a1b9-102">Recordset.Cancel Method (DAO)</span></span>


<span data-ttu-id="6a1b9-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a1b9-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="6a1b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a1b9-104">Syntax</span></span>

<span data-ttu-id="6a1b9-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="6a1b9-105">*expression* .Cancel</span></span>

<span data-ttu-id="6a1b9-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a1b9-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a1b9-107">Remarks</span></span>

<span data-ttu-id="6a1b9-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="6a1b9-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="6a1b9-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="6a1b9-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


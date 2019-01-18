---
title: Recordset.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716712"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="14ed0-102">Recordset.Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="14ed0-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="14ed0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14ed0-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="14ed0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ed0-104">Syntax</span></span>

<span data-ttu-id="14ed0-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="14ed0-105">*expression* .Cancel</span></span>

<span data-ttu-id="14ed0-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ed0-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ed0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14ed0-107">Remarks</span></span>

<span data-ttu-id="14ed0-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="14ed0-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="14ed0-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="14ed0-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


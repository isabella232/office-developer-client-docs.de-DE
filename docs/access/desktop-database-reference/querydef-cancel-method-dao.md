---
title: QueryDef.Cancel-Methode (DAO)
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
ms.openlocfilehash: ab28f1b976144c40eb8be639bb7c7a1adc3e4450
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920228"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="a5c1d-102">QueryDef.Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5c1d-102">QueryDef.Cancel method (DAO)</span></span>


<span data-ttu-id="a5c1d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5c1d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5c1d-104">Syntax</span></span>

<span data-ttu-id="a5c1d-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="a5c1d-105">*expression* .Cancel</span></span>

<span data-ttu-id="a5c1d-106">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a5c1d-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5c1d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5c1d-107">Remarks</span></span>

<span data-ttu-id="a5c1d-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="a5c1d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="a5c1d-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a5c1d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


---
title: Recordset2.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 159f476b592a8c944df2dc4570d84377c89b5043
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929231"
---
# <a name="recordset2cancel-method-dao"></a><span data-ttu-id="c606d-102">Recordset2.Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="c606d-102">Recordset2.Cancel method (DAO)</span></span>


<span data-ttu-id="c606d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c606d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c606d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c606d-104">Syntax</span></span>

<span data-ttu-id="c606d-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="c606d-105">*expression* .Cancel</span></span>

<span data-ttu-id="c606d-106">*Ausdruck* Ein Ausdruck, der ein **Recordset2** -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="c606d-106">*expression* An expression that returns a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c606d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c606d-107">Remarks</span></span>

<span data-ttu-id="c606d-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="c606d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c606d-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c606d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


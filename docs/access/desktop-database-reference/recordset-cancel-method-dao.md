---
title: Recordset.Cancel-Methode (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81b08472b46ab3a3d35d184e2f8b7be8673f7d1f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927263"
---
# <a name="recordsetcancel-method-dao"></a><span data-ttu-id="8f53d-102">Recordset.Cancel-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="8f53d-102">Recordset.Cancel method (DAO)</span></span>


<span data-ttu-id="8f53d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8f53d-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="8f53d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f53d-104">Syntax</span></span>

<span data-ttu-id="8f53d-105">*Ausdruck* . Abbrechen</span><span class="sxs-lookup"><span data-stu-id="8f53d-105">*expression* .Cancel</span></span>

<span data-ttu-id="8f53d-106">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8f53d-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f53d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8f53d-107">Remarks</span></span>

<span data-ttu-id="8f53d-108">Verwenden die **Abbrechen** -Methode, um die Ausführung eines asynchronen Aufrufs von **Execute-** oder **OpenConnection** -Methode beendet werden (d. h., die Methode mit der Option DbRunAsync aufgerufen wurde).</span><span class="sxs-lookup"><span data-stu-id="8f53d-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="8f53d-109">**Abbrechen** gibt einen Laufzeitfehler zurück, wenn DbRunAsync nicht in der-Methode verwendet wurde, den Sie beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8f53d-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>


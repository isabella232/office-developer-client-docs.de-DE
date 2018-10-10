---
title: State-Eigenschaft (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a42ade39a50eb5dc40e213d6f4c3f4ed0ba3475e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474123"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="8122b-102">State-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8122b-102">State Property (ADO MD)</span></span>


<span data-ttu-id="8122b-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8122b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8122b-104">Gibt den aktuellen Status der Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="8122b-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="8122b-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8122b-105">Return Values</span></span>

<span data-ttu-id="8122b-p101">Gibt einen ganzzahligen, schreibgeschützten **Long** -Wert zurück, der den aktuellen Status des [Cellset](cellset-object-ado-md.md)-Objekts angibt. Die folgenden Werte sind gültig: **adStateClosed** (0) und **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="8122b-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="8122b-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8122b-108">Remarks</span></span>

<span data-ttu-id="8122b-p102">Verweisen Sie in dem Projekt auf die ADO-Typbibliothek verweisen, um die [ObjectStateEnum](objectstateenum.md)-Konstantennamen zu verwenden. Weitere Informationen hierzu finden Sie unter [Verwenden von ADO mit ADO MD](using-ado-with-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8122b-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>


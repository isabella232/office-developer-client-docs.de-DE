---
title: State-Eigenschaft (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 33933fb71ee3d7541640469eebc650c0f52a9784
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922013"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="11eef-102">State-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="11eef-102">State property (ADO MD)</span></span>


<span data-ttu-id="11eef-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11eef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11eef-104">Gibt den aktuellen Status der Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="11eef-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="11eef-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="11eef-105">Return values</span></span>

<span data-ttu-id="11eef-p101">Gibt einen ganzzahligen, schreibgeschützten **Long** -Wert zurück, der den aktuellen Status des [Cellset](cellset-object-ado-md.md)-Objekts angibt. Die folgenden Werte sind gültig: **adStateClosed** (0) und **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="11eef-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="11eef-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11eef-108">Remarks</span></span>

<span data-ttu-id="11eef-p102">Verweisen Sie in dem Projekt auf die ADO-Typbibliothek verweisen, um die [ObjectStateEnum](objectstateenum.md)-Konstantennamen zu verwenden. Weitere Informationen hierzu finden Sie unter [Verwenden von ADO mit ADO MD](using-ado-with-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="11eef-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>


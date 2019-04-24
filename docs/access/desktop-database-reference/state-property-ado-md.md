---
title: State-Eigenschaft (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306363"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="b3944-102">State-Eigenschaft (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="b3944-102">State property (ADO MD)</span></span>


<span data-ttu-id="b3944-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3944-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b3944-104">Gibt den aktuellen Status der Zellmenge an.</span><span class="sxs-lookup"><span data-stu-id="b3944-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="b3944-105">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b3944-105">Return values</span></span>

<span data-ttu-id="b3944-106">Gibt einen ganzzahligen, schreibgeschützten **Long**-Wert zurück, der den aktuellen Status des [Cellset](cellset-object-ado-md.md)-Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="b3944-106">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only.</span></span> <span data-ttu-id="b3944-107">Die folgenden Werte sind gültig: **adStateClosed** (0) und **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="b3944-107">The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3944-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3944-108">Remarks</span></span>

<span data-ttu-id="b3944-p102">Verweisen Sie in dem Projekt auf die ADO-Typbibliothek verweisen, um die [ObjectStateEnum](objectstateenum.md)-Konstantennamen zu verwenden. Weitere Informationen hierzu finden Sie unter [Verwenden von ADO mit ADO MD](using-ado-with-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="b3944-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>


---
title: TableDef. RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5eb9588927c9e35fea54964f16150735a7374cd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314287"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="1dd87-102">TableDef. RecordCount-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1dd87-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="1dd87-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1dd87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1dd87-104">Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="1dd87-104">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="1dd87-105">Schreibgeschützter **Long**-Wert.</span><span class="sxs-lookup"><span data-stu-id="1dd87-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd87-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dd87-106">Syntax</span></span>

<span data-ttu-id="1dd87-107">*Ausdruck* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="1dd87-107">*expression* .RecordCount</span></span>

<span data-ttu-id="1dd87-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1dd87-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd87-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd87-109">Remarks</span></span>

<span data-ttu-id="1dd87-110">Ein **Recordset**- oder **TableDef**-Objekt ohne Datensätze hat eine **RecordCount**-Eigenschaftseinstellung von "0".</span><span class="sxs-lookup"><span data-stu-id="1dd87-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="1dd87-111">Wenn Sie verknüpfte**TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.</span><span class="sxs-lookup"><span data-stu-id="1dd87-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>


---
title: TableDef.RecordCount-Eigenschaft (DAO)
TOCTitle: RecordCount Property
ms:assetid: f8804244-0134-fc1f-1f5f-4971afe17974
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836946(v=office.15)
ms:contentKeyID: 48548783
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b24aaa5aec9b17adc169c67733a19a9077a4930
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920921"
---
# <a name="tabledefrecordcount-property-dao"></a><span data-ttu-id="e8922-102">TableDef.RecordCount-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8922-102">TableDef.RecordCount property (DAO)</span></span>


<span data-ttu-id="e8922-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8922-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8922-p101">Gibt die Gesamtzahl der Datensätze in einem **[TableDef](tabledef-object-dao.md)** -Objekt zurück. Schreibgeschützter **Long**-Wert.</span><span class="sxs-lookup"><span data-stu-id="e8922-p101">Returns the total number of records in a **[TableDef](tabledef-object-dao.md)** object. Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8922-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8922-106">Syntax</span></span>

<span data-ttu-id="e8922-107">*Ausdruck* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="e8922-107">*expression* .RecordCount</span></span>

<span data-ttu-id="e8922-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8922-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8922-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8922-109">Remarks</span></span>

<span data-ttu-id="e8922-110">Die **RecordCount**-Eigenschaft eines **Recordset**- oder **TableDef**-Objekts ohne Datensätze hat den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="e8922-110">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="e8922-111">Wenn Sie verknüpfte**TableDef**-Objekte verwenden, ist der Wert der **RecordCount**-Eigenschaft immer –1.</span><span class="sxs-lookup"><span data-stu-id="e8922-111">When you work with linked**TableDef** objects, the **RecordCount** property setting is always –1.</span></span>


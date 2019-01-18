---
title: Property.Value-Eigenschaft (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713380"
---
# <a name="propertyvalue-property-dao"></a><span data-ttu-id="91e27-102">Property.Value-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="91e27-102">Property.Value property (DAO)</span></span>

<span data-ttu-id="91e27-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91e27-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91e27-p101">Legt den Wert eines Objekts fest oder gibt ihn zurück. **Variant**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="91e27-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="91e27-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91e27-106">Syntax</span></span>

<span data-ttu-id="91e27-107">*Ausdruck* . Wert</span><span class="sxs-lookup"><span data-stu-id="91e27-107">*expression* .Value</span></span>

<span data-ttu-id="91e27-108">*Ausdruck* Eine Variable, die ein **Property-** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="91e27-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91e27-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91e27-109">Remarks</span></span>

<span data-ttu-id="91e27-110">Die Einstellung eines Rückgabewerts ist ein Variant-Datentyp, der als für den Datentyp geeigneter Wert ausgewertet wird, wie in der Type-Eigenschaft des Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="91e27-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="91e27-111">Im Allgemeinen wird die **Value**-Eigenschaft verwendet, um Daten in **Recordset**-Objekten abzufragen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="91e27-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="91e27-p102">Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field**, **Parameter** und **Property**. Aus diesem Grund können Sie den Wert dieser Objekte direkt festlegen oder zurückgeben, ohne die **Value**-Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="91e27-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="91e27-114">Der Versuch, die **Value**-Eigenschaft in einem unzulässigen Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), verursacht einen auffangbaren Fehler.</span><span class="sxs-lookup"><span data-stu-id="91e27-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>

> [!NOTE]
> <span data-ttu-id="91e27-115">Beim Lesen von Dezimalwerten aus einer Microsoft SQL Server-Datenbank werden die Werte im Microsoft Access-Arbeitsbereich in wissenschaftlicher Schreibweise formatiert. Im ODBCDirect-Arbeitsbereich werden sie dagegen als normale Dezimalwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91e27-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>



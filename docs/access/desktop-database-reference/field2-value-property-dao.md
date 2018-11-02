---
title: Field2.Value-Eigenschaft (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec1bdab14743a43bc4abda029e5f77ec1a8e6212
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925149"
---
# <a name="field2value-property-dao"></a><span data-ttu-id="6c75d-102">Field2.Value-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c75d-102">Field2.Value property (DAO)</span></span>


<span data-ttu-id="6c75d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c75d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c75d-p101">Legt den Wert eines Objekts fest oder gibt ihn zurück. **Variant**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6c75d-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c75d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c75d-106">Syntax</span></span>

<span data-ttu-id="6c75d-107">*Ausdruck* . Wert</span><span class="sxs-lookup"><span data-stu-id="6c75d-107">*expression* .Value</span></span>

<span data-ttu-id="6c75d-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c75d-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c75d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c75d-109">Remarks</span></span>

<span data-ttu-id="6c75d-110">Die Einstellung eines Rückgabewerts ist ein Variant-Datentyp, der als für den Datentyp geeigneter Wert ausgewertet wird, wie in der Type-Eigenschaft des Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="6c75d-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="6c75d-111">In der Regel werden mit der **Value**-Eigenschaft Daten in **Recordset**-Objekten abgerufen und geändert.</span><span class="sxs-lookup"><span data-stu-id="6c75d-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="6c75d-p102">Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field2**, **Parameter** und **Property**. Sie können deshalb den Wert dieser Objekte festlegen oder zurückgeben, indem Sie direkt auf das Objekt verweisen, anstatt die **Value**-Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6c75d-p102">The **Value** property is the default property of the **Field2**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="6c75d-114">Wenn Sie versuchen, die **Value**-Eigenschaft in einem ungeeigneten Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field2**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="6c75d-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field2** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="6c75d-115">Dezimale Werte werden beim Lesen aus einer Microsoft SQL Server-Datenbank in einem Microsoft Access-Arbeitsbereich mit einer wissenschaftlichen Schreibweise formatiert, in einem ODBCDirect-Arbeitsbereich werden sie jedoch als normale Dezimalwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c75d-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>



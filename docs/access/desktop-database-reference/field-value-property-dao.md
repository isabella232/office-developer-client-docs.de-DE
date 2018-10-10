---
title: Field.Value Property (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 946ce8ec4219229e047d1bef5c3ff6de403eb7c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473455"
---
# <a name="fieldvalue-property-dao"></a><span data-ttu-id="aaeff-102">Field.Value Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="aaeff-102">Field.Value Property (DAO)</span></span>


<span data-ttu-id="aaeff-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aaeff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aaeff-p101">Legt den Wert eines Objekts fest oder gibt ihn zurück. **Variant**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="aaeff-p101">Sets or returns the value of an object. Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaeff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="aaeff-106">Syntax</span></span>

<span data-ttu-id="aaeff-107">*Ausdruck* . Wert</span><span class="sxs-lookup"><span data-stu-id="aaeff-107">*expression* .Value</span></span>

<span data-ttu-id="aaeff-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="aaeff-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aaeff-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aaeff-109">Remarks</span></span>

<span data-ttu-id="aaeff-110">Die Einstellung eines Rückgabewerts ist ein Variant-Datentyp, der als für den Datentyp geeigneter Wert ausgewertet wird, wie in der Type-Eigenschaft des Objekts angegeben.</span><span class="sxs-lookup"><span data-stu-id="aaeff-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="aaeff-111">Im Allgemeinen wird die **Value**-Eigenschaft verwendet, um Daten in **Recordset**-Objekten abzufragen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="aaeff-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="aaeff-p102">Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field**, **Parameter** und **Property**. Aus diesem Grund können Sie den Wert dieser Objekte direkt festlegen oder zurückgeben, ohne die **Value**-Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="aaeff-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="aaeff-114">Der Versuch, die **Value**-Eigenschaft in einem unzulässigen Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), verursacht einen auffangbaren Fehler.</span><span class="sxs-lookup"><span data-stu-id="aaeff-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aaeff-115">Beim Lesen von Dezimalwerten aus einer Microsoft SQL Server-Datenbank werden die Werte im Microsoft Access-Arbeitsbereich in wissenschaftlicher Schreibweise formatiert. Im ODBCDirect-Arbeitsbereich werden sie dagegen als normale Dezimalwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aaeff-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span></P>



---
title: Field. Value-Eigenschaft (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9b51bb4e08546531f95e3795074f90b5d94d4c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292923"
---
# <a name="fieldvalue-property-dao"></a><span data-ttu-id="1098f-102">Field. Value-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="1098f-102">Field.Value property (DAO)</span></span>


<span data-ttu-id="1098f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1098f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1098f-104">Legt den Wert eines Objekts fest oder gibt ihn zurück.</span><span class="sxs-lookup"><span data-stu-id="1098f-104">Sets or returns the value of an object.</span></span> <span data-ttu-id="1098f-105">**Variant** mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1098f-105">Read/write **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1098f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1098f-106">Syntax</span></span>

<span data-ttu-id="1098f-107">*Ausdruck* . Wert</span><span class="sxs-lookup"><span data-stu-id="1098f-107">*expression* .Value</span></span>

<span data-ttu-id="1098f-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1098f-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1098f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1098f-109">Remarks</span></span>

<span data-ttu-id="1098f-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span><span class="sxs-lookup"><span data-stu-id="1098f-110">The setting or return value is a Variant data type that evaluates to a value appropriate for the data type, as specified by the **Type** property of an object.</span></span>

<span data-ttu-id="1098f-111">Im Allgemeinen wird die **Value**-Eigenschaft verwendet, um Daten in **Recordset**-Objekten abzufragen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1098f-111">Generally, the **Value** property is used to retrieve and alter data in **Recordset** objects.</span></span>

<span data-ttu-id="1098f-p102">Die **Value**-Eigenschaft ist die Standardeigenschaft der Objekte **Field**, **Parameter** und **Property**. Aus diesem Grund können Sie den Wert dieser Objekte direkt festlegen oder zurückgeben, ohne die **Value**-Eigenschaft anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1098f-p102">The **Value** property is the default property of the **Field**, **Parameter**, and **Property** objects. Therefore, you can set or return the value of one of these objects by referring to them directly instead of specifying the **Value** property.</span></span>

<span data-ttu-id="1098f-114">Der Versuch, die **Value**-Eigenschaft in einem unzulässigen Kontext festzulegen oder zurückzugeben (z. B. die **Value**-Eigenschaft eines **Field**-Objekts in der **Fields**-Auflistung eines **TableDef**-Objekts), verursacht einen auffangbaren Fehler.</span><span class="sxs-lookup"><span data-stu-id="1098f-114">Trying to set or return the **Value** property in an inappropriate context (for example, the **Value** property of a **Field** object in the **Fields** collection of a **TableDef** object) will cause a trappable error.</span></span>


> [!NOTE]
> <span data-ttu-id="1098f-115">Beim Lesen von Dezimalwerten aus einer Microsoft SQL Server-Datenbank werden die Werte im Microsoft Access-Arbeitsbereich in wissenschaftlicher Schreibweise formatiert. Im ODBCDirect-Arbeitsbereich werden sie dagegen als normale Dezimalwerte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1098f-115">When reading decimal values from a Microsoft SQL Server database, they will be formatted using scientific notation through a Microsoft Access workspace, but will appear as normal decimal values through an ODBCDirect workspace.</span></span>



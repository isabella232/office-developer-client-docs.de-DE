---
title: GetString-Methode (ADO)
TOCTitle: GetString Method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba235094aa7f491cbd86bf753713d50f01009d47
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605401"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="20ba2-102">GetString-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="20ba2-102">GetString Method (ADO)</span></span>


<span data-ttu-id="20ba2-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="20ba2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="20ba2-104">Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="20ba2-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="20ba2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20ba2-105">Syntax</span></span>

<span data-ttu-id="20ba2-106">*Variant* = *Recordset-Objekt*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="20ba2-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

<span data-ttu-id="20ba2-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="20ba2-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="20ba2-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20ba2-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="20ba2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20ba2-109">Return value</span></span>
>>>>>>> <span data-ttu-id="20ba2-110">master</span><span class="sxs-lookup"><span data-stu-id="20ba2-110">master</span></span>

<span data-ttu-id="20ba2-111">Gibt das **Recordset** -Objekt als eine **Variant** -Variable (BSTR) mit Zeichenfolgenwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="20ba2-111">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="20ba2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20ba2-112">Parameters</span></span>

  - <span data-ttu-id="20ba2-113">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="20ba2-113">*StringFormat*</span></span>

  - <span data-ttu-id="20ba2-p101">Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.</span><span class="sxs-lookup"><span data-stu-id="20ba2-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="20ba2-116">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="20ba2-116">*NumRows*</span></span>

  - <span data-ttu-id="20ba2-117">Optional.</span><span class="sxs-lookup"><span data-stu-id="20ba2-117">Optional.</span></span> <span data-ttu-id="20ba2-118">Die Anzahl von im **Recordset** -Objekt zu konvertierenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="20ba2-118">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="20ba2-119">Wenn *NumRows* nicht angegeben ist oder wenn es größer als die Gesamtzahl der Zeilen im **Recordset-Objekt**ist, werden alle Zeilen in das **Recordset-Objekt** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="20ba2-119">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="20ba2-120">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="20ba2-120">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="20ba2-p103">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.</span><span class="sxs-lookup"><span data-stu-id="20ba2-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="20ba2-123">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="20ba2-123">*RowDelimiter*</span></span>

  - <span data-ttu-id="20ba2-p104">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.</span><span class="sxs-lookup"><span data-stu-id="20ba2-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="20ba2-126">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="20ba2-126">*NullExpr*</span></span>

  - <span data-ttu-id="20ba2-p105">Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="20ba2-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="20ba2-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="20ba2-129">Remarks</span></span>

<span data-ttu-id="20ba2-p106">In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset** -Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="20ba2-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="20ba2-132">Diese Methode entspricht der **GetClipString** -Methode in RDO.</span><span class="sxs-lookup"><span data-stu-id="20ba2-132">This method is equivalent to the RDO **GetClipString** method.</span></span>


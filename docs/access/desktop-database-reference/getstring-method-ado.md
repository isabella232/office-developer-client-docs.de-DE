---
title: GetString-Methode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c6524c52ad3c4821d5b7987415f8a9c2dcb1b1d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919024"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="d2a21-102">GetString-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2a21-102">GetString method (ADO)</span></span>


<span data-ttu-id="d2a21-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2a21-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="d2a21-104">Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="d2a21-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a21-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2a21-105">Syntax</span></span>

<span data-ttu-id="d2a21-106">*Variant* = *Recordset-Objekt*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="d2a21-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="d2a21-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2a21-107">Return value</span></span>

<span data-ttu-id="d2a21-108">Gibt das **Recordset** -Objekt als eine **Variant** -Variable (BSTR) mit Zeichenfolgenwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="d2a21-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="d2a21-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2a21-109">Parameters</span></span>

  - <span data-ttu-id="d2a21-110">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="d2a21-110">*StringFormat*</span></span>

  - <span data-ttu-id="d2a21-p101">Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2a21-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>

  - <span data-ttu-id="d2a21-113">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="d2a21-113">*NumRows*</span></span>

  - <span data-ttu-id="d2a21-114">Optional.</span><span class="sxs-lookup"><span data-stu-id="d2a21-114">Optional.</span></span> <span data-ttu-id="d2a21-115">Die Anzahl von im **Recordset** -Objekt zu konvertierenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d2a21-115">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="d2a21-116">Wenn *NumRows* nicht angegeben ist oder wenn es größer als die Gesamtzahl der Zeilen im **Recordset-Objekt**ist, werden alle Zeilen in das **Recordset-Objekt** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="d2a21-116">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>

  - <span data-ttu-id="d2a21-117">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="d2a21-117">*ColumnDelimiter*</span></span>

  - <span data-ttu-id="d2a21-p103">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.</span><span class="sxs-lookup"><span data-stu-id="d2a21-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>

  - <span data-ttu-id="d2a21-120">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="d2a21-120">*RowDelimiter*</span></span>

  - <span data-ttu-id="d2a21-p104">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.</span><span class="sxs-lookup"><span data-stu-id="d2a21-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>

  - <span data-ttu-id="d2a21-123">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="d2a21-123">*NullExpr*</span></span>

  - <span data-ttu-id="d2a21-p105">Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d2a21-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a21-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d2a21-126">Remarks</span></span>

<span data-ttu-id="d2a21-p106">In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset** -Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="d2a21-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="d2a21-129">Diese Methode entspricht der **GetClipString** -Methode in RDO.</span><span class="sxs-lookup"><span data-stu-id="d2a21-129">This method is equivalent to the RDO **GetClipString** method.</span></span>


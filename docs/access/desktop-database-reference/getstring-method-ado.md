---
title: GetString-Methode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ea28efb8fdeaa0643d1d940419b7650527ddf6e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698211"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="e45ef-102">GetString-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="e45ef-102">GetString method (ADO)</span></span>

<span data-ttu-id="e45ef-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e45ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e45ef-104">Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="e45ef-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e45ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e45ef-105">Syntax</span></span>

<span data-ttu-id="e45ef-106">*Variant* = *Recordset-Objekt*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="e45ef-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="e45ef-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e45ef-107">Return value</span></span>

<span data-ttu-id="e45ef-108">Gibt das **Recordset** -Objekt als eine **Variant** -Variable (BSTR) mit Zeichenfolgenwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="e45ef-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="e45ef-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e45ef-109">Parameters</span></span>

|<span data-ttu-id="e45ef-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e45ef-110">Parameter</span></span>|<span data-ttu-id="e45ef-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e45ef-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e45ef-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="e45ef-112">*StringFormat*</span></span> |<span data-ttu-id="e45ef-p101">Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.</span><span class="sxs-lookup"><span data-stu-id="e45ef-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="e45ef-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="e45ef-115">*NumRows*</span></span> |<span data-ttu-id="e45ef-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="e45ef-116">Optional.</span></span> <span data-ttu-id="e45ef-117">Die Anzahl von im **Recordset** -Objekt zu konvertierenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="e45ef-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="e45ef-118">Wenn *NumRows* nicht angegeben ist oder wenn es größer als die Gesamtzahl der Zeilen im **Recordset-Objekt**ist, werden alle Zeilen in das **Recordset-Objekt** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e45ef-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="e45ef-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="e45ef-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="e45ef-p103">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.</span><span class="sxs-lookup"><span data-stu-id="e45ef-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="e45ef-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="e45ef-122">*RowDelimiter*</span></span> |<span data-ttu-id="e45ef-p104">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.</span><span class="sxs-lookup"><span data-stu-id="e45ef-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="e45ef-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="e45ef-125">*NullExpr*</span></span> |<span data-ttu-id="e45ef-p105">Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e45ef-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e45ef-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e45ef-128">Remarks</span></span>

<span data-ttu-id="e45ef-p106">In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset** -Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="e45ef-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="e45ef-131">Diese Methode entspricht der **GetClipString** -Methode in RDO.</span><span class="sxs-lookup"><span data-stu-id="e45ef-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


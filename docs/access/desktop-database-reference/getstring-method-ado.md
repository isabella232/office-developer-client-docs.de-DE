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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292188"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="ace3d-102">GetString-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ace3d-102">GetString method (ADO)</span></span>

<span data-ttu-id="ace3d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ace3d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ace3d-104">Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="ace3d-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ace3d-105">Syntax</span></span>

<span data-ttu-id="ace3d-106">\*\* = *Recordset*-Datentyp. GetString (*StringFormat*, *numRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="ace3d-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="ace3d-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ace3d-107">Return value</span></span>

<span data-ttu-id="ace3d-108">Gibt das **Recordset**-Objekt als eine **Variant**-Variable (BSTR) mit Zeichenfolgenwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="ace3d-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="ace3d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace3d-109">Parameters</span></span>

|<span data-ttu-id="ace3d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ace3d-110">Parameter</span></span>|<span data-ttu-id="ace3d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ace3d-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ace3d-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="ace3d-112">*StringFormat*</span></span> |<span data-ttu-id="ace3d-p101">Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="ace3d-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="ace3d-115">*NumRows*</span></span> |<span data-ttu-id="ace3d-p102">Optional. Die Anzahl von im **Recordset**-Objekt zu konvertierenden Zeilen. Ist *NumRows* nicht angegeben oder größer als die Gesamtanzahl der Zeilen im **Recordset**-Objekt, werden alle Zeilen im **Recordset**-Objekt konvertiert.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p102">Optional. The number of rows to be converted in the **Recordset**. If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="ace3d-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="ace3d-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="ace3d-p103">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="ace3d-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="ace3d-122">*RowDelimiter*</span></span> |<span data-ttu-id="ace3d-p104">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="ace3d-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="ace3d-125">*NullExpr*</span></span> |<span data-ttu-id="ace3d-p105">Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ace3d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ace3d-128">Remarks</span></span>

<span data-ttu-id="ace3d-p106">In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset**-Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="ace3d-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="ace3d-131">Diese Methode entspricht der **GetClipString** -Methode in RDO.</span><span class="sxs-lookup"><span data-stu-id="ace3d-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


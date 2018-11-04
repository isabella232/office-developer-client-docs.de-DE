---
title: GetString-Methode (ADO)
TOCTitle: GetString method (ADO)
ms:assetid: f496305e-a1f5-7014-7808-7e4961e5f0fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250242(v=office.15)
ms:contentKeyID: 48548693
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b4926b3568d6c7289ca9d3158a8723e016ed344
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949673"
---
# <a name="getstring-method-ado"></a><span data-ttu-id="645d5-102">GetString-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="645d5-102">GetString method (ADO)</span></span>

<span data-ttu-id="645d5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="645d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="645d5-104">Gibt das [Recordset](recordset-object-ado.md)-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="645d5-104">Returns the [Recordset](recordset-object-ado.md) as a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="645d5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="645d5-105">Syntax</span></span>

<span data-ttu-id="645d5-106">*Variant* = *Recordset-Objekt*. GetString (*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span><span class="sxs-lookup"><span data-stu-id="645d5-106">*Variant* = *recordset*.GetString(*StringFormat*, *NumRows*, *ColumnDelimiter*, *RowDelimiter*, *NullExpr*)</span></span>

## <a name="return-value"></a><span data-ttu-id="645d5-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="645d5-107">Return value</span></span>

<span data-ttu-id="645d5-108">Gibt das **Recordset** -Objekt als eine **Variant** -Variable (BSTR) mit Zeichenfolgenwerten zurück.</span><span class="sxs-lookup"><span data-stu-id="645d5-108">Returns the **Recordset** as a string-valued **Variant** (BSTR).</span></span>

## <a name="parameters"></a><span data-ttu-id="645d5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="645d5-109">Parameters</span></span>

|<span data-ttu-id="645d5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="645d5-110">Parameter</span></span>|<span data-ttu-id="645d5-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="645d5-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="645d5-112">*StringFormat*</span><span class="sxs-lookup"><span data-stu-id="645d5-112">*StringFormat*</span></span> |<span data-ttu-id="645d5-p101">Ein [StringFormatEnum](stringformatenum.md)-Wert, der angibt, wie das **Recordset**-Objekt in eine Zeichenfolge konvertiert werden soll. Die Parameter *RowDelimiter*, *ColumnDelimiter* und *NullExpr* werden nur mit einem *StringFormat* mit dem Wert **adClipString** verwendet.</span><span class="sxs-lookup"><span data-stu-id="645d5-p101">A [StringFormatEnum](stringformatenum.md) value that specifies how the **Recordset** should be converted to a string. The *RowDelimiter*, *ColumnDelimiter*, and *NullExpr* parameters are used only with a *StringFormat* of **adClipString**.</span></span>|
|<span data-ttu-id="645d5-115">*NumRows*</span><span class="sxs-lookup"><span data-stu-id="645d5-115">*NumRows*</span></span> |<span data-ttu-id="645d5-116">Optional.</span><span class="sxs-lookup"><span data-stu-id="645d5-116">Optional.</span></span> <span data-ttu-id="645d5-117">Die Anzahl von im **Recordset** -Objekt zu konvertierenden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="645d5-117">The number of rows to be converted in the **Recordset**.</span></span> <span data-ttu-id="645d5-118">Wenn *NumRows* nicht angegeben ist oder wenn es größer als die Gesamtzahl der Zeilen im **Recordset-Objekt**ist, werden alle Zeilen in das **Recordset-Objekt** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="645d5-118">If *NumRows* is not specified, or if it is greater than the total number of rows in the **Recordset**, then all the rows in the **Recordset** are converted.</span></span>|
|<span data-ttu-id="645d5-119">*ColumnDelimiter*</span><span class="sxs-lookup"><span data-stu-id="645d5-119">*ColumnDelimiter*</span></span> |<span data-ttu-id="645d5-p103">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Tabulatorzeichen.</span><span class="sxs-lookup"><span data-stu-id="645d5-p103">Optional. A delimiter used between columns, if specified, otherwise the TAB character.</span></span>|
|<span data-ttu-id="645d5-122">*RowDelimiter*</span><span class="sxs-lookup"><span data-stu-id="645d5-122">*RowDelimiter*</span></span> |<span data-ttu-id="645d5-p104">Optional. Wenn angegeben, ein zwischen den Spalten verwendetes Trennzeichen, andernfalls das Wagenrücklaufzeichen.</span><span class="sxs-lookup"><span data-stu-id="645d5-p104">Optional. A delimiter used between rows, if specified, otherwise the CARRIAGE RETURN character.</span></span>|
|<span data-ttu-id="645d5-125">*NullExpr*</span><span class="sxs-lookup"><span data-stu-id="645d5-125">*NullExpr*</span></span> |<span data-ttu-id="645d5-p105">Optional. Wenn angegeben, ein statt des Nullwerts verwendeter Ausdruck, andernfalls die leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="645d5-p105">Optional. An expression used in place of a null value, if specified, otherwise the empty string.</span></span>|

## <a name="remarks"></a><span data-ttu-id="645d5-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="645d5-128">Remarks</span></span>

<span data-ttu-id="645d5-p106">In der Zeichenfolge werden Zeilendaten aber keine Schemadaten gespeichert. Daher kann ein **Recordset** -Objekt nicht erneut mithilfe dieser Zeichenfolge geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="645d5-p106">Row data, but no schema data, is saved to the string. Therefore, a **Recordset** cannot be reopened using this string.</span></span>

<span data-ttu-id="645d5-131">Diese Methode entspricht der **GetClipString** -Methode in RDO.</span><span class="sxs-lookup"><span data-stu-id="645d5-131">This method is equivalent to the RDO **GetClipString** method.</span></span>


---
title: CompareBookmarks-Methode (ADO)
TOCTitle: CompareBookmarks method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 460a77284141daad1834699c4dc1775be05c5c26
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712162"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="19436-102">CompareBookmarks-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="19436-102">CompareBookmarks method (ADO)</span></span>

<span data-ttu-id="19436-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19436-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19436-104">Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="19436-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="19436-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19436-105">Syntax</span></span>

<span data-ttu-id="19436-106">*Ergebnis* = *Recordset-Objekt*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="19436-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

## <a name="return-value"></a><span data-ttu-id="19436-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="19436-107">Return value</span></span>

<span data-ttu-id="19436-108">Gibt einen [CompareEnum](compareenum.md)-Wert zurück, der die relative Zeilenposition von zwei Datensätzen angibt, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="19436-108">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="19436-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="19436-109">Parameters</span></span>

|<span data-ttu-id="19436-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="19436-110">Parameter</span></span>|<span data-ttu-id="19436-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19436-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="19436-112">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="19436-112">*Bookmark1*</span></span> |<span data-ttu-id="19436-113">Die Textmarke der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="19436-113">The bookmark of the first row.</span></span>|
|<span data-ttu-id="19436-114">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="19436-114">*Bookmark2*</span></span> |<span data-ttu-id="19436-115">Die Textmarke der zweiten Zeile.</span><span class="sxs-lookup"><span data-stu-id="19436-115">The bookmark of the second row.</span></span>|

## <a name="remarks"></a><span data-ttu-id="19436-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="19436-116">Remarks</span></span>

<span data-ttu-id="19436-p101">Die Textmarken müssen auf dasselbe [Recordset](recordset-object-ado.md)-Objekt oder auf ein **Recordset** -Objekt und dessen [Klon](clone-method-ado.md) angewendet werden. Sie können Textmarken aus verschiedenen **Recordset** -Objekten nicht zuverlässig vergleichen, selbst wenn sie von derselben Quelle oder demselben Befehl erstellt wurden. Sie können auch keine Textmarken für ein **Recordset** -Objekt vergleichen, wenn dessen zugrundeliegender Anbieter Vergleiche nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="19436-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="19436-p102">Eine Textmarke identifiziert eine Zeile in einem **Recordset** -Objekt eindeutig. Verwenden Sie die [Bookmark](bookmark-property-ado.md)-Eigenschaft der aktuellen Zeile, um deren Textmarke abzurufen.</span><span class="sxs-lookup"><span data-stu-id="19436-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="19436-122">Da der Datentyp einer Textmarke anbieterspezifisch ist, gibt ADO sie als einen Variant-Wert.</span><span class="sxs-lookup"><span data-stu-id="19436-122">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="19436-123">SQL Server-Textmarken sind beispielsweise vom Typ DATENBANKTYP\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="19436-123">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="19436-124">ADO würde als einen Variant-Wert mit dem Untertyp Double dieses Typs verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="19436-124">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="19436-p104">Beim Vergleichen von Textmarken werden von ADO keine Umwandlungen vorgenommen. Die Werte werden einfach an den Anbieter übergeben, bei dem der Vergleich durchgeführt wird. Wenn an die **CompareBookmarks** -Methode übergebene Textmarken in Variablen unterschiedlichen Typs gespeichert sind, wird möglicherweise der folgende Typkonfliktfehler generiert: "Die Argumente weisen einen falschen Typ auf, liegen außerhalb des gültigen Bereichs oder führen untereinander zu Konflikten".</span><span class="sxs-lookup"><span data-stu-id="19436-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="19436-128">Eine Textmarke, die ungültig oder falsch formatiert ist, verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="19436-128">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


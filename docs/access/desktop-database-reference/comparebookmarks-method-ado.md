---
title: CompareBookmarks-Methode (ADO)
TOCTitle: CompareBookmarks Method (ADO)
ms:assetid: 826cb3c7-2f5c-284f-421d-6b7b07f14dec
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249564(v=office.15)
ms:contentKeyID: 48545977
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fc4cf3540d22d3981bb13a7af3251dd625c2c99
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606248"
---
# <a name="comparebookmarks-method-ado"></a><span data-ttu-id="685ca-102">CompareBookmarks-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="685ca-102">CompareBookmarks Method (ADO)</span></span>


<span data-ttu-id="685ca-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="685ca-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="685ca-104">Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="685ca-104">Compares two bookmarks and returns an indication of their relative values.</span></span>

## <a name="syntax"></a><span data-ttu-id="685ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="685ca-105">Syntax</span></span>

<span data-ttu-id="685ca-106">*Ergebnis* = *Recordset-Objekt*. CompareBookmarks (*Bookmark1*, *Bookmark2*)</span><span class="sxs-lookup"><span data-stu-id="685ca-106">*result* = *recordset*.CompareBookmarks(*Bookmark1*, *Bookmark2*)</span></span>

<span data-ttu-id="685ca-107"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="685ca-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="685ca-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="685ca-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="685ca-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="685ca-109">Return value</span></span>
>>>>>>> <span data-ttu-id="685ca-110">master</span><span class="sxs-lookup"><span data-stu-id="685ca-110">master</span></span>

<span data-ttu-id="685ca-111">Gibt einen [CompareEnum](compareenum.md)-Wert zurück, der die relative Zeilenposition von zwei Datensätzen angibt, die durch ihre Textmarken dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="685ca-111">Returns a [CompareEnum](compareenum.md) value that indicates the relative row position of two records represented by their bookmarks.</span></span>

## <a name="parameters"></a><span data-ttu-id="685ca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="685ca-112">Parameters</span></span>

  - <span data-ttu-id="685ca-113">*Bookmark1*</span><span class="sxs-lookup"><span data-stu-id="685ca-113">*Bookmark1*</span></span>

  - <span data-ttu-id="685ca-114">Die Textmarke der ersten Zeile.</span><span class="sxs-lookup"><span data-stu-id="685ca-114">The bookmark of the first row.</span></span>

  - <span data-ttu-id="685ca-115">*Bookmark2*</span><span class="sxs-lookup"><span data-stu-id="685ca-115">*Bookmark2*</span></span>

  - <span data-ttu-id="685ca-116">Die Textmarke der zweiten Zeile.</span><span class="sxs-lookup"><span data-stu-id="685ca-116">The bookmark of the second row.</span></span>

## <a name="remarks"></a><span data-ttu-id="685ca-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="685ca-117">Remarks</span></span>

<span data-ttu-id="685ca-p101">Die Textmarken müssen auf dasselbe [Recordset](recordset-object-ado.md)-Objekt oder auf ein **Recordset** -Objekt und dessen [Klon](clone-method-ado.md) angewendet werden. Sie können Textmarken aus verschiedenen **Recordset** -Objekten nicht zuverlässig vergleichen, selbst wenn sie von derselben Quelle oder demselben Befehl erstellt wurden. Sie können auch keine Textmarken für ein **Recordset** -Objekt vergleichen, wenn dessen zugrundeliegender Anbieter Vergleiche nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="685ca-p101">The bookmarks must apply to the same [Recordset](recordset-object-ado.md) object, or a **Recordset** object and its [clone](clone-method-ado.md). You cannot reliably compare bookmarks from different **Recordset** objects, even if they were created from the same source or command. Nor can you compare bookmarks for a **Recordset** object whose underlying provider does not support comparisons.</span></span>

<span data-ttu-id="685ca-p102">Eine Textmarke identifiziert eine Zeile in einem **Recordset** -Objekt eindeutig. Verwenden Sie die [Bookmark](bookmark-property-ado.md)-Eigenschaft der aktuellen Zeile, um deren Textmarke abzurufen.</span><span class="sxs-lookup"><span data-stu-id="685ca-p102">A bookmark uniquely identifies a row in a **Recordset** object. Use the current row's [Bookmark](bookmark-property-ado.md) property to obtain its bookmark.</span></span>

<span data-ttu-id="685ca-123">Da der Datentyp einer Textmarke anbieterspezifisch ist, gibt ADO sie als einen Variant-Wert.</span><span class="sxs-lookup"><span data-stu-id="685ca-123">Because the data type of a bookmark is provider specific, ADO exposes it as a Variant.</span></span> <span data-ttu-id="685ca-124">SQL Server-Textmarken sind beispielsweise vom Typ DATENBANKTYP\_R8 (Double).</span><span class="sxs-lookup"><span data-stu-id="685ca-124">For example, SQL Server bookmarks are of type DBTYPE\_R8 (Double).</span></span> <span data-ttu-id="685ca-125">ADO würde als einen Variant-Wert mit dem Untertyp Double dieses Typs verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="685ca-125">ADO would expose this type as a Variant with a subtype of Double.</span></span>

<span data-ttu-id="685ca-p104">Beim Vergleichen von Textmarken werden von ADO keine Umwandlungen vorgenommen. Die Werte werden einfach an den Anbieter übergeben, bei dem der Vergleich durchgeführt wird. Wenn an die **CompareBookmarks** -Methode übergebene Textmarken in Variablen unterschiedlichen Typs gespeichert sind, wird möglicherweise der folgende Typkonfliktfehler generiert: "Die Argumente weisen einen falschen Typ auf, liegen außerhalb des gültigen Bereichs oder führen untereinander zu Konflikten".</span><span class="sxs-lookup"><span data-stu-id="685ca-p104">When comparing bookmarks, ADO does not attempt any type of coercion. The values are simply passed to the provider where the compare occurs. If bookmarks passed to the **CompareBookmarks** method are stored in variables of differing types, it can generate the type mismatch error, "Arguments are of the wrong type, are out of the acceptable range, or are in conflict with each other."</span></span>

<span data-ttu-id="685ca-129">Eine Textmarke, die ungültig oder falsch formatiert ist, verursacht einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="685ca-129">A bookmark that is not valid or incorrectly formed will cause an error.</span></span>


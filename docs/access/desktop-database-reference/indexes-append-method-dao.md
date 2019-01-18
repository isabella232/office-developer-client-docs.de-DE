---
title: Indexes.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bcebcf2f7fbce59c6050100f1763923a6025526e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713443"
---
# <a name="indexesappend-method-dao"></a><span data-ttu-id="72f08-102">Indexes.Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="72f08-102">Indexes.Append method (DAO)</span></span>

<span data-ttu-id="72f08-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="72f08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72f08-104">Fügt der **Indexes**-Auflistung ein neues **Index**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="72f08-104">Adds a new **Index** to the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f08-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="72f08-105">Syntax</span></span>

<span data-ttu-id="72f08-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="72f08-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="72f08-107">*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="72f08-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="72f08-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72f08-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72f08-109">Name</span><span class="sxs-lookup"><span data-stu-id="72f08-109">Name</span></span></p></th>
<th><p><span data-ttu-id="72f08-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="72f08-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="72f08-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="72f08-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="72f08-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72f08-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72f08-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="72f08-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="72f08-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="72f08-114">Required</span></span></p></td>
<td><p><span data-ttu-id="72f08-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="72f08-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="72f08-116">Eine Objektvariable, die das Element darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="72f08-116">An object variable that represents the item being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="72f08-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72f08-117">Remarks</span></span>

<span data-ttu-id="72f08-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="72f08-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="72f08-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="72f08-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="72f08-120">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="72f08-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="72f08-121">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="72f08-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>


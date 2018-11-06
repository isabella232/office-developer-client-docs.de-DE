---
title: Indexes.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 60dce80f-505b-e988-3ac1-8ecaae3d3d09
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194835(v=office.15)
ms:contentKeyID: 48545191
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7781f18615f424fd4139fb3fe46868ec00a43c24
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997882"
---
# <a name="indexesappend-method-dao"></a><span data-ttu-id="fb4b6-102">Indexes.Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb4b6-102">Indexes.Append method (DAO)</span></span>

<span data-ttu-id="fb4b6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb4b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb4b6-104">Fügt der **Indexes**-Auflistung ein neues **Index**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-104">Adds a new **Index** to the **Indexes** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb4b6-105">Syntax</span></span>

<span data-ttu-id="fb4b6-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="fb4b6-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="fb4b6-107">*Ausdruck* Eine Variable, die ein **Indexes** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-107">*expression* A variable that represents an **Indexes** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb4b6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb4b6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb4b6-109">Name</span><span class="sxs-lookup"><span data-stu-id="fb4b6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fb4b6-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="fb4b6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="fb4b6-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fb4b6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="fb4b6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb4b6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb4b6-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="fb4b6-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="fb4b6-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="fb4b6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="fb4b6-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="fb4b6-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="fb4b6-116">Eine Objektvariable, die das Element darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-116">An object variable that represents the item being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fb4b6-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb4b6-117">Remarks</span></span>

<span data-ttu-id="fb4b6-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="fb4b6-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="fb4b6-120">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="fb4b6-121">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="fb4b6-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>


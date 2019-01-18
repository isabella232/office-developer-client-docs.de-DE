---
title: Workspaces.Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 195c26a6-a1d1-40a8-7e7e-13cd632008b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845644(v=office.15)
ms:contentKeyID: 48543498
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11d721d58301d2adb33b2e381d88d7245531ff06
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718884"
---
# <a name="workspacesappend-method-dao"></a><span data-ttu-id="f2153-102">Workspaces.Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2153-102">Workspaces.Append method (DAO)</span></span>

<span data-ttu-id="f2153-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2153-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2153-104">Fügt der **Workspaces**-Auflistung ein neues **Workspace**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f2153-104">Adds a new **Workspace** to the **Workspaces** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2153-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2153-105">Syntax</span></span>

<span data-ttu-id="f2153-106">*Ausdruck* . Fügen Sie (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="f2153-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="f2153-107">*Ausdruck* Eine Variable, die ein **Workspaces** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2153-107">*expression* A variable that represents a **Workspaces** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2153-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2153-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2153-109">Name</span><span class="sxs-lookup"><span data-stu-id="f2153-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f2153-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="f2153-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="f2153-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f2153-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="f2153-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2153-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2153-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="f2153-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="f2153-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="f2153-114">Required</span></span></p></td>
<td><p><span data-ttu-id="f2153-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="f2153-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="f2153-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f2153-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f2153-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2153-117">Remarks</span></span>

<span data-ttu-id="f2153-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="f2153-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="f2153-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="f2153-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="f2153-120">Wenn das Objekt an die, das Sie anfügen möchten (beispielsweise wenn Sie, alle **Field** -Objekte **Fields** -Auflistung eines **Index** -Objekts angefügt haben, bevor es an eine **Indexes** -Auflistung angehängt wird) abgeschlossen ist oder wenn die Eigenschaften in einem oder mehreren festlegen untergeordnete Objekte sind falsch ist, verwenden die **Append** -Methode einen Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="f2153-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="f2153-121">Angenommen, wenn Sie keinen Feldtyp angegeben und versuchen Sie es dann das **Field** -Objekt an die **Fields** -Auflistung in ein **TableDef** -Objekt angefügt werden soll, löst mit der **Append** -Methode einen Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="f2153-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>


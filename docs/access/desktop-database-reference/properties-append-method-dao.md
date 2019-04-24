---
title: Properties. Append-Methode (DAO)
TOCTitle: Append Method
ms:assetid: 47f1e24f-975c-3fdc-5c3c-8c91f2920c81
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193232(v=office.15)
ms:contentKeyID: 48544609
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 528809495ebefd15a8895b15a9d51f84e6892980
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301309"
---
# <a name="propertiesappend-method-dao"></a><span data-ttu-id="be9bd-102">Properties. Append-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="be9bd-102">Properties.Append method (DAO)</span></span>

<span data-ttu-id="be9bd-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be9bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be9bd-104">Fügt der **Properties**-Auflistung ein neues **Property**-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="be9bd-104">Adds a new **Property** to the **Properties** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9bd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be9bd-105">Syntax</span></span>

<span data-ttu-id="be9bd-106">*Ausdruck* . Append (***Objekt***)</span><span class="sxs-lookup"><span data-stu-id="be9bd-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="be9bd-107">*Ausdruck* Eine Variable, die ein **Properties** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="be9bd-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="be9bd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be9bd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be9bd-109">Name</span><span class="sxs-lookup"><span data-stu-id="be9bd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="be9bd-110">Erforderlich/optional</span><span class="sxs-lookup"><span data-stu-id="be9bd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="be9bd-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="be9bd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="be9bd-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="be9bd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be9bd-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="be9bd-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="be9bd-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="be9bd-114">Required</span></span></p></td>
<td><p><span data-ttu-id="be9bd-115"><strong>Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="be9bd-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="be9bd-116">Eine Objektvariable, die das Feld darstellt, das an die Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="be9bd-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="be9bd-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be9bd-117">Remarks</span></span>

<span data-ttu-id="be9bd-118">Das angefügte Objekt wird zu einem beständigen Objekt und auf einem Datenträger gespeichert, bis Sie es mithilfe der **Delete**-Methode löschen.</span><span class="sxs-lookup"><span data-stu-id="be9bd-118">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="be9bd-119">Das Hinzufügen eines neuen Objekts geschieht ohne Verzögerung. Trotzdem sollten Sie die **Refresh**-Methode auf alle weiteren Auflistungen anwenden, die von Änderungen an der Datenbankstruktur betroffen sein könnten.</span><span class="sxs-lookup"><span data-stu-id="be9bd-119">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="be9bd-120">Wenn das Objekt, das Sie anfügen, nicht vollständig ist (beispielsweise, wenn Sie keine **Field** -Objekte an eine **Fields** -Auflistung eines **Index** -Objekts angefügt haben, \*\*\*\* bevor es an eine Indexes-Auflistung angefügt wird) oder wenn die Eigenschaften, die in einem oder mehreren festgelegt sind untergeordnete Objekte sind falsch, bei Verwendung der **Append** -Methode wird ein Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="be9bd-120">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="be9bd-121">Wenn Sie beispielsweise noch keinen Feldtyp angegeben haben und dann versuchen, das **Field** -Objekt an die **Fields** -Auflistung in einem **TableDef** -Objekt anzufügen, löst mithilfe der **Append** -Methode ein Laufzeitfehler aus.</span><span class="sxs-lookup"><span data-stu-id="be9bd-121">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>


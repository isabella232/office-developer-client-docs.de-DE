---
title: LockNavigationPane-Makroaktion
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717804"
---
# <a name="locknavigationpane-macro-action"></a><span data-ttu-id="6069a-102">LockNavigationPane-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="6069a-102">LockNavigationPane macro action</span></span>


<span data-ttu-id="6069a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6069a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6069a-104">Mit der **SperrenNavigationsbereich** -Aktion können Sie verhindern, dass Benutzer Datenbankobjekte löschen können, die im Navigationsbereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6069a-104">You can use the **LockNavigationPane** action to prevent users from deleting database objects that are displayed in the Navigation Pane.</span></span>

## <a name="setting"></a><span data-ttu-id="6069a-105">Einstellung</span><span class="sxs-lookup"><span data-stu-id="6069a-105">Setting</span></span>

<span data-ttu-id="6069a-106">Die **SperrenNavigationsbereich** -Aktion verfügt über folgendes Argument.</span><span class="sxs-lookup"><span data-stu-id="6069a-106">The **LockNavigationPane** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6069a-107">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="6069a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6069a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6069a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6069a-109"><strong>Lock</strong></span><span class="sxs-lookup"><span data-stu-id="6069a-109"><strong>Lock</strong></span></span></p></td>
<td><p><span data-ttu-id="6069a-110">Wählen Sie <strong>Ja</strong> zum Sperren des Navigationsbereichs aus, oder wählen Sie <strong>Nein</strong> zum Aufheben der Sperrung des Navigationsbereichs aus.</span><span class="sxs-lookup"><span data-stu-id="6069a-110">Select <strong>Yes</strong> to lock the Navigation Pane, or <strong>No</strong> to unlock the Navigation Pane.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6069a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6069a-111">Remarks</span></span>

<span data-ttu-id="6069a-112">Durch Sperren des Navigationsbereichs werden Sie daran gehindert, Datenbankobjekte zu löschen oder in die Zwischenablage auszuschneiden.</span><span class="sxs-lookup"><span data-stu-id="6069a-112">Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard.</span></span> <span data-ttu-id="6069a-113">Es ist *nicht* verhindern, dass Sie einen der folgenden Vorgänge ausführen:</span><span class="sxs-lookup"><span data-stu-id="6069a-113">It does *not* prevent you from performing any of the following operations:</span></span>

  - <span data-ttu-id="6069a-114">Kopieren von Datenbankobjekten in die Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="6069a-114">Copying database objects to the clipboard</span></span>

  - <span data-ttu-id="6069a-115">Einfügen von Datenbankobjekten aus der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="6069a-115">Pasting database objects from the clipboard</span></span>

  - <span data-ttu-id="6069a-116">Ein- oder Ausblenden des Navigationsbereichs</span><span class="sxs-lookup"><span data-stu-id="6069a-116">Displaying or hiding the Navigation Pane</span></span>

  - <span data-ttu-id="6069a-117">Auswählen verschiedener Organisationsschemas für den Navigationsbereich</span><span class="sxs-lookup"><span data-stu-id="6069a-117">Selecting different Navigation Pane organization schemes</span></span>

  - <span data-ttu-id="6069a-118">Ein- oder Ausblenden von Abschnitten des Navigationsbereichs</span><span class="sxs-lookup"><span data-stu-id="6069a-118">Showing or hiding sections of the Navigation Pane</span></span>

<span data-ttu-id="6069a-119">Verwenden Sie zum Ausführen der **SperrenNavigationsbereich** -Aktion in einem VBA-Modul die **LockNavigationPane** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6069a-119">To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.</span></span>


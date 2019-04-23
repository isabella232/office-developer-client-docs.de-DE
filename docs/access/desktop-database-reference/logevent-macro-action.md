---
title: LogEvent-Makroaktion
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289836"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="751a1-102">LogEvent-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="751a1-102">LogEvent macro action</span></span>

<span data-ttu-id="751a1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="751a1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="751a1-104">Mit der **ProtokollierenEreignis** -Aktion werden Informationen in die **USysApplicationLog** -Systemtabelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="751a1-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="751a1-105">Die **ProtokollierenEreignis**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="751a1-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="751a1-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="751a1-106">Setting</span></span>

<span data-ttu-id="751a1-107">Die **ProtokollierenEreignis**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="751a1-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="751a1-108">Argument</span><span class="sxs-lookup"><span data-stu-id="751a1-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="751a1-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="751a1-109">Required</span></span></p></th>
<th><p><span data-ttu-id="751a1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="751a1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="751a1-111"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="751a1-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="751a1-112">Nein</span><span class="sxs-lookup"><span data-stu-id="751a1-112">No</span></span></p></td>
<td><p><span data-ttu-id="751a1-p101">Ein Zeichenfolgenausdruck, der die Bedingung beschreibt, die Sie protokollieren möchten. Die Länge der Beschreibung darf 255 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="751a1-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="751a1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="751a1-115">Remarks</span></span>

<span data-ttu-id="751a1-p102">Mit der **ProtokollierenEreignis** -Aktion können Sie in der **USysApplicationLog** -Systemtabelle Statusinformationen schreiben, für die nicht mit der **[AuslösenFehler](raiseerror-macro-action.md)** -Aktion ein Fehler ausgelöst werden muss. Beispielsweise können Sie Änderungen in einem bestimmten Feld protokollieren oder die Einträge in **USysApplicationLog** beim Debuggen des Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="751a1-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="751a1-118">Wenn Sie die **ProtokollierenEreignis** -Aktion zum Schreiben in der **USysApplicationLog** -Tabelle verwenden, wird die **Kategorie** -Spalte automatisch auf **Benutzer** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="751a1-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="751a1-119">Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="751a1-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="751a1-120">Klicken Sie im Menü **Datei** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="751a1-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="751a1-121">Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="751a1-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="751a1-122">Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="751a1-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="751a1-123">Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="751a1-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="751a1-124">Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="751a1-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>


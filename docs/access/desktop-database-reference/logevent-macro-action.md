---
title: LogEvent-Makroaktion
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edc2fcaa72f6bfb912708948903aa09b25447580
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998173"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="e0bc7-102">LogEvent-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="e0bc7-102">LogEvent macro action</span></span>

<span data-ttu-id="e0bc7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0bc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0bc7-104">Mit der **ProtokollierenEreignis** -Aktion werden Informationen in die **USysApplicationLog** -Systemtabelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>

> [!NOTE]
> <span data-ttu-id="e0bc7-105">[!HINWEIS] Die **ProtokollierenEreignis** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-105">The **LogEvent** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e0bc7-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e0bc7-106">Setting</span></span>

<span data-ttu-id="e0bc7-107">Die **ProtokollierenEreignis** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0bc7-108">Argument</span><span class="sxs-lookup"><span data-stu-id="e0bc7-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e0bc7-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0bc7-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e0bc7-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0bc7-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0bc7-111"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="e0bc7-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="e0bc7-112">Nein</span><span class="sxs-lookup"><span data-stu-id="e0bc7-112">No</span></span></p></td>
<td><p><span data-ttu-id="e0bc7-p101">Ein Zeichenfolgenausdruck, der die Bedingung beschreibt, die Sie protokollieren möchten. Die Länge der Beschreibung darf 255 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="e0bc7-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0bc7-115">Remarks</span></span>

<span data-ttu-id="e0bc7-p102">Mit der **ProtokollierenEreignis** -Aktion können Sie in der **USysApplicationLog** -Systemtabelle Statusinformationen schreiben, für die nicht mit der **[AuslösenFehler](raiseerror-macro-action.md)** -Aktion ein Fehler ausgelöst werden muss. Beispielsweise können Sie Änderungen in einem bestimmten Feld protokollieren oder die Einträge in **USysApplicationLog** beim Debuggen des Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="e0bc7-118">Wenn Sie die **ProtokollierenEreignis** -Aktion zum Schreiben in der **USysApplicationLog** -Tabelle verwenden, wird die **Kategorie** -Spalte automatisch auf **Benutzer** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="e0bc7-119">Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="e0bc7-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="e0bc7-120">Klicken Sie im Menü **Datei** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="e0bc7-121">Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="e0bc7-122">Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="e0bc7-123">Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="e0bc7-124">Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e0bc7-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>


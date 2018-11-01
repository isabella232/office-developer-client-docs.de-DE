---
title: ProtokollierenEreignis-Makroaktion
TOCTitle: LogEvent Macro Action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 093313028822bebea26fbf86dfc94063e5512e14
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873376"
---
# <a name="logevent-macro-action"></a><span data-ttu-id="e73d5-102">ProtokollierenEreignis-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="e73d5-102">LogEvent Macro Action</span></span>


<span data-ttu-id="e73d5-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e73d5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e73d5-104">Mit der **ProtokollierenEreignis** -Aktion werden Informationen in die **USysApplicationLog** -Systemtabelle geschrieben.</span><span class="sxs-lookup"><span data-stu-id="e73d5-104">The **LogEvent** action writes information to the **USysApplicationLog** system table.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e73d5-105">[!HINWEIS] Die <STRONG>ProtokollierenEreignis</STRONG> -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e73d5-105">The <STRONG>LogEvent</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="e73d5-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e73d5-106">Setting</span></span>

<span data-ttu-id="e73d5-107">Die **ProtokollierenEreignis** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e73d5-107">The **LogEvent** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e73d5-108">Argument</span><span class="sxs-lookup"><span data-stu-id="e73d5-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e73d5-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="e73d5-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e73d5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e73d5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e73d5-111"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="e73d5-111"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="e73d5-112">Nein</span><span class="sxs-lookup"><span data-stu-id="e73d5-112">No</span></span></p></td>
<td><p><span data-ttu-id="e73d5-p101">Ein Zeichenfolgenausdruck, der die Bedingung beschreibt, die Sie protokollieren möchten. Die Länge der Beschreibung darf 255 Zeichen nicht überschreiten.</span><span class="sxs-lookup"><span data-stu-id="e73d5-p101">A string expression that describes the condition that you want to log. The description cannot exceed 255 characters.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e73d5-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e73d5-115">Remarks</span></span>

<span data-ttu-id="e73d5-p102">Mit der **ProtokollierenEreignis** -Aktion können Sie in der **USysApplicationLog** -Systemtabelle Statusinformationen schreiben, für die nicht mit der **[AuslösenFehler](raiseerror-macro-action.md)** -Aktion ein Fehler ausgelöst werden muss. Beispielsweise können Sie Änderungen in einem bestimmten Feld protokollieren oder die Einträge in **USysApplicationLog** beim Debuggen des Makros verwenden.</span><span class="sxs-lookup"><span data-stu-id="e73d5-p102">The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.</span></span>

<span data-ttu-id="e73d5-118">Wenn Sie die **ProtokollierenEreignis** -Aktion zum Schreiben in der **USysApplicationLog** -Tabelle verwenden, wird die **Kategorie** -Spalte automatisch auf **Benutzer** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e73d5-118">When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.</span></span>

<span data-ttu-id="e73d5-119">Zum Anzeigen der **USysApplicationLog** -Tabelle gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="e73d5-119">To see the **USysApplicationLog** table, use the following steps:</span></span>

1.  <span data-ttu-id="e73d5-120">Klicken Sie im Menü **Datei** auf **Optionen**.</span><span class="sxs-lookup"><span data-stu-id="e73d5-120">Click the **File** menu,and then click **Options**.</span></span>

2.  <span data-ttu-id="e73d5-121">Klicken Sie im Dialogfeld **Access-Optionen** auf die Registerkarte **Aktuelle Datenbank**.</span><span class="sxs-lookup"><span data-stu-id="e73d5-121">In the **Access Options** dialog box, click the **Current Database** tab.</span></span>

3.  <span data-ttu-id="e73d5-122">Klicken Sie im Bereich **Navigation** auf **Navigationsoptionen**.</span><span class="sxs-lookup"><span data-stu-id="e73d5-122">In the **Navigation** section, click **Navigation Options**.</span></span>

4.  <span data-ttu-id="e73d5-123">Klicken Sie im Dialogfeld **Navigationsoptionen** auf **Systemobjekte anzeigen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e73d5-123">In the **Navigation Options** dialog box, click **Show System Objects**, and then click **OK**.</span></span>

5.  <span data-ttu-id="e73d5-124">Klicken Sie auf **OK**, um das Dialogfeld **Access-Optionen** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e73d5-124">Click **OK** to dismiss the **Access Options** dialog box.</span></span>


---
title: RepaintObject-Makroaktion
TOCTitle: RepaintObject macro action
ms:assetid: e8fa7d0b-578c-5071-2bd5-b772b48637a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836055(v=office.15)
ms:contentKeyID: 48548431
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm195788
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 369c518ab0ab213975bb7da3c96b6e5844bad9ee
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919416"
---
# <a name="repaintobject-macro-action"></a><span data-ttu-id="c53d4-102">RepaintObject-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="c53d4-102">RepaintObject macro action</span></span>


<span data-ttu-id="c53d4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c53d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c53d4-p101">Sie können die **AktualisierenObjekt** -Aktion verwenden, um alle ausstehenden Bildschirmaktualisierungen für ein angegebenes Datenbankobjekt oder für das aktive Datenbankobjekt durchzuführen, falls keines angegeben ist. Zu solchen Aktualisierungen gehören alle ausstehenden Neuberechnungen für die Steuerelemente des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p101">You can use the **RepaintObject** action to complete any pending screen updates for a specified database object or for the active database object, if none is specified. Such updates include any pending recalculations for the object's controls.</span></span>

## <a name="setting"></a><span data-ttu-id="c53d4-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="c53d4-106">Setting</span></span>

<span data-ttu-id="c53d4-107">Die **AktualisierenObjekt** -Aktion verwendet die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="c53d4-107">The **RepaintObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c53d4-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="c53d4-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c53d4-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c53d4-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c53d4-110"><strong>Objekttyp</strong></span><span class="sxs-lookup"><span data-stu-id="c53d4-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c53d4-p102">Der Typ des zu aktualisierenden Objekts. Klicken Sie im Feld Objekttyp im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Tabelle, Abfrage, Formular, Bericht, Makro, Modul, Datenzugriffsseite, Serversicht, Diagramm, Gespeicherte Prozedur oder Funktion. Lassen Sie dieses Argument leer, um das aktive Objekt auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p102">The type of object to repaint. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. Leave this argument blank to select the active object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c53d4-114"><strong>Objektname</strong></span><span class="sxs-lookup"><span data-stu-id="c53d4-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c53d4-p103">Der Name des zu aktualisierenden Objekts. Im Feld <strong>Objektname</strong> werden alle Objekte in der Datenbank des Typs angezeigt, der vom Argument <strong>Objekttyp</strong> ausgewählt ist. Wenn Sie das Argument <strong>Objekttyp</strong> leer lassen, müssen Sie auch dieses Argument leer lassen.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p103">The name of the object to repaint. The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c53d4-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c53d4-118">Remarks</span></span>

<span data-ttu-id="c53d4-p104">Microsoft Access wartet mit dem Beenden ausstehender Bildschirmaktualisierungen, bis andere ausstehende Aufgaben beendet sind. Mit dieser Aktion können Sie die sofortige Aktualisierung der Steuerelemente im angegebenen Objekt erzwingen. In den folgenden Fällen können Sie diese Aktion verwenden:</span><span class="sxs-lookup"><span data-stu-id="c53d4-p104">Microsoft Access waits to complete pending screen updates until it finishes other pending tasks. With this action, you can force immediate repainting of the controls in the specified object. You can use this action:</span></span>

  - <span data-ttu-id="c53d4-p105">Wenn Sie die **SetzenWert** -Aktion zum Ändern von Werten für eine Vielzahl von Steuerelementen verwenden. In Access werden die Änderungen möglicherweise nicht unmittelbar angezeigt, insbesondere, wenn andere Steuerelemente (wie berechnete Steuerelemente) von Werten des geänderten Steuerelements abhängen.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p105">When you use the **SetValue** action to change values in a number of controls. Access might not show the changes immediately, especially if other controls (such as calculated controls) depend on values in the changed controls.</span></span>

  - <span data-ttu-id="c53d4-p106">Wenn Sie sicher gehen möchten, dass das angezeigte Formular Daten in all seinen Steuerelementen anzeigt. Beispielsweise zeigen Steuerelemente, die OLE-Objekte enthalten, ihre Daten nicht unmittelbar nach Öffnen eines Formulars an.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p106">When you want to make sure that the form you are viewing displays data in all of its controls. For example, controls containing OLE objects don't display their data immediately after you open a form.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="c53d4-p107">Diese Aktion verursacht keine erneute Abfrage der Datenbank, sodass keine neuen und geänderten Datensätze angezeigt oder Datensätze aus der zugrunde liegenden Tabelle oder der zugrunde liegenden Abfrage des Objekts entfernt werden. Verwenden Sie zur erneuten Abfrage der Objektquelle oder eines ihrer Steuerelemente die <STRONG>AktualisierenDaten</STRONG> -Aktion. Verwenden Sie die <STRONG>AnzeigenAlleDatensätze</STRONG> -Aktion, um die neuesten Datensätze anzuzeigen, und entfernen Sie eventuell angewendete Filter.</span><span class="sxs-lookup"><span data-stu-id="c53d4-p107">This action doesn't cause a requery of the database, so it doesn't show new and changed records or remove deleted records from the object's underlying table or query. Use the <STRONG>Requery</STRONG> action to requery the source of the object or one of its controls. Use the <STRONG>ShowAllRecords</STRONG> action to display the most recent records and remove any applied filters.</span></span></P>
> <LI>
> <P><span data-ttu-id="c53d4-129">Die <STRONG>AktualisierenObjekt</STRONG> -Aktion hat dieselbe Wirkung wie das Klicken auf <STRONG>Aktualisieren</STRONG> in der Gruppe <STRONG>Datensätze</STRONG>auf der Registerkarte <STRONG>Start</STRONG>, durch das alle Änderungen angezeigt werden, die Sie oder andere Benutzer an den aktuell angezeigten Datensätzen in Formularen und Datenblättern vorgenommen haben.</span><span class="sxs-lookup"><span data-stu-id="c53d4-129">The <STRONG>RepaintObject</STRONG> action doesn't have the same effect as clicking <STRONG>Refresh</STRONG> in the <STRONG>Records</STRONG> group on the <STRONG>Home</STRONG> tab, which shows any changes you or other users have made to the currently displayed records in forms and datasheets.</span></span></P></LI></UL>



<span data-ttu-id="c53d4-130">Verwenden Sie die **RepaintObject** -Methode des **DoCmd** -Objekts, um die **AktualisierenObjekt** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c53d4-130">To run the **RepaintObject** action in a Visual Basic for Applications (VBA) module, use the **RepaintObject** method of the **DoCmd** object.</span></span>


---
title: OpenDiagram-Makroaktion
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288357"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="ce99c-102">OpenDiagram-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="ce99c-102">OpenDiagram macro action</span></span>

<span data-ttu-id="ce99c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce99c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce99c-104">In einem Access-Projekt können Sie die **ÖffnenDiagramm** -Aktion verwenden, um ein Datenbankdiagramm in der Entwurfsansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ce99c-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="ce99c-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="ce99c-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="ce99c-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ce99c-106">Setting</span></span>

<span data-ttu-id="ce99c-107">Die **ÖffnenDiagramm**-Aktion verwendet das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="ce99c-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ce99c-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="ce99c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="ce99c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce99c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ce99c-110"><strong>Diagrammname</strong></span><span class="sxs-lookup"><span data-stu-id="ce99c-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="ce99c-111">Der Name des zu öffnenden Datenbankdiagramms.</span><span class="sxs-lookup"><span data-stu-id="ce99c-111">The name of the database diagram to open.</span></span> <span data-ttu-id="ce99c-112">Im Feld <strong>Diagramm Name</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator werden alle Datenbankdiagramme in der aktuellen Datenbank angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce99c-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="ce99c-113">Dies ist ein erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="ce99c-113">This is a required argument.</span></span> <span data-ttu-id="ce99c-114">Wenn Sie ein Makro, das die <strong>ÖffnenDiagramm</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</span><span class="sxs-lookup"><span data-stu-id="ce99c-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="ce99c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce99c-115">Remarks</span></span>

<span data-ttu-id="ce99c-116">Diese Aktion entspricht dem Doppelklicken auf ein Datenbankdiagramm im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Datenbankdiagramm im Navigationsbereich und dem anschließenden Klicken auf **Entwurfsansicht**.</span><span class="sxs-lookup"><span data-stu-id="ce99c-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="ce99c-p102">[!TIPP] Sie können ein Datenbankdiagramm aus dem Navigationsbereich in eine Makro aktionszeile ziehen. Hierdurch wird automatisch eine **ÖffnenDiagramm** -Aktion erstellt, die das Datenbankdiagramm in der Entwurfsansicht öffnet.</span><span class="sxs-lookup"><span data-stu-id="ce99c-p102">You can drag a database diagram from the Navigation Pane to a macro action row. This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="ce99c-119">Verwenden Sie die **OpenDiagram** -Methode des **DoCmd** -Objekts, um die **ÖffnenDiagramm** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ce99c-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>


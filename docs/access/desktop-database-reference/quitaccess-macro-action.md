---
title: QuitAccess-Makroaktion
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f30459483af92a915aaa1e94eb4bb12e0f8ca93c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919689"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="9d9d1-102">QuitAccess-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="9d9d1-102">QuitAccess macro action</span></span>


<span data-ttu-id="9d9d1-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d9d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d9d1-p101">Sie können die **BeendenAccess** -Aktion verwenden, um Microsoft Access zu beenden. Für das Speichern von Datenbankobjekten vor dem Beenden von Access kann die **BeendenAccess** -Aktion außerdem mindestens eine Option festlegen.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-p101">You can use the **QuitAccess** action to exit Microsoft Access. The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="9d9d1-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="9d9d1-108">Einstellung</span><span class="sxs-lookup"><span data-stu-id="9d9d1-108">Setting</span></span>

<span data-ttu-id="9d9d1-109">Die **BeendenAccess** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-109">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9d9d1-110">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="9d9d1-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9d9d1-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d9d1-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d9d1-112"><strong>Options</strong></span><span class="sxs-lookup"><span data-stu-id="9d9d1-112"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="9d9d1-p103">Gibt an, was mit nicht gespeicherten Objekten geschieht, wenn Sie Access beenden. Klicken Sie im Feld Optionen im Bereich Aktionsargumente des Bereichs Makro-Generator auf Nachfragen (um Dialogfelder anzuzeigen, die Sie fragen, ob Sie ein Objekt speichern möchten), Alles speichern (um alle Objekte zu speichern, ohne anhand von Dialogfeldern gefragt zu werden) oder auf Beenden (um zu beenden, ohne die Objekte zu speichern). Die Standardeinstellung ist Alles speichern.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-p103">Specifies what happens to unsaved objects when you quit Access. Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9d9d1-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d9d1-116">Remarks</span></span>

<span data-ttu-id="9d9d1-117">Access führt keine Aktionen aus, die in einem Makro auf die **BeendenAccess** -Aktion folgen.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-117">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="9d9d1-p104">Sie können diese Aktion verwenden, um Access ohne Aufforderungen in den Dialogfeldern **Speichern** zu beenden, indem Sie einen benutzerdefinierten Menübefehl oder eine Schaltfläche in einem Formular verwenden. Unter Umständen verfügen Sie über ein Masterformular, das Sie zum Anzeigen der Objekte in Ihrem benutzerdefinierten Arbeitsbereich verwenden. Dieses Formular enthält möglicherweise eine Schaltfläche **Beenden**, mit der ein Makro ausgeführt wird, das die **BeendenAccess** -Aktion enthält, deren Argument **Optionen** auf **Alles speichern** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-p104">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form. For example, you might have a master form that you use to display the objects in your custom workspace. This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="9d9d1-p105">Diese Aktion hat dieselbe Wirkung wie ein Klicken auf die Registerkarte **Datei** und dann ein Klicken auf **Beenden**. Wenn beim Klicken auf diesen Befehl nicht gespeicherte Objekte vorhanden sind, stimmen die Dialogfelder, die angezeigt werden, mit denen überein, die angezeigt werden, wenn Sie **Nachfragen** für das Argument **Optionen** der **BeendenAccess** -Aktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-p105">This action has the same effect as clicking the **File** tab and then clicking **Exit**. If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="9d9d1-123">In einem Makro können Sie die **SpeichernObjekt** -Aktion verwenden, um ein angegebenes Objekt zu speichern, ohne Access beenden oder das Objekt schließen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-123">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="9d9d1-124">Verwenden Sie die **Quit** -Methode des **DoCmd** -Objekts, um die **BeendenAccess** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9d9d1-124">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>


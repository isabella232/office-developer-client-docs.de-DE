---
title: RunSavedImportExport-Makroaktion
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7f98076c147a55561adf2baf24b55274bbea463d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998847"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="d0a48-102">RunSavedImportExport-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="d0a48-102">RunSavedImportExport macro action</span></span>

<span data-ttu-id="d0a48-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0a48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0a48-104">Mit der **RunSavedImportExport** -Aktion können Sie eine gespeicherte Import- oder Exportspezifikation ausführen, die Sie mit dem Import- bzw. Export-Assistenten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d0a48-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>

> [!NOTE]
> <span data-ttu-id="d0a48-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="d0a48-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="d0a48-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="d0a48-106">Setting</span></span>

<span data-ttu-id="d0a48-107">Die **RunSavedImportExport** -Aktion hat das folgende Argument.</span><span class="sxs-lookup"><span data-stu-id="d0a48-107">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0a48-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="d0a48-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d0a48-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0a48-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0a48-110"><strong>Name des gespeicherten Imports oder Exports</strong></span><span class="sxs-lookup"><span data-stu-id="d0a48-110"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d0a48-111">Wählen Sie den Namen einer gespeicherten Import- oder Exportspezifikation in der Dropdownliste aus.</span><span class="sxs-lookup"><span data-stu-id="d0a48-111">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d0a48-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0a48-112">Remarks</span></span>

- <span data-ttu-id="d0a48-113">Diese Makroaktion hat denselben Effekt wie das Ausführen der folgenden Prozedur in Access:</span><span class="sxs-lookup"><span data-stu-id="d0a48-113">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
  1.  <span data-ttu-id="d0a48-114">Klicken Sie auf der Registerkarte **Externe Daten** auf **Gespeicherte Importe** oder **Gespeicherte Exporte**.</span><span class="sxs-lookup"><span data-stu-id="d0a48-114">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
  2.  <span data-ttu-id="d0a48-115">Klicken Sie im Dialogfeld **Datentasks verwalten** auf der Registerkarte **Gespeicherte Importe** oder **Gespeicherte Exporte** (abhängig von Ihrer Auswahl im vorherigen Schritt) auf die Spezifikation, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="d0a48-115">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
  3.  <span data-ttu-id="d0a48-116">Klicken Sie auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d0a48-116">Click **Run**.</span></span>

- <span data-ttu-id="d0a48-117">Vergewissern Sie sich vor der Ausführung der **RunSavedImportExport** -Aktion, dass die Quell- und Zieldateien vorhanden sind, die Datenquelle zum Importieren bereit ist und der Vorgang nicht versehentlich Daten in der Zieldatei überschreibt.</span><span class="sxs-lookup"><span data-stu-id="d0a48-117">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

- <span data-ttu-id="d0a48-118">Links zu weiteren Informationen über das Speichern und Ausführen von Import- und Exportspezifikationen finden Sie im Abschnitt **Siehe auch**.</span><span class="sxs-lookup"><span data-stu-id="d0a48-118">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

- <span data-ttu-id="d0a48-119">Wenn die gespeicherte Import- oder Exportspezifikation, die Sie auswählen, für das Argument **Gespeichert importieren exportieren Name** gelöscht wird, nachdem das Makro erstellt wird, zeigt Access die folgende Fehlermeldung angezeigt, wenn das Makro ausgeführt wird: \*\*die Spezifikation mit dem angegebenen Index ist nicht vorhanden. Geben Sie einen anderen Index. ' \*\*\* Spezifikation Namen \***'.**</span><span class="sxs-lookup"><span data-stu-id="d0a48-119">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>


---
title: ImportSharePointList-Makroaktion
TOCTitle: ImportSharePointList macro action
ms:assetid: 6a633d7d-d81d-0e2e-6c1c-706a552c1bf2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195403(v=office.15)
ms:contentKeyID: 48545429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152234
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: df77d2375b66df907832b6ff2717427ae54a35a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291859"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="7a1e3-102">ImportSharePointList-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="7a1e3-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="7a1e3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a1e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a1e3-104">Mit der **ImportierenSharePointListe** -Aktion können Sie Daten von einer Microsoft SharePoint Foundation-Website importieren oder verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="7a1e3-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="7a1e3-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="7a1e3-106">Setting</span></span>

<span data-ttu-id="7a1e3-107">Die **ImportierenSharePointListe**-Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a1e3-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="7a1e3-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="7a1e3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a1e3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a1e3-110"><strong>Transfertyp</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-111">Wählen Sie den Übertragungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="7a1e3-112">Wählen Sie <strong>importieren</strong> aus, um die SharePoint Foundation-Daten in eine Tabelle in Microsoft Access zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="7a1e3-113">Aktualisierungen der Daten in Access wirken sich nicht auf die Daten in SharePoint Foundation aus.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="7a1e3-114">Entsprechend wirken sich Aktualisierungen an den Daten in SharePoint Foundation nicht auf die Daten in Access aus.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="7a1e3-115">Wählen Sie <strong>Link</strong> aus, um eine verknüpfte Tabelle in Access zu erstellen, die mit den Daten in SharePoint Foundation verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="7a1e3-116">Aktualisierungen der Daten in Access werden in SharePoint Foundation widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="7a1e3-117">Entsprechend werden Aktualisierungen der Daten in SharePoint Foundation in Access wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1e3-118"><strong>Websiteadresse</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-119">Geben Sie den vollständigen Pfad der SharePoint-Website ein.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a1e3-120"><strong>Listen-ID</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-121">Geben Sie den Namen oder die GUID der zu übertragenden Liste ein.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-121">Enter the name or GUID of the list to be transferred.</span></span> <span data-ttu-id="7a1e3-122">Erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-122">Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1e3-123"><strong>Sicht-ID</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-p104">Geben Sie die GUID der Ansicht für die Liste ein, die Sie verwenden möchten. Lassen Sie das Argument leer, um alle Zeilen und Spalten in der Liste zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a1e3-126"><strong>Tabellenname</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-127">Geben Sie den Namen ein, der in Access für die Tabelle oder die verknüpfte Tabelle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1e3-128"><strong>Nachschlageanzeigewerte abrufen</strong></span><span class="sxs-lookup"><span data-stu-id="7a1e3-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e3-129">Wählen Sie <strong>Ja</strong>, um Anzeigewerte für Nachschlagefelder statt der ID zu übertragen, um die Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7a1e3-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a1e3-130">Remarks</span></span>

- <span data-ttu-id="7a1e3-131">Diese Aktion hat den gleichen Effekt wie das Klicken auf **SharePoint-Liste** in der Gruppe **Importieren** auf der Registerkarte **Externe Daten**. Die Argumente für die Aktion entsprechen den Optionen, die Sie im Assistenten für externe Daten auswählen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="7a1e3-132">Verwenden Sie die **TransferSharePointList** -Methode des **DoCmd** -Objekts, um die **ImportierenSharePointListe** -Aktion in einem VBA-Modul auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="7a1e3-133">Wenn Sie eine nicht vorhandene Liste oder Ansicht angeben, tritt kein Fehler auf, und es werden keine Daten übertragen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="7a1e3-p105">Eine GUID ist ein eindeutiger hexadezimaler Bezeichner für eine Liste oder eine Ansicht. Eine GUID muss im folgenden Format eingegeben werden, in dem jedes "F" eine hexadezimale Nummer ist (0 bis 9 oder A bis F).</span><span class="sxs-lookup"><span data-stu-id="7a1e3-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="7a1e3-136">Sie erhalten die GUID für eine Liste oder Ansicht von der SharePoint-Website mithilfe der folgenden Prozedur:</span><span class="sxs-lookup"><span data-stu-id="7a1e3-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="7a1e3-137">Öffnen Sie die Liste in SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="7a1e3-138">Wenn die gewünschte Ansicht nicht angezeigt wird, klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann die gewünschte Ansicht.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="7a1e3-139">Klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann **Diese Ansicht ändern**.Die Adresse in der Adressleiste des Browsers enthält die GUIDs sowohl für die Liste als auch für die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="7a1e3-140">Die GUID für die Liste befolgt **Liste=**, und die GUID für die Ansicht befolgt **Ansicht=**.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="7a1e3-141">In der Adresse wird jedoch jedes **{** -Zeichen (linke Klammer) durch die Zeichenfolge **%7B** dargestellt, jeder **-** (Bindestrich) durch die Zeichenfolge **%2D**, und jedes **}** -Zeichen (rechte Klammer) wird durch die Zeichenfolge **%7D** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="7a1e3-142">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7a1e3-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="7a1e3-143">Bevor Sie die GUIDs aus der Adresse als Argumente in dieser Makroaktion verwenden können, müssen Sie jede **% 7B** -Zeichenfolge durch das Zeichen **{** ersetzen, jede **%-2D** - **-** Zeichenfolge durch das Zeichen ersetzen und jede **% 7D** -Zeichenfolge durch die **}** -Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="7a1e3-144">Fügen Sie nicht das **&** -Zeichen (kaufmännisches Und-Zeichen) ein, das auf die **%7D** -Zeichenfolge in der Listen-GUID folgt.</span><span class="sxs-lookup"><span data-stu-id="7a1e3-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>


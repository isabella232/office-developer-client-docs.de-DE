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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726204"
---
# <a name="importsharepointlist-macro-action"></a><span data-ttu-id="2129b-102">ImportSharePointList-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="2129b-102">ImportSharePointList macro action</span></span>

<span data-ttu-id="2129b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2129b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2129b-104">Mit der **ImportierenSharePointListe** -Aktion können Sie Daten von einer Microsoft SharePoint Foundation-Website importieren oder verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="2129b-104">You can use the **ImportSharePointList** action to import or link data from a Microsoft SharePoint Foundation site.</span></span>

> [!NOTE]
> <span data-ttu-id="2129b-105">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="2129b-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="2129b-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="2129b-106">Setting</span></span>

<span data-ttu-id="2129b-107">Die **ImportierenSharePointListe** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="2129b-107">The **ImportSharePointList** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2129b-108">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="2129b-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2129b-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2129b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2129b-110"><strong>Transfertyp</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-110"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-111">Wählen Sie den Übertragungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="2129b-111">Select the type of transfer.</span></span></p>
<ul>
<li><p><span data-ttu-id="2129b-112">Wählen Sie <strong>Importieren</strong> , kopieren Sie die SharePoint Foundation-Daten in eine Tabelle in Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2129b-112">Select <strong>Import</strong> to copy the SharePoint Foundation data into a table in Microsoft Access.</span></span> <span data-ttu-id="2129b-113">Updates für die Daten in Access haben keinen Einfluss auf die Daten in SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="2129b-113">Updates to the data in Access do not affect the data in SharePoint Foundation.</span></span> <span data-ttu-id="2129b-114">Aktualisierung der Daten in SharePoint Foundation wirken sich dagegen nicht auf die Daten in Access aus.</span><span class="sxs-lookup"><span data-stu-id="2129b-114">Likewise, updates to the data in SharePoint Foundation do not affect the data in Access.</span></span></p></li>
<li><p><span data-ttu-id="2129b-115">Wählen Sie <strong>Link</strong> erstellen Sie eine verknüpfte Tabelle in Access, die eine Verknüpfung mit den Daten in SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="2129b-115">Select <strong>Link</strong> to create a linked table in Access that links to the data in SharePoint Foundation.</span></span> <span data-ttu-id="2129b-116">Aktualisierung der Daten in Access werden in SharePoint Foundation übernommen.</span><span class="sxs-lookup"><span data-stu-id="2129b-116">Updates to the data in Access are reflected in SharePoint Foundation.</span></span> <span data-ttu-id="2129b-117">Dementsprechend werden Updates mit den Daten in SharePoint Foundation in Access wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="2129b-117">Likewise, updates to the data in SharePoint Foundation are reflected in Access.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2129b-118"><strong>Websiteadresse</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-118"><strong>Site Address</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-119">Geben Sie den vollständigen Pfad der SharePoint-Website ein.</span><span class="sxs-lookup"><span data-stu-id="2129b-119">Enter the full path of the SharePoint site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2129b-120"><strong>Listen-ID</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-120"><strong>List ID</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-p103">Geben Sie den Namen oder die GUID der zu übertragenden Liste ein. Erforderliches Argument.</span><span class="sxs-lookup"><span data-stu-id="2129b-p103">Enter the name or GUID of the list to be transferred. Required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2129b-123"><strong>Sicht-ID</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-123"><strong>View ID</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-p104">Geben Sie die GUID der Ansicht für die Liste ein, die Sie verwenden möchten. Lassen Sie das Argument leer, um alle Zeilen und Spalten in der Liste zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="2129b-p104">Enter the GUID of the view for the list you want to use. Leave this argument blank to transfer all rows and columns in the list.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2129b-126"><strong>Tabellenname</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-127">Geben Sie den Namen ein, der in Access für die Tabelle oder die verknüpfte Tabelle angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2129b-127">Enter the name you want displayed for the table or linked table in Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2129b-128"><strong>Nachschlageanzeigewerte abrufen</strong></span><span class="sxs-lookup"><span data-stu-id="2129b-128"><strong>Get Lookup Display Values</strong></span></span></p></td>
<td><p><span data-ttu-id="2129b-129">Wählen Sie <strong>Ja</strong>, um Anzeigewerte für Nachschlagefelder statt der ID zu übertragen, um die Suche durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="2129b-129">Select <strong>Yes</strong> to transfer display values for Lookup fields instead of the ID used to perform the lookup.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2129b-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2129b-130">Remarks</span></span>

- <span data-ttu-id="2129b-131">Diese Aktion hat den gleichen Effekt wie das Klicken auf **SharePoint-Liste** in der Gruppe **Importieren** auf der Registerkarte **Externe Daten**. Die Argumente für die Aktion entsprechen den Optionen, die Sie im Assistenten für externe Daten auswählen.</span><span class="sxs-lookup"><span data-stu-id="2129b-131">This action has the same effect as clicking **SharePoint List** in the **Import** group on the **External Data** tab. The arguments for the action correspond to the choices you make in the Get External Data Wizard.</span></span>

- <span data-ttu-id="2129b-132">Verwenden Sie die **TransferSharePointList** -Methode des **DoCmd** -Objekts, um die **ImportierenSharePointListe** -Aktion in einem VBA-Modul auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2129b-132">To run the **ImportSharePointList** action in a VBA module, use the **TransferSharePointList** method of the **DoCmd** object.</span></span>

- <span data-ttu-id="2129b-133">Wenn Sie eine nicht vorhandene Liste oder Ansicht angeben, tritt kein Fehler auf, und es werden keine Daten übertragen.</span><span class="sxs-lookup"><span data-stu-id="2129b-133">If you specify a nonexistent list or view, no error occurs, and no data is transferred.</span></span>

- <span data-ttu-id="2129b-p105">Eine GUID ist ein eindeutiger hexadezimaler Bezeichner für eine Liste oder eine Ansicht. Eine GUID muss im folgenden Format eingegeben werden, in dem jedes "F" eine hexadezimale Nummer ist (0 bis 9 oder A bis F).</span><span class="sxs-lookup"><span data-stu-id="2129b-p105">A GUID is a unique hexadecimal identifier for a list or a view. A GUID must be entered in the following format, where each "F" is a hexadecimal number (0 through 9 or A through F).</span></span>
    
  `{FFFFFFFF-FFFF-FFFF-FFFF-FFFFFFFFFFFF}`
    
  <span data-ttu-id="2129b-136">Sie erhalten die GUID für eine Liste oder Ansicht von der SharePoint-Website mithilfe der folgenden Prozedur:</span><span class="sxs-lookup"><span data-stu-id="2129b-136">You can obtain the GUID for a list or view from the SharePoint site by using the following procedure:</span></span>
    
  1. <span data-ttu-id="2129b-137">Öffnen Sie die Liste in SharePoint Foundation.</span><span class="sxs-lookup"><span data-stu-id="2129b-137">Open the list in SharePoint Foundation.</span></span>
    
  2. <span data-ttu-id="2129b-138">Wenn die gewünschte Ansicht nicht angezeigt wird, klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann die gewünschte Ansicht.</span><span class="sxs-lookup"><span data-stu-id="2129b-138">If the view you want is not displayed, click the **View** drop-down arrow and then select the view you want.</span></span>
    
  3. <span data-ttu-id="2129b-139">Klicken Sie auf den Dropdownpfeil **Ansicht**, und markieren Sie dann **Diese Ansicht ändern**.Die Adresse in der Adressleiste des Browsers enthält die GUIDs sowohl für die Liste als auch für die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="2129b-139">Click the **View** drop-down arrow and then select **Modify this View**.The address in the browser's address bar contains the GUIDs for both the list and the view.</span></span> <span data-ttu-id="2129b-140">Die GUID für die Liste befolgt **Liste=**, und die GUID für die Ansicht befolgt **Ansicht=**.</span><span class="sxs-lookup"><span data-stu-id="2129b-140">The GUID for the list follows **List=**, and the GUID for the view follows **View=**.</span></span> <span data-ttu-id="2129b-141">In der Adresse wird jedoch jedes **{** -Zeichen (linke Klammer) durch die Zeichenfolge **%7B** dargestellt, jeder **-** (Bindestrich) durch die Zeichenfolge **%2D**, und jedes **}** -Zeichen (rechte Klammer) wird durch die Zeichenfolge **%7D** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2129b-141">However, in the address, each **{** (left brace) character is represented by the string **%7B**, each **-** (hyphen) character is represented by the string **%2D**, and each **}** (right brace) character is represented by the string **%7D**.</span></span> <span data-ttu-id="2129b-142">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2129b-142">For example:</span></span>
        
     `https://MySite12/_layouts/ViewEdit.aspx?List=%7B2A82A404%2D5529%2D47DC%2DAE13%2DAC1D9BC0A84F%7D&View=%7B357B4FE6%2D44CF%2D4275%2DB91F%2D46558301579B%7D`
        
  <span data-ttu-id="2129b-143">Bevor Sie die GUIDs der Absenderadresse als Argumente in dieser Makroaktion verwenden können, müssen Sie jede **% 7 b** -Zeichenfolge mit dem Zeichen **{** ersetzen, ersetzen Sie jedes **% 2D** string mit der **-** Zeichen, und Ersetzen Sie jede **% 7 D** Zeichenfolge mit der **}** Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2129b-143">Before you can use the GUIDs from the address as arguments in this macro action, you must replace each **%7B** string with the **{** character, replace each **%2D** string with the **-** character, and replace each **%7D** string with the **}** character.</span></span> <span data-ttu-id="2129b-144">Fügen Sie nicht das **&** -Zeichen (kaufmännisches Und-Zeichen) ein, das auf die **%7D** -Zeichenfolge in der Listen-GUID folgt.</span><span class="sxs-lookup"><span data-stu-id="2129b-144">Do not include the **&** (ampersand) character that follows the **%7D** string in the list GUID.</span></span>


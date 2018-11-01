---
title: ImportExportSpreadsheet-Makroaktion
TOCTitle: ImportExportSpreadsheet Macro Action
ms:assetid: 526aef41-8329-5335-9d16-4d332542a297
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193927(v=office.15)
ms:contentKeyID: 48544846
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm31446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 78819ba2a82bf2fc9ab5c39300d06c1acdda80bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875805"
---
# <a name="importexportspreadsheet-macro-action"></a><span data-ttu-id="3a38a-102">ImportExportSpreadsheet-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="3a38a-102">ImportExportSpreadsheet Macro Action</span></span>


<span data-ttu-id="3a38a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a38a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a38a-p101">Mit der **ImportExportSpreadsheet** -Aktion können Sie Daten zwischen der aktuellen Access-Datenbank (.mdb oder .accdb) oder einem Access-Projekt (.adp) und einer Tabellenkalkulationsdatei importieren oder exportieren. Sie können auch die Daten in einer Microsoft Excel-Tabellenkalkulation mit der aktuellen Microsoft Access-Datenbank verknüpfen. Bei einer verknüpften Tabellenkalkulation können Sie die Tabellenkalkulationsdaten mit Access anzeigen und bearbeiten, während trotzdem uneingeschränkter Zugriff auf die Daten aus Ihrem Excel-Tabellenkalkulationsprogramm möglich ist. Sie können auch eine Verknüpfung mit Daten in einer Lotus-1-2-3-Tabellenkalkulationsdatei herstellen, diese Daten sind jedoch in Access schreibgeschützt. .</span><span class="sxs-lookup"><span data-stu-id="3a38a-p101">You can use the **ImportExportSpreadsheet** action to import or export data between the current Access database (.mdb or .accdb) or Access project (.adp) and a spreadsheet file. You can also link the data in a Microsoft Excel spreadsheet to the current Microsoft Access database. With a linked spreadsheet, you can view and edit the spreadsheet data with Access while still allowing complete access to the data from your Excel spreadsheet program. You can also link to data in a Lotus 1-2-3 spreadsheet file, but this data is read-only in Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3a38a-p102">[!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="3a38a-110">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3a38a-110">Setting</span></span>

<span data-ttu-id="3a38a-111">Die **TransferSpreadsheet** -Aktion hat die folgenden Argumente.</span><span class="sxs-lookup"><span data-stu-id="3a38a-111">The **TransferSpreadsheet** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3a38a-112">Aktionsargument</span><span class="sxs-lookup"><span data-stu-id="3a38a-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3a38a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a38a-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3a38a-114"><strong>Transfertyp</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-114"><strong>Transfer Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p103">Der Transfertyp, den Sie vornehmen möchten. Wählen Sie <strong>Importieren</strong>, <strong>Exportieren</strong> oder <strong>Verknüpfen</strong> im Feld <strong>Transfertyp</strong> des Abschnitts <strong>Aktionsargumente</strong> des Bereichs "Makro-Generator" aus. Die Standardeinstellung ist <strong>Importieren</strong>.  </span><span class="sxs-lookup"><span data-stu-id="3a38a-p103">The type of transfer you want to make. Select <strong>Import</strong>, <strong>Export</strong>, or <strong>Link</strong> in the <strong>Transfer Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. The default is <strong>Import</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="3a38a-118">Der Transfertyp <STRONG>Verknüpfen</STRONG> wird für Access-Projekte (.adp) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3a38a-118">The <STRONG>Link</STRONG> transfer type is not supported for Access projects (.adp).</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a38a-119"><strong>Dateiformat</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-119"><strong>Spreadsheet Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p104">Der Tabellenkalkulationstyp, in den importiert, aus dem exportiert oder zu dem eine Verknüpfung hergestellt werden soll. Sie können einen der im Feld aufgeführten Tabellenkalkulationstypen auswählen. Die Standardeinstellung ist <strong>Excel-Arbeitsmappe</strong>.  </span><span class="sxs-lookup"><span data-stu-id="3a38a-p104">The type of spreadsheet to import from, export to, or link to. You can select one of a number of spreadsheet types in the box. The default is <strong>Excel Workbook</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="3a38a-p105">Sie können aus Lotus WK4-Dateien importieren und eine (schreibgeschützte) Verknüpfung mit diesen herstellen, aber Sie können keine Access-Daten in dieses Tabellenkalkulationsformat exportieren. Auch das Importieren, Exportieren oder Verknüpfen von Daten aus Lotus WKS- oder Excel Version 2.0-Tabellenkalkulationen mit dieser Aktion wird von Access nicht mehr unterstützt. Wenn Sie Daten aus einer Tabellenkalkulation im Excel Version 2.0- oder Lotus WKS-Format importieren oder eine Verknüpfung mit diesen herstellen möchten, konvertieren Sie die Tabellenkalkulationsdaten in eine neuere Version von Excel oder Lotus 1-2-3, bevor Sie die Daten in Access importieren oder verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p105">You can import from and link (read-only) to Lotus .WK4 files, but you can't export Access data to this spreadsheet format. Access also no longer supports importing, exporting, or linking data from Lotus .WKS or Excel version 2.0 spreadsheets with this action. If you want to import from or link to spreadsheet data in Excel version 2.0 or Lotus .WKS format, convert the spreadsheet data to a later version of Excel or Lotus 1-2-3 before importing or linking the data into Access.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a38a-126"><strong>Tabellenname</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-126"><strong>Table Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p106">Der Name der Access-Tabelle, in die Tabellenkalkulationsdaten importiert, aus der solche Daten exportiert bzw. mit der solche Daten verknüpft werden sollen. Sie können auch den Namen der Access-Auswahlabfrage eingeben, aus der Sie Daten exportieren möchten. Dies ist ein erforderliches Argument. Wenn Sie <strong>Importieren</strong> im Argument <strong>Transfertyp</strong> auswählen, hängt Access die Tabellenkalkulationsdaten an diese Tabelle an, sofern die Tabelle bereits vorhanden ist. Andernfalls erstellt Access eine neue Tabelle mit den Tabellenkalkulationsdaten. In Access können Sie bei Verwendung der <strong>ImportExportSpreadsheet</strong> -Aktion keine SQL-Anweisung verwenden, um die zu exportierenden Daten anzugeben. Anstatt eine SQL-Anweisung zu verwenden, müssen Sie zunächst eine Abfrage erstellen und dann den Namen der Abfrage im Argument <strong>Tabellenname</strong> angeben.  </span><span class="sxs-lookup"><span data-stu-id="3a38a-p106">The name of the Access table to import spreadsheet data to, export spreadsheet data from, or link spreadsheet data to. You can also type the name of the Access select query you want to export data from. This is a required argument. If you select <strong>Import</strong> in the <strong>Transfer Type</strong> argument, Access appends the spreadsheet data to this table if the table already exists. Otherwise, Access creates a new table containing the spreadsheet data. In Access, you can't use an SQL statement to specify data to export when you are using the <strong>ImportExportSpreadsheet</strong> action. Instead of using an SQL statement, you must first create a query and then specify the name of the query in the <strong>Table Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a38a-134"><strong>Dateiname</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-134"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p107">Der Name der Tabellenkalkulationsdatei, aus der importiert, in die exportiert bzw. mit der verknüpft werden soll. Geben Sie den vollständigen Pfad an. Dies ist ein erforderliches Argument. Wenn Sie Daten aus Access exportieren, erstellt Access eine neue Tabellenkalkulation. Wenn der Dateiname mit dem Namen einer vorhandenen Tabellenkalkulation identisch ist, ersetzt Access die vorhandene Tabellenkalkulation, es sei denn, Sie exportieren in eine Excel-Arbeitsmappe der Version 5.0 oder höher. In diesem Fall kopiert Access die exportierten Daten in das nächste verfügbare neue Arbeitsblatt in der Arbeitsmappe. Beim Importieren aus oder Verknüpfen mit einer Excel-Tabellenkalkulation der Version 5.0 oder höher können Sie das Argument <strong>Bereich</strong> verwenden, um ein bestimmtes Arbeitsblatt anzugeben.  </span><span class="sxs-lookup"><span data-stu-id="3a38a-p107">The name of the spreadsheet file to import from, export to, or link to. Include the full path. This is a required argument. Access creates a new spreadsheet when you export data from Access. If the file name is the same as the name of an existing spreadsheet, Access replaces the existing spreadsheet, unless you're exporting to an Excel version 5.0 or later workbook. In that case, Access copies the exported data to the next available new worksheet in the workbook. If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can specify a particular worksheet by using the <strong>Range</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3a38a-142"><strong>Besitzt Feldnamen</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-142"><strong>Has Field Names</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p108">Gibt an, ob die erste Zeile der Tabellenkalkulation die Namen der Felder enthält. Wenn Sie <strong>Ja</strong> wählen, verwendet Access die Namen in dieser Zeile beim Importieren oder Verknüpfen der Tabellenkalkulationsdaten als Feldnamen in der Access-Tabelle. Wenn Sie <strong>Nein</strong> wählen, behandelt Access die erste Zeile als normale Zeile mit Daten. Die Standardeinstellung ist <strong>Nein</strong>. Wenn Sie eine Access-Tabelle oder -Auswahlabfrage in eine Tabellenkalkulation exportieren, werden die Feldnamen in die erste Zeile der Tabellenkalkulation eingefügt, unabhängig davon, was Sie in diesem Argument auswählen.  </span><span class="sxs-lookup"><span data-stu-id="3a38a-p108">Specifies whether the first row of the spreadsheet contains the names of the fields. If you select <strong>Yes</strong>, Access uses the names in this row as field names in the Access table when you import or link the spreadsheet data. If you select <strong>No</strong>, Access treats the first row as a normal row of data. The default is <strong>No</strong>. When you export an Access table or select query to a spreadsheet, the field names are inserted into the first row of the spreadsheet no matter what you select in this argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3a38a-148"><strong>Bereich</strong></span><span class="sxs-lookup"><span data-stu-id="3a38a-148"><strong>Range</strong></span></span></p></td>
<td><p><span data-ttu-id="3a38a-p109">Der Bereich von Zellen, der importiert oder verknüpft werden soll. Lassen Sie dieses Argument leer, um die gesamten Tabellenkalkulation zu importieren oder zu verknüpfen. Sie können den Namen eines Bereichs in der Tabellenkalkulation eingeben oder den zu importierenden oder zu verknüpfenden Zellenbereich angeben, z. B. A1:E25 (beachten Sie, dass die A1..E25-Syntax in Access 97 oder höher nicht funktioniert). Wenn Sie aus einer Excel-Tabellenkalkulation der Version 5.0 oder höher importieren bzw. mit dieser verknüpfen, können Sie dem Bereich den Namen des Arbeitsblatts und ein Ausrufezeichen voranstellen; z. B. Budget!A1:C7.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p109">The range of cells to import or link. Leave this argument blank to import or link the entire spreadsheet. You can type the name of a range in the spreadsheet or specify the range of cells to import or link, such as A1:E25 (note that the A1..E25 syntax does not work in Access 97 or later). If you are importing from or linking to an Excel version 5.0 or later spreadsheet, you can prefix the range with the name of the worksheet and an exclamation point; for example, Budget!A1:C7.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="3a38a-p110">Beim Exportieren in eine Tabellenkalkulation müssen Sie dieses Argument leer lassen. Wenn Sie einen Bereich eingeben, tritt beim Exportvorgang ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p110">When you export to a spreadsheet, you must leave this argument blank. If you enter a range, the export will fail.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3a38a-155">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3a38a-155">Remarks</span></span>

<span data-ttu-id="3a38a-p111">Sie können die Daten in Access-Auswahlabfragen in Tabellenkalkulationen exportieren. Access exportiert das Resultset der Abfrage und behandelt es wie eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p111">You can export the data in Access select queries to spreadsheets. Access exports the result set of the query, treating it just like a table.</span></span>

<span data-ttu-id="3a38a-158">Tabellenkalkulationsdaten, die Sie an eine vorhandene Access-Tabelle anfügen, müssen mit der Struktur der Tabelle kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="3a38a-158">Spreadsheet data that you append to an existing Access table must be compatible with the table's structure.</span></span>

  - <span data-ttu-id="3a38a-159">Jedes Feld in der Tabellenkalkulation muss den gleichen Datentyp haben wie das entsprechende Feld in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a38a-159">Each field in the spreadsheet must be of the same data type as the corresponding field in the table.</span></span>

  - <span data-ttu-id="3a38a-160">Die Felder müssen in derselben Reihenfolge vorliegen (es sei denn, Sie legen das Argument **Besitzt Feldnamen** auf **Ja** fest; in diesem Fall müssen die Feldnamen in der Tabellenkalkulation mit den Feldnamen in der Tabelle übereinstimmen).</span><span class="sxs-lookup"><span data-stu-id="3a38a-160">The fields must be in the same order (unless you set the **Has Field Names** argument to **Yes**, in which case the field names in the spreadsheet must match the field names in the table).</span></span>

<span data-ttu-id="3a38a-p112">Diese Aktion entspricht dem Klicken auf die Registerkarte **Externe Daten** und dem Klicken auf **Excel** in der Gruppe **Importieren** oder **Exportieren** oder dem Klicken auf **Mehr** in der Gruppe **Importieren** oder **Exportieren** und dem Klicken auf **Lotus-1-2-3-Datei**. Sie können diese Befehle verwenden, um eine Datenquelle wie z. B. Access oder einen Datenbank-, Tabellenkalkulations- oder Textdateityp auszuwählen. Wenn Sie eine Tabellenkalkulation auswählen, wird eine Reihe von Dialogfeldern angezeigt oder ein Access-Assistent ausgeführt, in dem Sie den Namen der Tabellenkalkulation und andere Optionen auswählen. Die Argumente der **ImportExportSpreadsheet** -Aktion entsprechen den Optionen in diesen Dialogfeldern oder in den Assistenten.</span><span class="sxs-lookup"><span data-stu-id="3a38a-p112">This action is similar to clicking the **External Data** tab and clicking **Excel** in the **Import** or **Export** group, or clicking **More** in the **Import** or **Export** group and clicking **Lotus 1-2-3 File**. You can use these commands to select a source of data, such as Access or a type of database, spreadsheet, or text file. If you select a spreadsheet, a series of dialog boxes appear, or an Access wizard runs, in which you select the name of the spreadsheet and other options. The arguments of the **ImportExportSpreadsheet** action reflect the options in these dialog boxes or in the wizards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3a38a-165">[!HINWEIS] Beim Abfragen oder Filtern einer verknüpften Tabellenkalkulation wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="3a38a-165">If you query or filter a linked spreadsheet, the query or filter is case-sensitive.</span></span></P>



<span data-ttu-id="3a38a-166">Wenn Sie eine Verknüpfung mit einer Excel-Tabellenkalkulation herstellen, die im Bearbeitungsmodus geöffnet ist, stellt Access die Verknüpfung erst dann her, wenn die Excel-Tabellenkalkulation den Bearbeitungsmodus verlassen hat. Es gibt kein Timeout.</span><span class="sxs-lookup"><span data-stu-id="3a38a-166">If you link to an Excel spreadsheet that is open in Edit mode, Access will wait until the Excel spreadsheet is out of Edit mode before completing the link; there's no time-out.</span></span>

<span data-ttu-id="3a38a-167">Zum Ausführen der **ImportExportSpreadsheet** -Aktion in einem Visual Basic for Applications (VBA)-Modul verwenden Sie die **TransferSpreadsheet** -Methode des **DoCmd** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a38a-167">To run the **ImportExportSpreadsheet** action in a Visual Basic for Applications (VBA) module, use the **TransferSpreadsheet** method of the **DoCmd** object.</span></span>


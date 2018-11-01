---
title: Initialisieren des Microsoft Excel-Treibers
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f039378c619cb5c9ebe6a70ccae718f5abfdd306
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873901"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="f933e-102">Initialisieren des Microsoft Excel-Treibers</span><span class="sxs-lookup"><span data-stu-id="f933e-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="f933e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f933e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f933e-104">Bei der Installation des Excel-Treibers schreibt das Setupprogramm Standardwerte der Windows-Registrierung im Unterschlüssel Module und -ISAM-Formate.</span><span class="sxs-lookup"><span data-stu-id="f933e-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="f933e-105">Sie sollten diese Einstellungen nicht direkt geändert. Verwenden Sie das Setupprogramm für Ihre Anwendung hinzufügen, entfernen oder ändern Sie diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="f933e-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="f933e-106">In den folgenden Abschnitten werden die Initialisierung und ISAM formateinstellungen für die Microsoft Excel-Datenbanktreibers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f933e-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="f933e-107">Initialisierungseinstellungen für Excel</span><span class="sxs-lookup"><span data-stu-id="f933e-107">Excel Initialization Settings</span></span>

<span data-ttu-id="f933e-108">Die **Konnektivitätsmodul für Access\\Module\\Excel** Ordner enthält initialisierungseinstellungen für Aceexcl.dll-Treiber für den externen Zugriff zu Microsoft Excel-Arbeitsblättern verwendet.</span><span class="sxs-lookup"><span data-stu-id="f933e-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="f933e-109">Standardeinstellungen für die Einträge in diesem Ordner sind im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="f933e-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="f933e-110">Das Microsoft Access-Datenbankmodul verwendet die Einträge im Ordner Excel wie folgt.</span><span class="sxs-lookup"><span data-stu-id="f933e-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f933e-111">Eintrag</span><span class="sxs-lookup"><span data-stu-id="f933e-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="f933e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f933e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f933e-113">Win32</span><span class="sxs-lookup"><span data-stu-id="f933e-113">win32</span></span></p></td>
<td><p><span data-ttu-id="f933e-p103">Der Speicherort von msexcl40.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="f933e-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="f933e-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="f933e-118">Die Anzahl der Zeilen für den Datentyp überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="f933e-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="f933e-119">Der Datentyp ist die maximale Anzahl von Arten von Daten anhand.</span><span class="sxs-lookup"><span data-stu-id="f933e-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="f933e-120">Wenn eine Tie vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt: Zahl, Währung, Datum, Text, Boolean.</span><span class="sxs-lookup"><span data-stu-id="f933e-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="f933e-121">Wenn Daten, die nicht den Datentyp für die Spalte ermittelten übereinstimmt gefunden werden, wird es als einen <strong>Null</strong> -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f933e-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="f933e-122">Beim Import Wenn eine Spalte gemischte Datentypen wurde wird die gesamte Spalte gemäß der ImportMixedTypes-Einstellung umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="f933e-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="f933e-123">Die Standardanzahl von Zeilen zu überprüfenden ist 8.</span><span class="sxs-lookup"><span data-stu-id="f933e-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="f933e-124">Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="f933e-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="f933e-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="f933e-p105">Mögliche Werte sind MajorityType und Text. Mit MajorityType werden Spalten mit gemischten Datentypen beim Importieren in den vorherrschenden Datentyp konvertiert. Mit Text werden Spalten mit gemischten Datentypen beim Importieren in Text konvertiert. Die Standardeinstellung ist Text. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="f933e-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="f933e-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="f933e-p106">Die Anzahl leerer Zeichen, die vor neuen Daten am Ende eines Arbeitsblatts der Version 3.5 oder Version 4.0 eingefügt werden. Wenn AppendBlankRows beispielsweise auf 4 festgelegt wird, fügt Microsoft Jet 4 leere Zeilen am Ende des Arbeitsblatts ein, und danach erst Zeilen mit Daten. Mögliche ganzzahlige Werte für diese Einstellungen sind die Zahlen 0 bis 16; die Standardeinstellung ist 01 (eine zusätzliche Zeile wird eingefügt). Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="f933e-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="f933e-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="f933e-p107">Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden. Der Wert 00 gibt an, dass in der ersten Zeile keine Spaltennamen verwendet werden; Spaltennamen werden als F1, F2, F3 usw. angezeigt. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="f933e-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f933e-142">Die **Konnektivitätsmodul für Access\\Module\\Excel 8.0** Ordner enthält die folgenden Einträge, die für Microsoft Excel 97 gelten.</span><span class="sxs-lookup"><span data-stu-id="f933e-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f933e-143">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="f933e-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="f933e-144">Type</span><span class="sxs-lookup"><span data-stu-id="f933e-144">Type</span></span></p></th>
<th><p><span data-ttu-id="f933e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="f933e-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f933e-146">Engine</span><span class="sxs-lookup"><span data-stu-id="f933e-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="f933e-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f933e-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f933e-148">Excel</span><span class="sxs-lookup"><span data-stu-id="f933e-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="f933e-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="f933e-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f933e-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f933e-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="f933e-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="f933e-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="f933e-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f933e-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f933e-154">01</span><span class="sxs-lookup"><span data-stu-id="f933e-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="f933e-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="f933e-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f933e-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f933e-157">00</span><span class="sxs-lookup"><span data-stu-id="f933e-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="f933e-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="f933e-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="f933e-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="f933e-160">1</span><span class="sxs-lookup"><span data-stu-id="f933e-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="f933e-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="f933e-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f933e-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f933e-163">00</span><span class="sxs-lookup"><span data-stu-id="f933e-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="f933e-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="f933e-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f933e-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f933e-166">01</span><span class="sxs-lookup"><span data-stu-id="f933e-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f933e-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="f933e-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="f933e-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="f933e-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="f933e-p108">Exportiert Daten aus der aktuellen Datenbank in eine Microsoft Excel 97-Datei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="f933e-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f933e-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="f933e-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="f933e-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="f933e-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="f933e-173">01</span><span class="sxs-lookup"><span data-stu-id="f933e-173">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="f933e-174">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="f933e-174">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="f933e-175">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f933e-175">See also</span></span>

[<span data-ttu-id="f933e-176">Verwenden die Einstellung TypeGuessRows für Excel-Treibers</span><span class="sxs-lookup"><span data-stu-id="f933e-176">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
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
ms.openlocfilehash: 7c9a3282f3bb508a4c68ecbd3f2c0465cfee9bac
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603098"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="cb4ec-102">Initialisieren des Microsoft Excel-Treibers</span><span class="sxs-lookup"><span data-stu-id="cb4ec-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="cb4ec-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb4ec-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cb4ec-104"><<<<<<< HEAD bei der Installation des Microsoft® Excel-Treibers, das Setup-Programm schreibt einen Satz von Standardwerten in der Microsoft Windows®-Registrierung im Unterschlüssel Module und -ISAM-Formate.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-104"><<<<<<< HEAD When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="cb4ec-105">Sie sollten diese Einstellungen nicht direkt geändert. Verwenden Sie das Setupprogramm für Ihre Anwendung hinzufügen, entfernen oder ändern Sie diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="cb4ec-106">In den folgenden Abschnitten werden die Initialisierung und ISAM formateinstellungen für die Microsoft Excel-Datenbanktreibers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="cb4ec-107">Initialisierungseinstellungen für Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="cb4ec-107">Microsoft Excel Initialization Settings</span></span>
<span data-ttu-id="cb4ec-108">=== Bei der Installation des Excel-Treibers schreibt das Setupprogramm Standardwerte der Windows-Registrierung im Unterschlüssel Module und -ISAM-Formate.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-108">======= When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="cb4ec-109">Sie sollten diese Einstellungen nicht direkt geändert. Verwenden Sie das Setupprogramm für Ihre Anwendung hinzufügen, entfernen oder ändern Sie diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-109">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="cb4ec-110">In den folgenden Abschnitten werden die Initialisierung und ISAM formateinstellungen für die Microsoft Excel-Datenbanktreibers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-110">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="cb4ec-111">Initialisierungseinstellungen für Excel</span><span class="sxs-lookup"><span data-stu-id="cb4ec-111">Excel Initialization Settings</span></span>
>>>>>>> <span data-ttu-id="cb4ec-112">master</span><span class="sxs-lookup"><span data-stu-id="cb4ec-112">master</span></span>

<span data-ttu-id="cb4ec-113">Die **Konnektivitätsmodul für Access\\Module\\Excel** Ordner enthält initialisierungseinstellungen für Aceexcl.dll-Treiber für den externen Zugriff zu Microsoft Excel-Arbeitsblättern verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-113">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="cb4ec-114">Standardeinstellungen für die Einträge in diesem Ordner sind im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-114">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="cb4ec-115">Das Microsoft Access-Datenbankmodul verwendet die Einträge im Ordner Excel wie folgt.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-115">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb4ec-116">Eintrag</span><span class="sxs-lookup"><span data-stu-id="cb4ec-116">Entry</span></span></p></th>
<th><p><span data-ttu-id="cb4ec-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cb4ec-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-118">Win32</span><span class="sxs-lookup"><span data-stu-id="cb4ec-118">win32</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-p104">Der Speicherort von msexcl40.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-p104">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-122">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="cb4ec-122">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-123">Die Anzahl der Zeilen für den Datentyp überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-123">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="cb4ec-124">Der Datentyp ist die maximale Anzahl von Arten von Daten anhand.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-124">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="cb4ec-125">Wenn eine Tie vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt: Zahl, Währung, Datum, Text, Boolean.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-125">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="cb4ec-126">Wenn Daten, die nicht den Datentyp für die Spalte ermittelten übereinstimmt gefunden werden, wird es als einen <strong>Null</strong> -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-126">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="cb4ec-127">Beim Import Wenn eine Spalte gemischte Datentypen wurde wird die gesamte Spalte gemäß der ImportMixedTypes-Einstellung umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-127">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="cb4ec-128">Die Standardanzahl von Zeilen zu überprüfenden ist 8.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-128">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="cb4ec-129">Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-129">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-130">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="cb4ec-130">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-p106">Mögliche Werte sind MajorityType und Text. Mit MajorityType werden Spalten mit gemischten Datentypen beim Importieren in den vorherrschenden Datentyp konvertiert. Mit Text werden Spalten mit gemischten Datentypen beim Importieren in Text konvertiert. Die Standardeinstellung ist Text. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-p106">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-136">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="cb4ec-136">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-p107">Die Anzahl leerer Zeichen, die vor neuen Daten am Ende eines Arbeitsblatts der Version 3.5 oder Version 4.0 eingefügt werden. Wenn AppendBlankRows beispielsweise auf 4 festgelegt wird, fügt Microsoft Jet 4 leere Zeilen am Ende des Arbeitsblatts ein, und danach erst Zeilen mit Daten. Mögliche ganzzahlige Werte für diese Einstellungen sind die Zahlen 0 bis 16; die Standardeinstellung ist 01 (eine zusätzliche Zeile wird eingefügt). Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-p107">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-141">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="cb4ec-141">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-p108">Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden. Der Wert 00 gibt an, dass in der ersten Zeile keine Spaltennamen verwendet werden; Spaltennamen werden als F1, F2, F3 usw. angezeigt. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-p108">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cb4ec-147">Die **Konnektivitätsmodul für Access\\Module\\Excel 8.0** Ordner enthält die folgenden Einträge, die für Microsoft Excel 97 gelten.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-147">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cb4ec-148">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="cb4ec-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="cb4ec-149">Type</span><span class="sxs-lookup"><span data-stu-id="cb4ec-149">Type</span></span></p></th>
<th><p><span data-ttu-id="cb4ec-150">Wert</span><span class="sxs-lookup"><span data-stu-id="cb4ec-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-151">Engine</span><span class="sxs-lookup"><span data-stu-id="cb4ec-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cb4ec-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-153">Excel</span><span class="sxs-lookup"><span data-stu-id="cb4ec-153">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-154">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="cb4ec-154">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cb4ec-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-156">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="cb4ec-156">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="cb4ec-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb4ec-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-159">01</span><span class="sxs-lookup"><span data-stu-id="cb4ec-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="cb4ec-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb4ec-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-162">00</span><span class="sxs-lookup"><span data-stu-id="cb4ec-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="cb4ec-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="cb4ec-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-165">1</span><span class="sxs-lookup"><span data-stu-id="cb4ec-165">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="cb4ec-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb4ec-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-168">00</span><span class="sxs-lookup"><span data-stu-id="cb4ec-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="cb4ec-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb4ec-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-171">01</span><span class="sxs-lookup"><span data-stu-id="cb4ec-171">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb4ec-172">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="cb4ec-172">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="cb4ec-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-p109">Exportiert Daten aus der aktuellen Datenbank in eine Microsoft Excel 97-Datei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-p109">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb4ec-176">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="cb4ec-176">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb4ec-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="cb4ec-178">01</span><span class="sxs-lookup"><span data-stu-id="cb4ec-178">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="cb4ec-179">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="cb4ec-179">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

<span data-ttu-id="cb4ec-180"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="cb4ec-180"><<<<<<< HEAD</span></span>

=======
## <a name="see-also"></a><span data-ttu-id="cb4ec-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb4ec-181">See also</span></span>

[<span data-ttu-id="cb4ec-182">Verwenden die Einstellung TypeGuessRows für Excel-Treibers</span><span class="sxs-lookup"><span data-stu-id="cb4ec-182">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
>>>>>>> <span data-ttu-id="cb4ec-183">master</span><span class="sxs-lookup"><span data-stu-id="cb4ec-183">master</span></span>

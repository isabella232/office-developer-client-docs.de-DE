---
title: Initialisieren des Microsoft Excel-Treibers
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2fe59f34c04314f70117b3bc7f08d78c2d23ae6d
ms.sourcegitcommit: 62228a65109a9543cd223dfbf326dbf1af256748
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "30179663"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="1fcb0-102">Initialisieren des Microsoft Excel-Treibers</span><span class="sxs-lookup"><span data-stu-id="1fcb0-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="1fcb0-103">**Gilt für**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fcb0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1fcb0-104">Wenn Sie den Excel-Treiber installieren, schreibt das Setup Programm in der Unterschlüssel Engines-und ISAM-Formate in der Windows-Registrierung eine Reihe von Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="1fcb0-105">Sie sollten diese Einstellungen nicht direkt ändern; Verwenden Sie das Setupprogramm für Ihre Anwendung, um diese Einstellungen hinzuzufügen, zu entfernen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="1fcb0-106">In den folgenden Abschnitten werden Initialisierungs-und ISAMformat-Einstellungen für den Microsoft Excel-Datenbanktreiber beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="1fcb0-107">Excel-Initialisierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="1fcb0-107">Excel initialization settings</span></span>

<span data-ttu-id="1fcb0-108">Der **Excel-Ordner\\Access\\Connectivity Engine Engines** enthält Initialisierungseinstellungen für den Aceexcl. dll-Treiber, der für den externen Zugriff auf Microsoft Excel-Arbeitsblätter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="1fcb0-109">Typische Einstellungen für die Einträge in diesem Ordner werden im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="1fcb0-110">Das Microsoft Access-Datenbankmodul verwendet die Einträge im Ordner Excel wie folgt.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fcb0-111">Eintrag</span><span class="sxs-lookup"><span data-stu-id="1fcb0-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="1fcb0-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fcb0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-113">Win32</span><span class="sxs-lookup"><span data-stu-id="1fcb0-113">win32</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-p103">Der Speicherort von msexcl40.dll. Der vollständige Pfad wird bei der Installation festgelegt. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-p103">The location of msexcl40.dll. The full path is determined at the time of installation. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="1fcb0-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-118">Die Anzahl der Zeilen, die für den Datentyp überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="1fcb0-119">Der Datentyp wird anhand der maximalen Anzahl von Datentypen ermittelt.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="1fcb0-120">Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt: Number, Currency, Date, Text, Boolean.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="1fcb0-121">Wenn Daten gefunden werden, die nicht mit dem für die Spalte erkannten Datentyp übereinstimmen, wird er als <strong>null</strong> -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="1fcb0-122">Wenn eine Spalte beim Importieren gemischte Datentypen enthält, wird die gesamte Spalte gemäß der ImportMixedTypes-Einstellung umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="1fcb0-123">Die standardmäßige Anzahl der zu überprüfenden Zeilen ist 8.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="1fcb0-124">Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="1fcb0-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-p105">Mögliche Werte sind MajorityType und Text. Mit MajorityType werden Spalten mit gemischten Datentypen beim Importieren in den vorherrschenden Datentyp konvertiert. Mit Text werden Spalten mit gemischten Datentypen beim Importieren in Text konvertiert. Die Standardeinstellung ist Text. Die Werte sind vom Typ REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-p105">Can be set to MajorityType or Text. If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import. If set to Text, columns of mixed data types will be cast to Text on import. The default is Text. Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="1fcb0-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-p106">Die Anzahl leerer Zeichen, die vor neuen Daten am Ende eines Arbeitsblatts der Version 3.5 oder Version 4.0 eingefügt werden. Wenn AppendBlankRows beispielsweise auf 4 festgelegt wird, fügt Microsoft Jet 4 leere Zeilen am Ende des Arbeitsblatts ein, und danach erst Zeilen mit Daten. Mögliche ganzzahlige Werte für diese Einstellungen sind die Zahlen 0 bis 16; die Standardeinstellung ist 01 (eine zusätzliche Zeile wird eingefügt). Die Werte sind vom Typ REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-p106">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added. For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data. Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended). Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="1fcb0-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-p107">Ein binärer Wert, der angibt, ob die erste Zeile der Tabelle Spaltennamen enthält. Der Wert 01 gibt an, dass beim Importieren die Spaltennamen aus der ersten Zeile verwendet werden. Der Wert 00 gibt an, dass in der ersten Zeile keine Spaltennamen verwendet werden; Spaltennamen werden als F1, F2, F3 usw. angezeigt. Die Standardeinstellung ist 01. Die Werte sind vom Typ REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-p107">A binary value that indicates whether the first row of the table contains column names. A value of 01 indicates that, during import, column names are taken from the first row. A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on. The default is 01. Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1fcb0-142">Der Ordner **Access Connectivity\\Engine\\Engines Excel 8,0** enthält die folgenden einträge, die für Microsoft Excel 97 gelten.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1fcb0-143">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="1fcb0-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="1fcb0-144">Type</span><span class="sxs-lookup"><span data-stu-id="1fcb0-144">Type</span></span></p></th>
<th><p><span data-ttu-id="1fcb0-145">Wert</span><span class="sxs-lookup"><span data-stu-id="1fcb0-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-146">Engine</span><span class="sxs-lookup"><span data-stu-id="1fcb0-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1fcb0-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-148">Excel</span><span class="sxs-lookup"><span data-stu-id="1fcb0-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="1fcb0-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1fcb0-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="1fcb0-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="1fcb0-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fcb0-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-154">01</span><span class="sxs-lookup"><span data-stu-id="1fcb0-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="1fcb0-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fcb0-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-157">00</span><span class="sxs-lookup"><span data-stu-id="1fcb0-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-158">Isamtype</span><span class="sxs-lookup"><span data-stu-id="1fcb0-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="1fcb0-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-160">1</span><span class="sxs-lookup"><span data-stu-id="1fcb0-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="1fcb0-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fcb0-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-163">00</span><span class="sxs-lookup"><span data-stu-id="1fcb0-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="1fcb0-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fcb0-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-166">01</span><span class="sxs-lookup"><span data-stu-id="1fcb0-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1fcb0-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="1fcb0-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="1fcb0-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-p108">Exportiert Daten aus der aktuellen Datenbank in eine Microsoft Excel 97-Datei. Dabei werden die Daten überschrieben, wenn sie in eine vorhandene Datei exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-p108">Export data from the current database into a Microsoft Excel 97 file. This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1fcb0-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="1fcb0-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="1fcb0-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="1fcb0-173">01</span><span class="sxs-lookup"><span data-stu-id="1fcb0-173">01</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="1fcb0-174">Verwenden der TypeGuessRows-Einstellung für den Excel-Treiber</span><span class="sxs-lookup"><span data-stu-id="1fcb0-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="1fcb0-175">Bei Verwendung des Microsoft Excel-Treibers können Sie mit dem **TypeGuessRows** -Registrierungswert konfigurieren, wie viele Zeilen für den Datentyp überprüft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="1fcb0-176">Der **TypeGuessRows** -Wert befindet sich unter dem folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016taboffice-2016"></a>[<span data-ttu-id="1fcb0-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="1fcb0-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="1fcb0-178">Für eine MSI-Installation von Office</span><span class="sxs-lookup"><span data-stu-id="1fcb0-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="1fcb0-179">Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="1fcb0-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="1fcb0-181">Für 32-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="1fcb0-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="1fcb0-183">Für eine Klick-und-Los-Installation von Office</span><span class="sxs-lookup"><span data-stu-id="1fcb0-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="1fcb0-184">Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="1fcb0-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="1fcb0-186">Für 32-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="1fcb0-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="1fcb0-188">Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht).</span><span class="sxs-lookup"><span data-stu-id="1fcb0-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="1fcb0-189">Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="1fcb0-190">Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="1fcb0-191">Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="1fcb0-192">Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="1fcb0-193">Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="1fcb0-194">Zahl</span><span class="sxs-lookup"><span data-stu-id="1fcb0-194">Number</span></span>
- <span data-ttu-id="1fcb0-195">Währung</span><span class="sxs-lookup"><span data-stu-id="1fcb0-195">Currency</span></span>
- <span data-ttu-id="1fcb0-196">Datum</span><span class="sxs-lookup"><span data-stu-id="1fcb0-196">Date</span></span>
- <span data-ttu-id="1fcb0-197">Text</span><span class="sxs-lookup"><span data-stu-id="1fcb0-197">Text</span></span>
- <span data-ttu-id="1fcb0-198">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="1fcb0-198">Boolean</span></span>

<span data-ttu-id="1fcb0-199">Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="1fcb0-200">Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013taboffice-2013"></a>[<span data-ttu-id="1fcb0-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="1fcb0-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="1fcb0-202">Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="1fcb0-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="1fcb0-204">Für 32-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="1fcb0-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="1fcb0-206">Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht).</span><span class="sxs-lookup"><span data-stu-id="1fcb0-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="1fcb0-207">Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="1fcb0-208">Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="1fcb0-209">Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="1fcb0-210">Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="1fcb0-211">Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="1fcb0-212">Zahl</span><span class="sxs-lookup"><span data-stu-id="1fcb0-212">Number</span></span>
- <span data-ttu-id="1fcb0-213">Währung</span><span class="sxs-lookup"><span data-stu-id="1fcb0-213">Currency</span></span>
- <span data-ttu-id="1fcb0-214">Datum</span><span class="sxs-lookup"><span data-stu-id="1fcb0-214">Date</span></span>
- <span data-ttu-id="1fcb0-215">Text</span><span class="sxs-lookup"><span data-stu-id="1fcb0-215">Text</span></span>
- <span data-ttu-id="1fcb0-216">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="1fcb0-216">Boolean</span></span>

<span data-ttu-id="1fcb0-217">Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="1fcb0-218">Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010taboffice-2010"></a>[<span data-ttu-id="1fcb0-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="1fcb0-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="1fcb0-220">Für 32-Bit-Office auf 32-Bit-Windows oder 64-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="1fcb0-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="1fcb0-222">Für 32-Bit-Office unter 64-Bit-Windows:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="1fcb0-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access-Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="1fcb0-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="1fcb0-224">Die standardmäßige Anzahl der zu überprüfenden Zeilen ist **8** (acht).</span><span class="sxs-lookup"><span data-stu-id="1fcb0-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="1fcb0-225">Wenn Sie den **TypeGuessRows** -Wert auf **0** (null) festlegen, überprüft der Excel-Treiber die ersten 16.384-Zeilen nach dem Datentyp.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="1fcb0-226">Wenn Sie mehr als 16.384 Zeilen überprüfen möchten, legen Sie **TypeGuessRows** auf einen Wert fest, der auf Ihrem gewünschten Range basiert.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="1fcb0-227">Legen Sie **TypeGuessRows** auf 1.048.576 (die maximale Anzahl von Zeilen, die in Excel zulässig sind) fest, um alle Zeilen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="1fcb0-228">Der Datentyp wird durch die maximale Anzahl von Datentypen bestimmt, die gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="1fcb0-229">Wenn ein Tie-Wert vorhanden ist, wird der Datentyp in der folgenden Reihenfolge bestimmt:</span><span class="sxs-lookup"><span data-stu-id="1fcb0-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="1fcb0-230">Zahl</span><span class="sxs-lookup"><span data-stu-id="1fcb0-230">Number</span></span>
- <span data-ttu-id="1fcb0-231">Währung</span><span class="sxs-lookup"><span data-stu-id="1fcb0-231">Currency</span></span>
- <span data-ttu-id="1fcb0-232">Datum</span><span class="sxs-lookup"><span data-stu-id="1fcb0-232">Date</span></span>
- <span data-ttu-id="1fcb0-233">Text</span><span class="sxs-lookup"><span data-stu-id="1fcb0-233">Text</span></span>
- <span data-ttu-id="1fcb0-234">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="1fcb0-234">Boolean</span></span>

<span data-ttu-id="1fcb0-235">Wenn Daten gefunden werden, die nicht mit dem geschätzten Datentyp für die Spalte übereinstimmen, werden diese Daten als **null** -Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="1fcb0-236">Wenn während eines Imports eine Spalte gemischte Datentypen enthält, wird die gesamte Spalte in den Datentyp umgewandelt, der von der **ImportMixedTypes** -Einstellung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="1fcb0-237">[!HINWEIS] Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="1fcb0-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


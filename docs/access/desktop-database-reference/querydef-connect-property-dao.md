---
title: QueryDef.Connect-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698274"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="fe648-102">QueryDef.Connect-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="fe648-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="fe648-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe648-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe648-p101">Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="fe648-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe648-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe648-106">Syntax</span></span>

<span data-ttu-id="fe648-107">*Ausdruck* . Eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="fe648-107">*expression* .Connect</span></span>

<span data-ttu-id="fe648-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="fe648-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe648-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe648-109">Remarks</span></span>

<span data-ttu-id="fe648-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="fe648-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="fe648-112">Sie können eine SQL-Pass-Through-Abfrage für eine Tabelle ausführen, die mit Ihrer Microsoft Access-Datenbankdatei verknüpft ist, indem Sie zunächst die **Connect**-Eigenschaft der Datenbank der verknüpften Tabelle auf eine gültige ODBC-Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe648-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="fe648-p103">Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="fe648-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="fe648-115">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fe648-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fe648-116">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="fe648-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="fe648-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="fe648-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="fe648-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fe648-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fe648-119">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="fe648-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="fe648-120">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="fe648-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="fe648-121">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="fe648-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="fe648-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="fe648-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="fe648-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="fe648-124">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="fe648-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="fe648-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="fe648-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="fe648-127">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="fe648-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="fe648-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="fe648-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="fe648-130">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="fe648-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="fe648-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="fe648-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="fe648-133">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="fe648-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="fe648-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="fe648-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="fe648-136">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="fe648-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="fe648-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="fe648-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="fe648-139">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="fe648-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="fe648-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="fe648-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="fe648-142">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="fe648-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="fe648-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="fe648-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="fe648-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="fe648-145">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="fe648-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-146">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="fe648-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="fe648-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="fe648-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="fe648-148">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="fe648-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="fe648-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="fe648-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="fe648-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="fe648-151">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="fe648-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-152">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="fe648-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="fe648-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="fe648-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="fe648-154">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="fe648-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="fe648-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="fe648-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="fe648-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="fe648-157">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="fe648-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="fe648-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="fe648-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="fe648-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="fe648-160">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="fe648-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-161">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="fe648-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="fe648-162">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="fe648-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="fe648-163">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="fe648-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-164">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="fe648-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="fe648-165">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="fe648-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="fe648-166">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-167">Text</span><span class="sxs-lookup"><span data-stu-id="fe648-167">Text</span></span></p></td>
<td><p><span data-ttu-id="fe648-168">Text;</span><span class="sxs-lookup"><span data-stu-id="fe648-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="fe648-169">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="fe648-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fe648-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="fe648-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="fe648-171">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="fe648-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="fe648-172">Keine</span><span class="sxs-lookup"><span data-stu-id="fe648-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fe648-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="fe648-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="fe648-174">Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="fe648-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="fe648-175">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="fe648-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fe648-176">Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="fe648-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="fe648-177">Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="fe648-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="fe648-178">Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fe648-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="fe648-179">Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fe648-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="fe648-180">Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fe648-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="fe648-181">Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.</span><span class="sxs-lookup"><span data-stu-id="fe648-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="fe648-182">Für ein **QueryDef** -Objekt in einer Microsoft Access-Arbeitsbereich können Sie die **Connect** -Eigenschaft mit der ReturnsRecords-Eigenschaft verwenden, um eine ODBC SQL Pass-Through-Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fe648-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="fe648-183">Die "databasetype" der Verbindungszeichenfolge ist "ODBC;", und den Rest der Zeichenfolge enthält Informationen zu den ODBC-Treiber verwendet, um die remote-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="fe648-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="fe648-184">Weitere Informationen finden Sie in der Dokumentation des Treibers.</span><span class="sxs-lookup"><span data-stu-id="fe648-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="fe648-185">Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe648-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="fe648-186">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="fe648-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>



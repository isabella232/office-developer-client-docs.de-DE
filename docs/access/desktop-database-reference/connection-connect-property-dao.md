---
title: Connection.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8dc64341ddd48f9f973354c162811dd7f8eb6f3f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886893"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="e8ba9-102">Connection.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8ba9-102">Connection.Connect Property (DAO)</span></span>


<span data-ttu-id="e8ba9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8ba9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8ba9-p101">Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Verbindung bereitstellt, oder gibt den Wert zurück. **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ba9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8ba9-106">Syntax</span></span>

<span data-ttu-id="e8ba9-107">*Ausdruck* . Eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="e8ba9-107">*expression* .Connect</span></span>

<span data-ttu-id="e8ba9-108">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ba9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e8ba9-109">Remarks</span></span>

<span data-ttu-id="e8ba9-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="e8ba9-112">Wenn Sie eine SQL Pass-Through-Abfrage zu einer Tabelle ausführen möchten, die mit der Microsoft Access-Datenbankdatei verknüpft ist, müssen Sie zuerst die **Connect**-Eigenschaft der Datenbank, zu der die verknüpfte Tabelle gehört, auf eine gültige ODBC-Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="e8ba9-113">Bei einem **TableDef**-Objekt, das eine verknüpfte Tabelle darstellt, besteht die Einstellung der **Connect**-Eigenschaft aus einem oder zwei Teilen (dem Bezeichner eines Datenbanktyps und dem Pfad zur Datenbank), die jeweils mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="e8ba9-p103">Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="e8ba9-116">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8ba9-117">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="e8ba9-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="e8ba9-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="e8ba9-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="e8ba9-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e8ba9-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-120">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="e8ba9-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-121">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="e8ba9-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-122">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="e8ba9-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="e8ba9-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-125">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="e8ba9-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-128">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="e8ba9-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-131">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="e8ba9-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-134">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="e8ba9-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-137">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="e8ba9-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-140">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="e8ba9-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-143">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="e8ba9-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="e8ba9-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-146">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="e8ba9-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-147">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="e8ba9-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-149">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="e8ba9-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="e8ba9-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-152">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="e8ba9-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-153">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="e8ba9-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-155">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="e8ba9-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="e8ba9-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-158">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="e8ba9-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="e8ba9-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-161">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="e8ba9-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-162">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="e8ba9-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-163">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-164">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="e8ba9-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-165">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="e8ba9-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-166">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-167">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-168">Text</span><span class="sxs-lookup"><span data-stu-id="e8ba9-168">Text</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-169">Text;</span><span class="sxs-lookup"><span data-stu-id="e8ba9-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-170">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="e8ba9-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8ba9-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="e8ba9-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-172">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="e8ba9-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-173">Keine</span><span class="sxs-lookup"><span data-stu-id="e8ba9-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8ba9-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="e8ba9-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-175">Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="e8ba9-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="e8ba9-176">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="e8ba9-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e8ba9-177">Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="e8ba9-178">Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="e8ba9-179">Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="e8ba9-180">Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="e8ba9-181">Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="e8ba9-182">Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="e8ba9-183">Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect** -Eigenschaft eine Null-Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="e8ba9-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="e8ba9-184">Sie können die **Connect** -Eigenschaft für ein **Database** -Objekt festlegen, durch die Bereitstellung ein Quellargument, um die **OpenDatabase** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="e8ba9-185">Überprüfen Sie die Einstellung, um den Typ, den Pfad, die Benutzer-ID, das Kennwort oder die ODBC-Datenquelle der Datenbank zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="e8ba9-186">Für ein **QueryDef** -Objekt in einer Microsoft Access-Arbeitsbereich können Sie die **Connect** -Eigenschaft mit der ReturnsRecords-Eigenschaft verwenden, um eine ODBC SQL Pass-Through-Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="e8ba9-187">Die "databasetype" der Verbindungszeichenfolge ist "ODBC;", und den Rest der Zeichenfolge enthält Informationen zu den ODBC-Treiber verwendet, um die remote-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="e8ba9-188">Weitere Informationen finden Sie in der Dokumentation des Treibers.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="e8ba9-189">Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="e8ba9-190">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="e8ba9-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>



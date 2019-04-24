---
title: Connection. Connect-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295926"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="643c8-102">Connection. Connect-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="643c8-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="643c8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="643c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="643c8-104">Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Verbindung bereitstellt, oder gibt den Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="643c8-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="643c8-105">**String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="643c8-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="643c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="643c8-106">Syntax</span></span>

<span data-ttu-id="643c8-107">*Ausdruck* . Verbinden</span><span class="sxs-lookup"><span data-stu-id="643c8-107">*expression* .Connect</span></span>

<span data-ttu-id="643c8-108">*Ausdruck* Eine Variable, die ein **Connection** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="643c8-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="643c8-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="643c8-109">Remarks</span></span>

<span data-ttu-id="643c8-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="643c8-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="643c8-112">Wenn Sie eine SQL Pass-Through-Abfrage zu einer Tabelle ausführen möchten, die mit der Microsoft Access-Datenbankdatei verknüpft ist, müssen Sie zuerst die **Connect**-Eigenschaft der Datenbank, zu der die verknüpfte Tabelle gehört, auf eine gültige ODBC-Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="643c8-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="643c8-113">Bei einem **TableDef**-Objekt, das eine verknüpfte Tabelle darstellt, besteht die Einstellung der **Connect**-Eigenschaft aus einem oder zwei Teilen (dem Bezeichner eines Datenbanktyps und dem Pfad zur Datenbank), die jeweils mit einem Semikolon enden.</span><span class="sxs-lookup"><span data-stu-id="643c8-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="643c8-114">Der Pfad, wie in der folgenden Tabelle dargestellt, ist der vollständige Pfad für das Verzeichnis, das die Datenbankdateien enthält, und es muss der Bezeichner DATABASE = vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="643c8-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="643c8-115">In einigen Fällen (wie in den Datenbanken von Microsoft Excel und Microsoft Access-Datenbankmodul) sollten Sie einen bestimmten Dateinamen in das Argument Datenbankpfad aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="643c8-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="643c8-116">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect**-Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="643c8-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="643c8-117">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="643c8-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="643c8-118">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="643c8-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="643c8-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="643c8-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="643c8-120">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="643c8-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="643c8-121">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="643c8-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="643c8-122">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="643c8-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="643c8-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="643c8-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="643c8-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="643c8-125">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="643c8-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="643c8-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="643c8-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="643c8-128">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="643c8-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="643c8-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="643c8-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="643c8-131">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="643c8-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="643c8-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="643c8-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="643c8-134">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="643c8-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="643c8-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="643c8-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="643c8-137">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="643c8-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="643c8-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="643c8-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="643c8-140">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="643c8-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="643c8-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="643c8-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="643c8-143">Laufwerk: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="643c8-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="643c8-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="643c8-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="643c8-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="643c8-146">Laufwerk: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="643c8-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-147">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="643c8-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="643c8-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="643c8-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="643c8-149">Laufwerk: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="643c8-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="643c8-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="643c8-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="643c8-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="643c8-152">Laufwerk: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="643c8-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-153">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="643c8-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="643c8-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="643c8-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="643c8-155">Laufwerk: \ path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="643c8-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="643c8-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="643c8-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="643c8-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="643c8-158">Laufwerk: \ path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="643c8-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="643c8-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="643c8-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="643c8-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="643c8-161">Laufwerk: \ path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="643c8-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-162">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="643c8-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="643c8-163">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="643c8-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="643c8-164">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="643c8-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-165">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="643c8-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="643c8-166">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="643c8-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="643c8-167">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-168">Text</span><span class="sxs-lookup"><span data-stu-id="643c8-168">Text</span></span></p></td>
<td><p><span data-ttu-id="643c8-169">Text;</span><span class="sxs-lookup"><span data-stu-id="643c8-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="643c8-170">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="643c8-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="643c8-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="643c8-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="643c8-172">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="643c8-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="643c8-173">Keine</span><span class="sxs-lookup"><span data-stu-id="643c8-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="643c8-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="643c8-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="643c8-175">Exchange 4,0; MAPILEVEL = folderPath; [BASISTYP = {0 | 1}]; [PROFILE = Profil;] [PWD = Kennwort;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="643c8-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="643c8-176">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="643c8-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="643c8-177">Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="643c8-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="643c8-178">Wenn ein Kennwort erforderlich ist, aber in der **Connect**-Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="643c8-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="643c8-p104">Für Daten in Microsoft Exchange muss für den erforderlichen MAPILEVEL-Schlüssel ein vollständig aufgelöster Ordnerpfad angegeben werden (z. B. "Mailbox - Pat SmithIAlpha/Today"). Der Pfad umfasst nicht den Namen des Ordners, der als Tabelle geöffnet wird. Der Name dieses Ordners muss stattdessen als name-Argument der **CreateTable**-Methode angegeben werden. Zum Öffnen eines Ordners muss der TABLETYPE-Schlüssel auf "0" gesetzt werden (Standard), zum Öffnen eines Adressbuchs muss er den Wert "1" erhalten. Der PROFILE-Schlüssel erhält standardmäßig den Wert des aktuell verwendeten Profils.</span><span class="sxs-lookup"><span data-stu-id="643c8-p104">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today"). The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method. The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book. The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="643c8-183">Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect**-Eigenschaft eine Null-Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="643c8-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="643c8-184">Sie können die **Connect** -Eigenschaft für ein **Database** -Objekt festlegen, indem Sie der OpenDatabase-Methode ein Source-Argument bereitstellen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="643c8-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="643c8-185">Überprüfen Sie die Einstellung, um den Typ, den Pfad, die Benutzer-ID, das Kennwort oder die ODBC-Datenquelle der Datenbank zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="643c8-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="643c8-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span><span class="sxs-lookup"><span data-stu-id="643c8-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="643c8-187">Der DatabaseType der Verbindungszeichenfolge ist "ODBC;", und der Rest der Zeichenfolge enthält spezifische Informationen für den ODBC-Treiber, der für den Zugriff auf die Remotedaten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="643c8-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="643c8-188">For more information, see the documentation for the specific driver.</span><span class="sxs-lookup"><span data-stu-id="643c8-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="643c8-189">Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="643c8-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="643c8-190">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="643c8-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>



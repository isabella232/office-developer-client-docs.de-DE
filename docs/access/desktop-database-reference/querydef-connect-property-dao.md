---
title: QueryDef.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1aef24850a2dfa9eeb801708ea773087b9d1ff40
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871444"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="ff636-102">QueryDef.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ff636-102">QueryDef.Connect Property (DAO)</span></span>


<span data-ttu-id="ff636-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff636-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff636-p101">Legt einen Wert fest, der Informationen über die Quelle der in einer Pass-Through-Abfrage verwendeten Datenbank bereitstellt, oder gibt den betreffenden Wert zurück. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="ff636-p101">Sets or returns a value that provides information about the source of database used in a pass-through query. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff636-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff636-106">Syntax</span></span>

<span data-ttu-id="ff636-107">*Ausdruck* . Eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="ff636-107">*expression* .Connect</span></span>

<span data-ttu-id="ff636-108">*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff636-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff636-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff636-109">Remarks</span></span>

<span data-ttu-id="ff636-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="ff636-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="ff636-112">Sie können eine SQL-Pass-Through-Abfrage für eine Tabelle ausführen, die mit Ihrer Microsoft Access-Datenbankdatei verknüpft ist, indem Sie zunächst die **Connect**-Eigenschaft der Datenbank der verknüpften Tabelle auf eine gültige ODBC-Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff636-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="ff636-p103">Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="ff636-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="ff636-115">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ff636-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff636-116">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="ff636-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="ff636-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="ff636-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="ff636-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ff636-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff636-119">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="ff636-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="ff636-120">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="ff636-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="ff636-121">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="ff636-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="ff636-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="ff636-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="ff636-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="ff636-124">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="ff636-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="ff636-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="ff636-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="ff636-127">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="ff636-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="ff636-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="ff636-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ff636-130">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="ff636-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="ff636-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="ff636-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="ff636-133">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="ff636-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="ff636-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="ff636-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="ff636-136">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="ff636-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="ff636-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="ff636-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="ff636-139">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="ff636-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="ff636-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="ff636-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="ff636-142">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="ff636-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="ff636-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="ff636-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="ff636-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="ff636-145">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="ff636-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-146">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="ff636-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="ff636-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="ff636-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ff636-148">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="ff636-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="ff636-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="ff636-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="ff636-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="ff636-151">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="ff636-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-152">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="ff636-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="ff636-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="ff636-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="ff636-154">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="ff636-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="ff636-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="ff636-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="ff636-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="ff636-157">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="ff636-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="ff636-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="ff636-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="ff636-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="ff636-160">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="ff636-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-161">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="ff636-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="ff636-162">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="ff636-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="ff636-163">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="ff636-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-164">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="ff636-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="ff636-165">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="ff636-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="ff636-166">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-167">Text</span><span class="sxs-lookup"><span data-stu-id="ff636-167">Text</span></span></p></td>
<td><p><span data-ttu-id="ff636-168">Text;</span><span class="sxs-lookup"><span data-stu-id="ff636-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="ff636-169">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="ff636-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff636-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="ff636-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="ff636-171">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="ff636-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="ff636-172">Keine</span><span class="sxs-lookup"><span data-stu-id="ff636-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff636-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="ff636-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="ff636-174">Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="ff636-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="ff636-175">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="ff636-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff636-176">Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="ff636-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="ff636-177">Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="ff636-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="ff636-178">Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff636-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="ff636-179">Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ff636-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="ff636-180">Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ff636-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="ff636-181">Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.</span><span class="sxs-lookup"><span data-stu-id="ff636-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="ff636-182">Für ein **QueryDef** -Objekt in einer Microsoft Access-Arbeitsbereich können Sie die **Connect** -Eigenschaft mit der ReturnsRecords-Eigenschaft verwenden, um eine ODBC SQL Pass-Through-Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ff636-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="ff636-183">Die "databasetype" der Verbindungszeichenfolge ist "ODBC;", und den Rest der Zeichenfolge enthält Informationen zu den ODBC-Treiber verwendet, um die remote-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ff636-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="ff636-184">Weitere Informationen finden Sie in der Dokumentation des Treibers.</span><span class="sxs-lookup"><span data-stu-id="ff636-184">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="ff636-185">Vor dem Festlegen der <STRONG>ReturnsRecords</STRONG>-Eigenschaft müssen Sie die <STRONG>Connect</STRONG>-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="ff636-185">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="ff636-186">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="ff636-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>



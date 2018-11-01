---
title: Database.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 82b75af86d45b8711660d769607c46b626477bac
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872795"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="09a01-102">Database.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="09a01-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="09a01-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09a01-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09a01-p101">Legt einen Wert fest, der Informationen zur Quelle einer geöffneten Datenbank bereitstellt, oder gibt den Wert zurück. **String**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="09a01-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a01-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="09a01-106">Syntax</span></span>

<span data-ttu-id="09a01-107">*Ausdruck* . Eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="09a01-107">*expression* .Connect</span></span>

<span data-ttu-id="09a01-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="09a01-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="09a01-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09a01-109">Remarks</span></span>

<span data-ttu-id="09a01-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="09a01-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="09a01-112">Sie können eine SQL-Pass-Through-Abfrage für eine Tabelle ausführen, die mit Ihrer Microsoft Access-Datenbankdatei verknüpft ist, indem Sie zunächst die **Connect**-Eigenschaft der Datenbank der verknüpften Tabelle auf eine gültige ODBC-Verbindungszeichenfolge festlegen.</span><span class="sxs-lookup"><span data-stu-id="09a01-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="09a01-p103">Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="09a01-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="09a01-115">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="09a01-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09a01-116">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="09a01-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="09a01-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="09a01-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="09a01-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="09a01-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a01-119">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="09a01-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="09a01-120">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="09a01-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="09a01-121">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="09a01-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="09a01-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="09a01-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="09a01-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="09a01-124">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="09a01-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="09a01-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="09a01-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="09a01-127">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="09a01-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="09a01-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="09a01-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="09a01-130">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="09a01-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="09a01-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="09a01-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="09a01-133">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="09a01-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="09a01-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="09a01-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="09a01-136">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="09a01-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="09a01-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="09a01-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="09a01-139">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="09a01-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="09a01-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="09a01-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="09a01-142">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="09a01-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="09a01-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="09a01-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="09a01-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="09a01-145">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="09a01-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-146">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="09a01-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="09a01-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="09a01-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="09a01-148">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="09a01-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="09a01-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="09a01-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="09a01-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="09a01-151">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="09a01-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-152">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="09a01-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="09a01-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="09a01-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="09a01-154">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="09a01-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="09a01-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="09a01-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="09a01-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="09a01-157">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="09a01-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="09a01-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="09a01-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="09a01-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="09a01-160">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="09a01-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-161">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="09a01-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="09a01-162">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="09a01-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="09a01-163">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="09a01-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-164">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="09a01-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="09a01-165">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="09a01-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="09a01-166">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-167">Text</span><span class="sxs-lookup"><span data-stu-id="09a01-167">Text</span></span></p></td>
<td><p><span data-ttu-id="09a01-168">Text;</span><span class="sxs-lookup"><span data-stu-id="09a01-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="09a01-169">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="09a01-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a01-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="09a01-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="09a01-171">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="09a01-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="09a01-172">Keine</span><span class="sxs-lookup"><span data-stu-id="09a01-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a01-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="09a01-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="09a01-174">Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="09a01-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="09a01-175">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="09a01-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09a01-176">Wenn der Bezeichner nur "ODBC;" lautet, zeigt der ODBC-Treiber ein Dialogfeld an, in dem alle registrierten ODBC-Datenquellennamen aufgeführt werden, sodass der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="09a01-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="09a01-177">Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="09a01-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="09a01-178">Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="09a01-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="09a01-179">Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="09a01-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="09a01-180">Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="09a01-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="09a01-181">Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.</span><span class="sxs-lookup"><span data-stu-id="09a01-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="09a01-182">Sie können die **Connect** -Eigenschaft für ein **Database** -Objekt festlegen, durch die Bereitstellung ein Quellargument, um die **OpenDatabase** -Methode.</span><span class="sxs-lookup"><span data-stu-id="09a01-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="09a01-183">Überprüfen Sie die Einstellung, um den Typ, den Pfad, die Benutzer-ID, das Kennwort oder die ODBC-Datenquelle der Datenbank zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="09a01-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="09a01-184">Sie müssen die **Connect**-Eigenschaft vor der **ReturnsRecords**-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="09a01-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="09a01-185">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="09a01-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>



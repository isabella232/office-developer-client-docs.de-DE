---
title: TableDef.Connect-Eigenschaft (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 322b59c6556b73186fe4034e64c75d9104d29560
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926899"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="3fd81-102">TableDef.Connect-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="3fd81-102">TableDef.Connect property (DAO)</span></span>


<span data-ttu-id="3fd81-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3fd81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3fd81-p101">Legt einen Wert fest, der Informationen über eine verknüpfte Tabelle bereitstellt, oder gibt den betreffenden Wert zurück. **String** -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="3fd81-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd81-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd81-106">Syntax</span></span>

<span data-ttu-id="3fd81-107">*Ausdruck* . Eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="3fd81-107">*expression* .Connect</span></span>

<span data-ttu-id="3fd81-108">*Ausdruck* Eine Variable, die ein **TableDef** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="3fd81-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd81-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3fd81-109">Remarks</span></span>

<span data-ttu-id="3fd81-p102">Die Einstellung der **Connect** -Eigenschaft ist ein **String** -Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect** -Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="3fd81-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="3fd81-112">Bei einem **TableDef** -Objekt, das eine verknüpfte Tabelle darstellt, besteht die **Connect** -Eigenschaft aus einem oder zwei Teilen (ein Datenbanktypbezeichner und ein Pfad für die Datenbank). Beide Teile enden mit einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="3fd81-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="3fd81-p103">Der Pfad ist der vollständige Pfadname für das Verzeichnis, das die Datenbankdateien enthält, wie in der folgenden Tabelle dargestellt. Der Pfadname muss mit dem Bezeichner DATABASE= beginnen. In einigen Fällen (wie bei Microsoft Excel- und Microsoft Access-Datenbanken) muss ein spezifischer Dateiname in das Argument des Datenbankpfads einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="3fd81-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="3fd81-115">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect** -Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3fd81-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3fd81-116">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="3fd81-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="3fd81-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="3fd81-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="3fd81-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3fd81-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-119">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="3fd81-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="3fd81-120">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="3fd81-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="3fd81-121">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="3fd81-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="3fd81-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="3fd81-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="3fd81-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-124">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="3fd81-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="3fd81-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="3fd81-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-127">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="3fd81-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="3fd81-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="3fd81-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-130">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="3fd81-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="3fd81-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="3fd81-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-133">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="3fd81-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="3fd81-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="3fd81-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-136">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="3fd81-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="3fd81-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="3fd81-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-139">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="3fd81-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="3fd81-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="3fd81-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-142">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="3fd81-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="3fd81-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="3fd81-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="3fd81-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-145">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="3fd81-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-146">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="3fd81-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="3fd81-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="3fd81-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-148">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="3fd81-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="3fd81-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="3fd81-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="3fd81-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-151">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="3fd81-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-152">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="3fd81-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="3fd81-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="3fd81-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-154">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="3fd81-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="3fd81-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="3fd81-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="3fd81-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-157">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="3fd81-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="3fd81-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="3fd81-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="3fd81-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-160">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="3fd81-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-161">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="3fd81-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="3fd81-162">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="3fd81-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-163">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="3fd81-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-164">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="3fd81-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="3fd81-165">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="3fd81-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-166">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-167">Text</span><span class="sxs-lookup"><span data-stu-id="3fd81-167">Text</span></span></p></td>
<td><p><span data-ttu-id="3fd81-168">Text;</span><span class="sxs-lookup"><span data-stu-id="3fd81-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="3fd81-169">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="3fd81-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fd81-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="3fd81-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="3fd81-171">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="3fd81-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="3fd81-172">Keine</span><span class="sxs-lookup"><span data-stu-id="3fd81-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fd81-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="3fd81-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="3fd81-174">Exchange 4.0; MAPILEVEL = Folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = Profile;] [PWD = Password;] [DATABASE = Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="3fd81-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="3fd81-175">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="3fd81-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fd81-176">Wenn ein Kennwort erforderlich ist, aber in der **Connect** -Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3fd81-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="3fd81-177">Für Daten in Microsoft Exchange sollte der erforderliche MAPILEVEL-Schlüssel in einen vollständig aufgelöster Ordnerpfad (beispielsweise "Postfach – Pat SmithIAlpha/heute") festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3fd81-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="3fd81-178">Der Pfad schließt nicht den Namen des Ordners ein, der als Tabelle geöffnet wird. der Name dieses Ordners sollten stattdessen als Namenargument für die **CreateTable** -Methode angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3fd81-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="3fd81-179">Öffnen Sie einen Ordner (Standard) oder "1" zum Öffnen eines Adressbuchs sollte der TABLETYPE-Schlüssel auf "0" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3fd81-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="3fd81-180">Die wichtigsten profilstandardeinstellungen Profil verwenden derzeit.</span><span class="sxs-lookup"><span data-stu-id="3fd81-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="3fd81-181">Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect** -Eigenschaft eine Null-Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="3fd81-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="3fd81-182">[!HINWEIS] Vor dem Festlegen der <STRONG>ReturnsRecords</STRONG> -Eigenschaft müssen Sie die <STRONG>Connect</STRONG> -Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="3fd81-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="3fd81-183">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="3fd81-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>



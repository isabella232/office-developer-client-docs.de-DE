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
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314385"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="f051f-102">TableDef.Connect-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="f051f-102">TableDef.Connect Property (DAO)</span></span>

<span data-ttu-id="f051f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f051f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f051f-104">Legt einen Wert fest, der Informationen über eine verknüpfte Tabelle bereitstellt, oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f051f-104">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="f051f-105">**Zeichenfolge** mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f051f-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f051f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f051f-106">Syntax</span></span>

<span data-ttu-id="f051f-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="f051f-107">expression  . Connect</span></span>

<span data-ttu-id="f051f-108">*Ausdruck* Eine Variable, die ein **TableDef**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f051f-108">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f051f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f051f-109">Remarks</span></span>

<span data-ttu-id="f051f-p102">Die Einstellung der **Connect**-Eigenschaft ist ein **String**-Wert, der aus einem Datenbanktypbezeichner und null oder mehreren durch Semikolons getrennten Parametern besteht. Die **Connect**-Eigenschaft übergibt bei Bedarf zusätzliche Informationen an ODBC- und bestimmte ISAM-Treiber.</span><span class="sxs-lookup"><span data-stu-id="f051f-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="f051f-112">Bei einem **TableDef** -Objekt, das eine verknüpfte Tabelle darstellt, besteht die **Connect** -Eigenschaft aus einem oder zwei Teilen (ein Datenbanktypbezeichner und ein Pfad für die Datenbank). Beide Teile enden mit einem Semikolon.</span><span class="sxs-lookup"><span data-stu-id="f051f-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="f051f-113">Der Pfad, wie in der folgenden Tabelle dargestellt, ist der vollständige Pfad für das Verzeichnis, das die Datenbankdateien enthält, und muss den Bezeichner DATABASE= vorangestellt haben.</span><span class="sxs-lookup"><span data-stu-id="f051f-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span> <span data-ttu-id="f051f-114">In einigen Fällen (z. B. bei Datenbanken in Microsoft Excel und Microsoft Access-Datenbankmodulen) sollten Sie einen bestimmten Dateinamen in das Argument mit dem Datenbankpfad einschließen.</span><span class="sxs-lookup"><span data-stu-id="f051f-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier  . In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="f051f-115">In der folgenden Tabelle sind die möglichen Datenbanktypen und ihre entsprechenden Datenbankbezeichner und Pfadnamen für die Einstellungen der **Connect**-Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f051f-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f051f-116">Datenbanktyp</span><span class="sxs-lookup"><span data-stu-id="f051f-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="f051f-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f051f-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="f051f-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f051f-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f051f-119">Microsoft Access-Datenbank</span><span class="sxs-lookup"><span data-stu-id="f051f-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="f051f-120">[Datenbank];</span><span class="sxs-lookup"><span data-stu-id="f051f-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="f051f-121">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="f051f-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="f051f-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="f051f-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="f051f-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="f051f-124">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="f051f-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="f051f-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="f051f-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="f051f-127">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="f051f-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="f051f-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="f051f-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f051f-130">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="f051f-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="f051f-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="f051f-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="f051f-133">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="f051f-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="f051f-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="f051f-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="f051f-136">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="f051f-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="f051f-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="f051f-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="f051f-139">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="f051f-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="f051f-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="f051f-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="f051f-142">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="f051f-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="f051f-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="f051f-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="f051f-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="f051f-145">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="f051f-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-146">Microsoft Excel 5.0 oder Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="f051f-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="f051f-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="f051f-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="f051f-148">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="f051f-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="f051f-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="f051f-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="f051f-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="f051f-151">Laufwerk:\Pfad\Dateiname.xls</span><span class="sxs-lookup"><span data-stu-id="f051f-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-152">Lotus 1-2-3 WKS und WK1</span><span class="sxs-lookup"><span data-stu-id="f051f-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="f051f-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="f051f-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="f051f-154">Laufwerk:\Pfad\Dateiname.wk1</span><span class="sxs-lookup"><span data-stu-id="f051f-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="f051f-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="f051f-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="f051f-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="f051f-157">Laufwerk:\Pfad\Dateiname.wk3</span><span class="sxs-lookup"><span data-stu-id="f051f-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="f051f-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="f051f-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="f051f-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="f051f-160">Laufwerk:\Pfad\Dateiname.wk4</span><span class="sxs-lookup"><span data-stu-id="f051f-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-161">HTML-Import</span><span class="sxs-lookup"><span data-stu-id="f051f-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="f051f-162">HTML-Import;</span><span class="sxs-lookup"><span data-stu-id="f051f-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="f051f-163">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="f051f-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-164">HTML-Export</span><span class="sxs-lookup"><span data-stu-id="f051f-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="f051f-165">HTML-Export;</span><span class="sxs-lookup"><span data-stu-id="f051f-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="f051f-166">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-167">Text</span><span class="sxs-lookup"><span data-stu-id="f051f-167">Text</span></span></p></td>
<td><p><span data-ttu-id="f051f-168">Text;</span><span class="sxs-lookup"><span data-stu-id="f051f-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="f051f-169">Laufwerk:\Pfad</span><span class="sxs-lookup"><span data-stu-id="f051f-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f051f-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="f051f-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="f051f-171">ODBC; DATABASE=Datenbank; UID=Benutzer; PWD=Kennwort; DSN= Datenquellenname; [LOGINTIMEOUT=Sekunden;]</span><span class="sxs-lookup"><span data-stu-id="f051f-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="f051f-172">Keine</span><span class="sxs-lookup"><span data-stu-id="f051f-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f051f-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="f051f-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="f051f-174">Exchange 4.0; MAPILEVEL=Ordnerpfad; [TABLETYPE={ 0 | 1 }];[PROFILE=Profil;] [PWD=Kennwort;] [DATABASE=Datenbank;]</span><span class="sxs-lookup"><span data-stu-id="f051f-174">Exchange 4.0; 
MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] 
[PWD=password;] 
[DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="f051f-175">Laufwerk:\Pfad\Dateiname</span><span class="sxs-lookup"><span data-stu-id="f051f-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f051f-176">Wenn ein Kennwort erforderlich ist, aber in der **Connect**-Eigenschaft nicht angegeben wird, wird ein Anmelde-Dialogfeld angezeigt, wenn der ODBC-Treiber erstmals auf eine Tabelle zugreift, und erneut, wenn die Verbindung geschlossen und neu geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="f051f-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="f051f-p104">Für Daten in Microsoft Exchange muss für den erforderlichen MAPILEVEL-Schlüssel ein vollständig aufgelöster Ordnerpfad angegeben werden (z. B. "Mailbox - Pat SmithIAlpha/Today"). Der Pfad umfasst nicht den Namen des Ordners, der als Tabelle geöffnet wird. Der Name dieses Ordners muss stattdessen als name-Argument der **CreateTable**-Methode angegeben werden. Zum Öffnen eines Ordners muss der TABLETYPE-Schlüssel auf "0" gesetzt werden (Standard), zum Öffnen eines Adressbuchs muss er den Wert "1" erhalten. Der PROFILE-Schlüssel erhält standardmäßig den Wert des aktuell verwendeten Profils.</span><span class="sxs-lookup"><span data-stu-id="f051f-p104">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today"). The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method. The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book. The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="f051f-181">Für Basistabellen in einer Micorosoft Access-Datenbank ist der Wert der **Connect**-Eigenschaft eine Null-Zeichenfolge ("").</span><span class="sxs-lookup"><span data-stu-id="f051f-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="f051f-182">Vor dem Festlegen der **ReturnsRecords**-Eigenschaft müssen Sie die **Connect**-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="f051f-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="f051f-183">Sie müssen die Zugriffsberechtigungen für den Computer besitzen, der den Datenbankserver enthält, auf den Sie zugreifen wollen.</span><span class="sxs-lookup"><span data-stu-id="f051f-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>

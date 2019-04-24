---
title: Initialisieren des Microsoft Exchange-Datenquellentreibers
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291407"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="49aa9-102">Initialisieren des Microsoft Exchange-Datenquellentreibers</span><span class="sxs-lookup"><span data-stu-id="49aa9-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="49aa9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49aa9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49aa9-104">Bei der Installation des Microsoft Exchange-Datenquellentreibers schreibt das Setup Programm in der Unterschlüssel Module und ISAM Formate eine Reihe von Standardwerten in die Microsoft Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="49aa9-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="49aa9-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span><span class="sxs-lookup"><span data-stu-id="49aa9-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="49aa9-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span><span class="sxs-lookup"><span data-stu-id="49aa9-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="49aa9-107">Microsoft Exchange-Datenquellen-Initialisierungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="49aa9-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="49aa9-108">Der Exchange-Ordner **Access Connectivity Engine\\Engines enthält Initialisierungseinstellungen für den Aceexch. dll-Treiber, der für den externen Zugriff auf Microsoft Outlook-und Microsoft Exchange-Ordner verwendet wird.\\**</span><span class="sxs-lookup"><span data-stu-id="49aa9-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="49aa9-109">The only entry in this folder is the following:</span><span class="sxs-lookup"><span data-stu-id="49aa9-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="49aa9-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span><span class="sxs-lookup"><span data-stu-id="49aa9-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="49aa9-111">Der vollständige Pfad wird bei der Installation festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49aa9-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="49aa9-112">Werte sind vom Typ REG\_SZ.</span><span class="sxs-lookup"><span data-stu-id="49aa9-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="49aa9-p104">Die Verwendung des Outlook-ISAM-Formats und des Exchange-Client-ISAM-Formats liefert ähnliche Ergebnisse. Der einzige Unterschied besteht darin, dass die beiden unterschiedlichen Clients für dieselben Spalten unterschiedliche Namen verwenden. Die beiden ISAM-Formate wurden erstellt, damit das Microsoft Access-Datenbankmodul die Spaltennamen in dem vom Benutzer gewünschten Format zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="49aa9-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="49aa9-116">Microsoft Outlook-Client-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="49aa9-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="49aa9-117">Der Ordner " **Access\\Connectivity Engine\\ISAM Formats Outlook 9,0** " enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="49aa9-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49aa9-118">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="49aa9-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="49aa9-119">Typ</span><span class="sxs-lookup"><span data-stu-id="49aa9-119">Type</span></span></p></th>
<th><p><span data-ttu-id="49aa9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="49aa9-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-121">Modul</span><span class="sxs-lookup"><span data-stu-id="49aa9-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="49aa9-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="49aa9-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="49aa9-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="49aa9-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="49aa9-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="49aa9-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="49aa9-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="49aa9-126">Outlook ()</span><span class="sxs-lookup"><span data-stu-id="49aa9-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="49aa9-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="49aa9-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-129">01</span><span class="sxs-lookup"><span data-stu-id="49aa9-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="49aa9-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="49aa9-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-132">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-133">Isamtype</span><span class="sxs-lookup"><span data-stu-id="49aa9-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="49aa9-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="49aa9-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="49aa9-135">3</span><span class="sxs-lookup"><span data-stu-id="49aa9-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="49aa9-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="49aa9-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-138">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="49aa9-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="49aa9-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-141">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="49aa9-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="49aa9-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-144">01</span><span class="sxs-lookup"><span data-stu-id="49aa9-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="49aa9-145">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="49aa9-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="49aa9-146">Microsoft Exchange-Client-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="49aa9-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="49aa9-147">Der Ordner **Access Connectivity\\Engine ISAM\\Exchange 4,0** enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="49aa9-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49aa9-148">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="49aa9-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="49aa9-149">Typ</span><span class="sxs-lookup"><span data-stu-id="49aa9-149">Type</span></span></p></th>
<th><p><span data-ttu-id="49aa9-150">Wert</span><span class="sxs-lookup"><span data-stu-id="49aa9-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-151">Modul</span><span class="sxs-lookup"><span data-stu-id="49aa9-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="49aa9-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="49aa9-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="49aa9-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="49aa9-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="49aa9-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="49aa9-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="49aa9-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="49aa9-156">Exchange ()</span><span class="sxs-lookup"><span data-stu-id="49aa9-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="49aa9-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="49aa9-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-159">01</span><span class="sxs-lookup"><span data-stu-id="49aa9-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="49aa9-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="49aa9-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-162">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-163">Isamtype</span><span class="sxs-lookup"><span data-stu-id="49aa9-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="49aa9-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="49aa9-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="49aa9-165">3</span><span class="sxs-lookup"><span data-stu-id="49aa9-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="49aa9-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="49aa9-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-168">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49aa9-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="49aa9-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="49aa9-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-171">00</span><span class="sxs-lookup"><span data-stu-id="49aa9-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49aa9-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="49aa9-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="49aa9-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="49aa9-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="49aa9-174">01</span><span class="sxs-lookup"><span data-stu-id="49aa9-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="49aa9-175">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="49aa9-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="49aa9-176">Anpassen der Datei "Schema. ini" für Outlook und Exchange-Daten</span><span class="sxs-lookup"><span data-stu-id="49aa9-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="49aa9-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span><span class="sxs-lookup"><span data-stu-id="49aa9-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="49aa9-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span><span class="sxs-lookup"><span data-stu-id="49aa9-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>


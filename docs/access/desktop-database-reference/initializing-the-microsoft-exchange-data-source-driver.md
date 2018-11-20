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
ms.openlocfilehash: c64f28769d88c2684485ba537bdbdf22afd30ac5
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026050"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="79adb-102">Initialisieren des Microsoft Exchange-Datenquellentreibers</span><span class="sxs-lookup"><span data-stu-id="79adb-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="79adb-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="79adb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79adb-104">Bei der Installation von Microsoft Exchange-Datenquellentreibers schreibt das Setupprogramm Standardwerte der Microsoft Windows-Registrierung im Unterschlüssel Module und -ISAM-Formate.</span><span class="sxs-lookup"><span data-stu-id="79adb-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="79adb-105">Sie sollten diese Einstellungen nicht direkt geändert. Verwenden Sie das Setupprogramm für Ihre Anwendung hinzufügen, entfernen oder ändern Sie diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="79adb-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="79adb-106">In den folgenden Abschnitten werden die Initialisierung und ISAM formateinstellungen für Microsoft Exchange-Datenquellentreibers beschrieben.</span><span class="sxs-lookup"><span data-stu-id="79adb-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="79adb-107">Initialisierungseinstellungen für Microsoft Exchange-Datenquelle</span><span class="sxs-lookup"><span data-stu-id="79adb-107">Microsoft Exchange data source initialization settings</span></span>

<span data-ttu-id="79adb-108">Die **Konnektivitätsmodul für Access\\Module\\Exchange** Ordner enthält initialisierungseinstellungen für Aceexch.dll-Treiber für den externen Zugriff auf Microsoft Outlook und Microsoft Exchange-Ordner verwendet.</span><span class="sxs-lookup"><span data-stu-id="79adb-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="79adb-109">Der einzige Eintrag in diesem Ordner lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="79adb-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="79adb-110">Microsoft Access-Datenbankmodul verwendet diese Einstellung, um den Speicherort der Aceexch.dll anzugeben.</span><span class="sxs-lookup"><span data-stu-id="79adb-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="79adb-111">Der vollständige Pfad wird bei der Installation bestimmt.</span><span class="sxs-lookup"><span data-stu-id="79adb-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="79adb-112">Werte sind vom Typ REG\_su.</span><span class="sxs-lookup"><span data-stu-id="79adb-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="79adb-p104">Die Verwendung des Outlook-ISAM-Formats und des Exchange-Client-ISAM-Formats liefert ähnliche Ergebnisse. Der einzige Unterschied besteht darin, dass die beiden unterschiedlichen Clients für dieselben Spalten unterschiedliche Namen verwenden. Die beiden ISAM-Formate wurden erstellt, damit das Microsoft Access-Datenbankmodul die Spaltennamen in dem vom Benutzer gewünschten Format zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="79adb-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="79adb-116">Microsoft Outlook-Client-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="79adb-116">Microsoft Outlook client ISAM formats</span></span>

<span data-ttu-id="79adb-117">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Outlook 9.0** Ordner enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="79adb-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79adb-118">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="79adb-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="79adb-119">Type</span><span class="sxs-lookup"><span data-stu-id="79adb-119">Type</span></span></p></th>
<th><p><span data-ttu-id="79adb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="79adb-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79adb-121">Engine</span><span class="sxs-lookup"><span data-stu-id="79adb-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="79adb-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="79adb-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="79adb-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="79adb-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="79adb-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="79adb-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="79adb-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="79adb-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="79adb-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="79adb-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="79adb-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-129">01</span><span class="sxs-lookup"><span data-stu-id="79adb-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="79adb-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="79adb-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-132">00</span><span class="sxs-lookup"><span data-stu-id="79adb-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="79adb-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="79adb-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="79adb-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="79adb-135">3</span><span class="sxs-lookup"><span data-stu-id="79adb-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="79adb-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="79adb-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-138">00</span><span class="sxs-lookup"><span data-stu-id="79adb-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="79adb-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="79adb-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-141">00</span><span class="sxs-lookup"><span data-stu-id="79adb-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="79adb-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="79adb-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-144">01</span><span class="sxs-lookup"><span data-stu-id="79adb-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="79adb-145">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="79adb-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="79adb-146">Microsoft Exchange-Client-ISAM-Formate</span><span class="sxs-lookup"><span data-stu-id="79adb-146">Microsoft Exchange client ISAM formats</span></span>

<span data-ttu-id="79adb-147">Die **Konnektivitätsmodul für Access\\-ISAM-Formate\\Exchange 4.0** Ordner enthält die folgenden Einträge.</span><span class="sxs-lookup"><span data-stu-id="79adb-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="79adb-148">Name des Eintrags</span><span class="sxs-lookup"><span data-stu-id="79adb-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="79adb-149">Type</span><span class="sxs-lookup"><span data-stu-id="79adb-149">Type</span></span></p></th>
<th><p><span data-ttu-id="79adb-150">Wert</span><span class="sxs-lookup"><span data-stu-id="79adb-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="79adb-151">Engine</span><span class="sxs-lookup"><span data-stu-id="79adb-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="79adb-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="79adb-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="79adb-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="79adb-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="79adb-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="79adb-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="79adb-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="79adb-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="79adb-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="79adb-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="79adb-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-159">01</span><span class="sxs-lookup"><span data-stu-id="79adb-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="79adb-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="79adb-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-162">00</span><span class="sxs-lookup"><span data-stu-id="79adb-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="79adb-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="79adb-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="79adb-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="79adb-165">3</span><span class="sxs-lookup"><span data-stu-id="79adb-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="79adb-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="79adb-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-168">00</span><span class="sxs-lookup"><span data-stu-id="79adb-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="79adb-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="79adb-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="79adb-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-171">00</span><span class="sxs-lookup"><span data-stu-id="79adb-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="79adb-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="79adb-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="79adb-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="79adb-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="79adb-174">01</span><span class="sxs-lookup"><span data-stu-id="79adb-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="79adb-175">Wenn Sie Einstellungen in der Windows-Registrierung ändern, müssen Sie das Datenbankmodul beenden und erneut starten, damit die neuen Einstellungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="79adb-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="79adb-176">Anpassen der Datei "Schema.ini" für Outlook- und Exchange-Daten</span><span class="sxs-lookup"><span data-stu-id="79adb-176">Customizing the Schema.ini file for Outlook and Exchange data</span></span>

<span data-ttu-id="79adb-p105">Die Datei Schema.ini wird von Outlook- und Exchange-ISAM weitgehend wie von Text-ISAM verwendet. Schema.ini enthält die Angaben zur Datenquelle: wie die Daten formatiert werden und die Namen der zu verwendenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="79adb-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="79adb-p106">Es ist nicht erforderlich, die Datei Schema.ini zu ändern, um Daten für Outlook und Exchange zu lesen, zu importieren oder zu exportieren. Viele der Einstellungen für Outlook und Exchange in der Datei Schema.ini beziehen sich auf interne Tags, die für MAPI benötigt werden. Sie sollten nicht versuchen, diese Tagwerte zu ändern.</span><span class="sxs-lookup"><span data-stu-id="79adb-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>


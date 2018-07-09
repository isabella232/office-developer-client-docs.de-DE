---
title: Konfigurieren von UDFs in Excel Online in der Office Online Server Preview
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Verwenden Sie benutzerdefinierte Funktionen (UDFs) zum Aufrufen von benutzerdefinierten Funktionen in Excel Online in Office Online Server Preview.
ms.openlocfilehash: ae2d668ebd4a4df278a5c19e702de248b1749b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790382"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a><span data-ttu-id="00d3b-103">Konfigurieren von UDFs in Excel Online in der Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="00d3b-103">Configure UDFs in Excel Online in Office Online Server Preview</span></span>

<span data-ttu-id="00d3b-104">[Dieses Thema ist der Dokumentation zur Vorabversion und kann in zukünftigen Versionen geändert.] Verwenden Sie benutzerdefinierte Funktionen (UDFs) zum Aufrufen von benutzerdefinierten Funktionen in Excel Online in Office Online Server Preview.</span><span class="sxs-lookup"><span data-stu-id="00d3b-104">[This topic is pre-release documentation and is subject to change in future releases.] Use user-defined functions (UDFs) in Excel Online in Office Online Server Preview to call custom functions.</span></span> 
  
<span data-ttu-id="00d3b-p101">Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:</span><span class="sxs-lookup"><span data-stu-id="00d3b-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="00d3b-107">Aufrufen benutzerdefinierter mathematischer Funktionen</span><span class="sxs-lookup"><span data-stu-id="00d3b-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="00d3b-108">Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern</span><span class="sxs-lookup"><span data-stu-id="00d3b-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="00d3b-109">Aufrufen von Webdiensten</span><span class="sxs-lookup"><span data-stu-id="00d3b-109">Call web services.</span></span>
    
<span data-ttu-id="00d3b-110">UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="00d3b-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="00d3b-p102">In einem lokalen Verzeichnis. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="00d3b-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="00d3b-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="00d3b-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="00d3b-p103">Im globalen Assemblycache. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="00d3b-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="00d3b-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=de, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="00d3b-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="00d3b-117">Verweisen auf den Speicherort beim Erstellen einer Definition **New-OfficeWebAppsExcelUserDefinedFunction** auf der Office Online Server Preview.</span><span class="sxs-lookup"><span data-stu-id="00d3b-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server Preview.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00d3b-118">Office Online Server Preview unterstützt keine UDFs auf Netzwerkfreigaben befinden.</span><span class="sxs-lookup"><span data-stu-id="00d3b-118">Office Online Server Preview does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server-preview"></a><span data-ttu-id="00d3b-119">Aktivieren von UDFs auf Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="00d3b-119">Enable UDFs on Office Online Server Preview</span></span>

<span data-ttu-id="00d3b-120">Wenn ein Administrator eine neue Office Web Apps Server-Farm erstellt mithilfe des [New-OfficeWebAppsFarm](https://technet.microsoft.com/de-de/library/jj219436.aspx) Windows PowerShell-Cmdlets, sind die UDF-Assemblys standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="00d3b-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/de-de/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="00d3b-121">Der Standardwert des Flags **ExcelUdfsAllowed** ist false.</span><span class="sxs-lookup"><span data-stu-id="00d3b-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="00d3b-122">Um UDFs aktivieren möchten, führen Sie den folgenden Windows PowerShell-Befehl auf der Office Online Server Preview, nachdem die Office Web Apps Server-Farm erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="00d3b-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server Preview, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a><span data-ttu-id="00d3b-123">Erstellen von UDF-Definitionen auf Office Online Server Preview</span><span class="sxs-lookup"><span data-stu-id="00d3b-123">Create UDF definitions on Office Online Server Preview</span></span>

<span data-ttu-id="00d3b-124">Nachdem Sie UDFs aktivieren, müssen Sie eine Definition für die Binärdatei zu erstellen, die den UDFs enthält.</span><span class="sxs-lookup"><span data-stu-id="00d3b-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="00d3b-125">Um eine Definition für die UDF auf der Office Online Server Preview binary zu erstellen, verwenden Sie das Cmdlet " **New-OfficeWebAppsExcelUserDefinedFunction** ".</span><span class="sxs-lookup"><span data-stu-id="00d3b-125">To create a definition for your UDF binary on the Office Online Server Preview, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="00d3b-126">Dieses Cmdlet umfasst die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="00d3b-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="00d3b-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="00d3b-127">**Assembly**</span></span>
    
- <span data-ttu-id="00d3b-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="00d3b-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="00d3b-129">**Aktivieren** (standardmäßig auf "false" festgelegt)</span><span class="sxs-lookup"><span data-stu-id="00d3b-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="00d3b-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00d3b-130">**Description**</span></span>
    
<span data-ttu-id="00d3b-131">Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="00d3b-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="00d3b-132">Nachdem das neue UDF-Verweises erstellt wurde, führen Sie **iisreset aus** , auf dem Server, um den Verweis sofort zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="00d3b-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a><span data-ttu-id="00d3b-133">Zusätzliche Office Online Server Preview UDF Windows PowerShell-Befehle</span><span class="sxs-lookup"><span data-stu-id="00d3b-133">Additional Office Online Server Preview UDF Windows PowerShell commands</span></span>

<span data-ttu-id="00d3b-134">Verwenden Sie die folgenden Windows PowerShell-Cmdlets UDFs entwickelt:</span><span class="sxs-lookup"><span data-stu-id="00d3b-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="00d3b-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (ohne erforderliche Parameter) - gibt eine Liste von UDF-Definitionen, die auf der Office Online Server Preview konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="00d3b-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server Preview.</span></span> 
    
- <span data-ttu-id="00d3b-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) - festgelegt Eigenschaften auf vorhandene UDF-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="00d3b-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="00d3b-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) - entfernt vorhandene UDF-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="00d3b-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="00d3b-138">UDF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="00d3b-138">UDF sample</span></span>

<span data-ttu-id="00d3b-139">Die folgenden Dateien stellen eine Beispielarbeitsmappe, die eine UDF-Datei und die binären UDF verwendet:</span><span class="sxs-lookup"><span data-stu-id="00d3b-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="00d3b-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) – eine Beispielarbeitsmappe, die eine UDF-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="00d3b-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) -- a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="00d3b-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) – die UDF-Binärdatei</span><span class="sxs-lookup"><span data-stu-id="00d3b-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) -- the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="00d3b-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00d3b-142">See also</span></span>

- [<span data-ttu-id="00d3b-143">Konfigurieren von Excel Online administrativen Einstellungen</span><span class="sxs-lookup"><span data-stu-id="00d3b-143">Configure Excel Online administrative settings</span></span>](https://technet.microsoft.com/de-de/library/jj219698%28v=office.16%29.aspx)  
- [<span data-ttu-id="00d3b-144">Office Online Server – Vorschau</span><span class="sxs-lookup"><span data-stu-id="00d3b-144">Office Online Server Preview</span></span>](https://technet.microsoft.com/de-de/library/jj219456%28v=office.16%29.aspx)
    


---
title: Konfigurieren von UDFs in Excel Online in Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Verwenden von benutzerdefinierten Funktionen in Excel Online in Office Online Server zum Aufrufen von benutzerdefinierten Funktionen.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311060"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="07dd0-103">Konfigurieren von UDFs in Excel Online in Office Online Server</span><span class="sxs-lookup"><span data-stu-id="07dd0-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="07dd0-104">Verwenden von benutzerdefinierten Funktionen in Excel Online in Office Online Server zum Aufrufen von benutzerdefinierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="07dd0-p101">Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:</span><span class="sxs-lookup"><span data-stu-id="07dd0-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="07dd0-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="07dd0-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="07dd0-108">Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern</span><span class="sxs-lookup"><span data-stu-id="07dd0-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="07dd0-109">Aufrufen von Webdiensten</span><span class="sxs-lookup"><span data-stu-id="07dd0-109">Call web services.</span></span>
    
<span data-ttu-id="07dd0-110">UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="07dd0-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="07dd0-p102">In einem lokalen Verzeichnis. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07dd0-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="07dd0-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="07dd0-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="07dd0-p103">Im globalen Assemblycache. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07dd0-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="07dd0-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="07dd0-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="07dd0-117">Verweisen Sie auf den Speicherort, wenn Sie eine **New-OfficeWebAppsExcelUserDefinedFunction-** Definition auf dem Office Online-Server erstellen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07dd0-118">Office Online Server unterstützt keine UDFs in Netzwerkfreigaben.</span><span class="sxs-lookup"><span data-stu-id="07dd0-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="07dd0-119">Aktivieren von UDFs auf Office Online Server</span><span class="sxs-lookup"><span data-stu-id="07dd0-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="07dd0-120">Wenn ein Administrator mithilfe des Windows PowerShell-Cmdlets [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) eine neue Office Web Apps Server-Farm erstellt, sind UDF-Assemblys standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="07dd0-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="07dd0-121">Der Standardwert des **ExcelUdfsAllowed**-Flags lautet "False".</span><span class="sxs-lookup"><span data-stu-id="07dd0-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="07dd0-122">Führen Sie den folgenden Windows PowerShell-Befehl auf dem Office Online-Server aus, um UDFs zu aktivieren, nachdem die Office Web Apps Server-Farm erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="07dd0-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="07dd0-123">Erstellen von UDF-Definitionen auf Office Online Server</span><span class="sxs-lookup"><span data-stu-id="07dd0-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="07dd0-124">Nach dem Aktivieren von UDFs müssen Sie eine Definition für die Binärdatei mit den UDFs erstellen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="07dd0-125">Verwenden Sie das **New-OfficeWebAppsExcelUserDefinedFunction-** Cmdlet, um eine Definition für Ihre UDF-Binärdatei auf dem Office Online-Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="07dd0-126">Dieses Cmdlet umfasst die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="07dd0-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="07dd0-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="07dd0-127">**Assembly**</span></span>
    
- <span data-ttu-id="07dd0-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="07dd0-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="07dd0-129">**Enable** (standardmäßig auf False festgelegt)</span><span class="sxs-lookup"><span data-stu-id="07dd0-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="07dd0-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="07dd0-130">**Description**</span></span>
    
<span data-ttu-id="07dd0-131">Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="07dd0-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="07dd0-132">Führen Sie nach dem Erstellen des neuen UDF-Verweises **iisreset** auf dem Server aus, um den Verweis sofort zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="07dd0-133">Zusätzliche UDF-Windows PowerShell-Befehle für Office Online Server</span><span class="sxs-lookup"><span data-stu-id="07dd0-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="07dd0-134">Verwenden Sie die folgenden Windows PowerShell-Cmdlets, um mit UDFs zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="07dd0-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="07dd0-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (keine erforderlichen Parameter)-gibt eine Liste der UDF-Definitionen zurück, die auf dem Office Online-Server konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="07dd0-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="07dd0-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Legt Eigenschaften für vorhandene UDF-Definitionen fest.</span><span class="sxs-lookup"><span data-stu-id="07dd0-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="07dd0-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Entfernt Eigenschaften von vorhandenen UDF-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="07dd0-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="07dd0-138">UDF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="07dd0-138">UDF sample</span></span>

<span data-ttu-id="07dd0-139">Die folgenden Dateien enthalten eine Beispielarbeitsmappe, die eine UDF und die UDF-Binärdatei verwendet:</span><span class="sxs-lookup"><span data-stu-id="07dd0-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="07dd0-140">[BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): eine Beispielarbeitsmappe, die eine UDF verwendet</span><span class="sxs-lookup"><span data-stu-id="07dd0-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="07dd0-141">[EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): die UDF-Binärdatei</span><span class="sxs-lookup"><span data-stu-id="07dd0-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="07dd0-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07dd0-142">See also</span></span>

- [<span data-ttu-id="07dd0-143">Konfigurieren von administrativen Einstellungen für Excel Online </span><span class="sxs-lookup"><span data-stu-id="07dd0-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="07dd0-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="07dd0-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


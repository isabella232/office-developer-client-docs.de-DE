---
title: Konfigurieren von UDFs in Excel Online in Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Verwenden Sie benutzerdefinierte Funktionen (USERFs) in Excel Online in Office Online Server zum Aufrufen benutzerdefinierter Funktionen.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102933"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="a9cb7-103">Konfigurieren von UDFs in Excel Online in Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a9cb7-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="a9cb7-104">Verwenden Sie benutzerdefinierte Funktionen (USERFs) in Excel Online in Office Online Server zum Aufrufen benutzerdefinierter Funktionen.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="a9cb7-p101">Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="a9cb7-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="a9cb7-108">Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern</span><span class="sxs-lookup"><span data-stu-id="a9cb7-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="a9cb7-109">Aufrufen von Webdiensten</span><span class="sxs-lookup"><span data-stu-id="a9cb7-109">Call web services.</span></span>
    
<span data-ttu-id="a9cb7-110">UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="a9cb7-p102">In einem lokalen Verzeichnis. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="a9cb7-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="a9cb7-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="a9cb7-p103">Im globalen Assemblycache. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="a9cb7-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="a9cb7-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="a9cb7-117">Verweisen Sie auf den Speicherort, wenn Sie eine **New-OfficeWebAppsExcelUserDefinedFunction-Definition** auf der Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a9cb7-118">Office Online Server unterstützt keine UDFs in Netzwerkfreigaben.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="a9cb7-119">Aktivieren von UDFs auf Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a9cb7-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="a9cb7-120">Wenn ein Administrator eine neue Office Web Apps Server-Farm mithilfe des [Cmdlets New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell erstellt, werden UDF-Assemblys standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-120">When an administrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="a9cb7-121">Der Standardwert des **ExcelUdfsAllowed**-Flags lautet "False".</span><span class="sxs-lookup"><span data-stu-id="a9cb7-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="a9cb7-122">Führen Sie zum Aktivieren von UDFs den folgenden befehl Windows PowerShell auf der Office Online Server aus, nachdem die Office Web Apps Server-Farm erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="a9cb7-123">Erstellen von UDF-Definitionen auf Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a9cb7-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="a9cb7-124">Nach dem Aktivieren von UDFs müssen Sie eine Definition für die Binärdatei mit den UDFs erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="a9cb7-125">Verwenden Sie das **Cmdlet New-OfficeWebAppsExcelUserDefinedFunction,** um eine Definition für Ihre UDF-Binärdatei auf der Office Online Server zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="a9cb7-126">Dieses Cmdlet umfasst die folgenden Parameter:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="a9cb7-127">**Assembly**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-127">**Assembly**</span></span>
    
- <span data-ttu-id="a9cb7-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="a9cb7-129">**Enable** (standardmäßig auf False festgelegt)</span><span class="sxs-lookup"><span data-stu-id="a9cb7-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="a9cb7-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9cb7-130">**Description**</span></span>
    
<span data-ttu-id="a9cb7-131">Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="a9cb7-132">Führen Sie nach dem Erstellen des neuen UDF-Verweises **iisreset** auf dem Server aus, um den Verweis sofort zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="a9cb7-133">Zusätzliche Office Online Server UDF-Windows PowerShell Befehle</span><span class="sxs-lookup"><span data-stu-id="a9cb7-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="a9cb7-134">Verwenden Sie die Windows PowerShell cmdlets, um mit UDFs zu arbeiten:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="a9cb7-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (keine erforderlichen Parameter) – Gibt eine Liste der UDF-Definitionen zurück, die auf der Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="a9cb7-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Legt Eigenschaften für vorhandene UDF-Definitionen fest.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="a9cb7-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Entfernt Eigenschaften von vorhandenen UDF-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="a9cb7-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="a9cb7-138">UDF-Beispiel</span><span class="sxs-lookup"><span data-stu-id="a9cb7-138">UDF sample</span></span>

<span data-ttu-id="a9cb7-139">Die folgende Beispieldatei enthält eine Beispielarbeitsmappe, die eine UDF und die UDF-Binärdatei verwendet:</span><span class="sxs-lookup"><span data-stu-id="a9cb7-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="a9cb7-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): eine Beispielarbeitsmappe, die eine UDF verwendet</span><span class="sxs-lookup"><span data-stu-id="a9cb7-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="a9cb7-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9cb7-141">See also</span></span>

- [<span data-ttu-id="a9cb7-142">Konfigurieren von administrativen Einstellungen für Excel Online</span><span class="sxs-lookup"><span data-stu-id="a9cb7-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="a9cb7-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a9cb7-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


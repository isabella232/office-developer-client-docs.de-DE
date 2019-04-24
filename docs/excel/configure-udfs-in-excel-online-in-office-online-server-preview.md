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
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Konfigurieren von UDFs in Excel Online in Office Online Server

Verwenden von benutzerdefinierten Funktionen in Excel Online in Office Online Server zum Aufrufen von benutzerdefinierten Funktionen. 
  
Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:
  
- Call custom mathematical functions.
    
- Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern
    
- Aufrufen von Webdiensten
    
UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:
  
- In einem lokalen Verzeichnis. Beispiel: 
    
    C:\UDFs\MySampleUdf.dll
    
- Im globalen Assemblycache. Beispiel: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Verweisen Sie auf den Speicherort, wenn Sie eine **New-OfficeWebAppsExcelUserDefinedFunction-** Definition auf dem Office Online-Server erstellen. 
  
> [!NOTE]
> Office Online Server unterstützt keine UDFs in Netzwerkfreigaben. 
  
## <a name="enable-udfs-on-office-online-server"></a>Aktivieren von UDFs auf Office Online Server 

Wenn ein Administrator mithilfe des Windows PowerShell-Cmdlets [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) eine neue Office Web Apps Server-Farm erstellt, sind UDF-Assemblys standardmäßig deaktiviert. Der Standardwert des **ExcelUdfsAllowed**-Flags lautet "False". 
  
Führen Sie den folgenden Windows PowerShell-Befehl auf dem Office Online-Server aus, um UDFs zu aktivieren, nachdem die Office Web Apps Server-Farm erstellt wurde.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Erstellen von UDF-Definitionen auf Office Online Server

Nach dem Aktivieren von UDFs müssen Sie eine Definition für die Binärdatei mit den UDFs erstellen. Verwenden Sie das **New-OfficeWebAppsExcelUserDefinedFunction-** Cmdlet, um eine Definition für Ihre UDF-Binärdatei auf dem Office Online-Server zu erstellen. Dieses Cmdlet umfasst die folgenden Parameter: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Enable** (standardmäßig auf False festgelegt) 
    
- **Beschreibung**
    
Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Führen Sie nach dem Erstellen des neuen UDF-Verweises **iisreset** auf dem Server aus, um den Verweis sofort zu übernehmen. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Zusätzliche UDF-Windows PowerShell-Befehle für Office Online Server

Verwenden Sie die folgenden Windows PowerShell-Cmdlets, um mit UDFs zu arbeiten:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (keine erforderlichen Parameter)-gibt eine Liste der UDF-Definitionen zurück, die auf dem Office Online-Server konfiguriert sind. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Legt Eigenschaften für vorhandene UDF-Definitionen fest. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Entfernt Eigenschaften von vorhandenen UDF-Definitionen. 
    
## <a name="udf-sample"></a>UDF-Beispiel

Die folgenden Dateien enthalten eine Beispielarbeitsmappe, die eine UDF und die UDF-Binärdatei verwendet:
  
- [BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): eine Beispielarbeitsmappe, die eine UDF verwendet  
- [EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): die UDF-Binärdatei 
    
## <a name="see-also"></a>Siehe auch

- [Konfigurieren von administrativen Einstellungen für Excel Online ](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


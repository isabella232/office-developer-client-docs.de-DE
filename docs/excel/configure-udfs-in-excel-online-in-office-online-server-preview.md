---
title: Konfigurieren von UDFs in Excel Online in Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Verwenden Sie benutzerdefinierte Funktionen (USER-Defined Functions, UDFs) in Excel Online in Office Online Server, um benutzerdefinierte Funktionen aufzurufen.
ms.openlocfilehash: caaf2eb4d0be74423759eaa25bb6499a0350006f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601387"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a>Konfigurieren von UDFs in Excel Online in Office Online Server

Verwenden Sie benutzerdefinierte Funktionen (USER-Defined Functions, UDFs) in Excel Online in Office Online Server, um benutzerdefinierte Funktionen aufzurufen. 
  
Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:
  
- Call custom mathematical functions.
    
- Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern
    
- Aufrufen von Webdiensten
    
UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:
  
- In einem lokalen Verzeichnis. Beispiel: 
    
    C:\UDFs\MySampleUdf.dll
    
- Im globalen Assemblycache. Beispiel: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Verweisen Sie auf den Speicherort, wenn Sie eine **New-OfficeWebAppsExcelUserDefinedFunction-Definition** im Office Online Server erstellen. 
  
> [!NOTE]
> Office Online Server unterstützt keine UDFs, die sich auf Netzwerkfreigaben befinden. 
  
## <a name="enable-udfs-on-office-online-server"></a>Aktivieren von UDFs auf Office Online Server 

Wenn ein Administrator mithilfe des Cmdlets ["New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell" eine neue Office Web Apps-Serverfarm erstellt, sind UDF-Assemblys standardmäßig deaktiviert. Der Standardwert des **ExcelUdfsAllowed**-Flags lautet "False". 
  
Führen Sie zum Aktivieren von UDFs den folgenden befehl Windows PowerShell auf dem Office Online Server aus, nachdem die Office Web Apps-Serverfarm erstellt wurde.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a>Erstellen von UDF-Definitionen für Office Online Server

Nach dem Aktivieren von UDFs müssen Sie eine Definition für die Binärdatei mit den UDFs erstellen. Verwenden Sie das Cmdlet **"New-OfficeWebAppsExcelUserDefinedFunction",** um eine Definition für ihre UDF-Binärdatei im Office Online Server zu erstellen. Dieses Cmdlet umfasst die folgenden Parameter: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Enable** (standardmäßig auf False festgelegt) 
    
- **Beschreibung**
    
Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Führen Sie nach dem Erstellen des neuen UDF-Verweises **iisreset** auf dem Server aus, um den Verweis sofort zu übernehmen. 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a>Zusätzliche befehle Office Online Server UDF-Windows PowerShell

Verwenden Sie die folgenden Windows PowerShell Cmdlets, um mit UDFs zu arbeiten:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (keine erforderlichen Parameter) – Gibt eine Liste der UDF-Definitionen zurück, die im Office Online Server konfiguriert sind. 
    
- **Set- OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Legt Eigenschaften für vorhandene UDF-Definitionen fest. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) – Entfernt Eigenschaften von vorhandenen UDF-Definitionen. 
    
## <a name="udf-sample"></a>UDF-Beispiel

Die folgende Beispieldatei enthält eine Beispielarbeitsmappe, die eine UDF- und die UDF-Binärdatei verwendet:
  
- [BooleanDataType.xlsx: ](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx)eine Beispielarbeitsmappe, die eine UDF verwendet  
    
## <a name="see-also"></a>Siehe auch

- [Konfigurieren von administrativen Einstellungen für Excel Online](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [Office Online Server](https://docs.microsoft.com/officeonlineserver/office-online-server)
    


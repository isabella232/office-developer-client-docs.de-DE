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
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Konfigurieren von UDFs in Excel Online in der Office Online Server Preview

[Dieses Thema ist der Dokumentation zur Vorabversion und kann in zukünftigen Versionen geändert.] Verwenden Sie benutzerdefinierte Funktionen (UDFs) zum Aufrufen von benutzerdefinierten Funktionen in Excel Online in Office Online Server Preview. 
  
Über UDFs (User-defined Functions, benutzerdefinierte Funktionen) in Excel Online können Sie in verwaltetem Code geschriebene benutzerdefinierte Funktionen mithilfe von Formeln in Zellen aufrufen. Sie können UDFs zu folgenden Zwecken verwenden:
  
- Aufrufen benutzerdefinierter mathematischer Funktionen
    
- Abrufen von Daten aus benutzerdefinierten Datenquellen in Arbeitsblättern
    
- Aufrufen von Webdiensten
    
UDF-Binärdateien können in einem von zwei Speicherorten installiert werden:
  
- In einem lokalen Verzeichnis. Beispiel: 
    
    C:\UDFs\MySampleUdf.dll
    
- Im globalen Assemblycache. Beispiel: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=de, PublicKeyToken=e8123117d7ba9ae38
    
Verweisen auf den Speicherort beim Erstellen einer Definition **New-OfficeWebAppsExcelUserDefinedFunction** auf der Office Online Server Preview. 
  
> [!NOTE]
> Office Online Server Preview unterstützt keine UDFs auf Netzwerkfreigaben befinden. 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Aktivieren von UDFs auf Office Online Server Preview

Wenn ein Administrator eine neue Office Web Apps Server-Farm erstellt mithilfe des [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell-Cmdlets, sind die UDF-Assemblys standardmäßig deaktiviert. Der Standardwert des Flags **ExcelUdfsAllowed** ist false. 
  
Um UDFs aktivieren möchten, führen Sie den folgenden Windows PowerShell-Befehl auf der Office Online Server Preview, nachdem die Office Web Apps Server-Farm erstellt wurde.
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Erstellen von UDF-Definitionen auf Office Online Server Preview

Nachdem Sie UDFs aktivieren, müssen Sie eine Definition für die Binärdatei zu erstellen, die den UDFs enthält. Um eine Definition für die UDF auf der Office Online Server Preview binary zu erstellen, verwenden Sie das Cmdlet " **New-OfficeWebAppsExcelUserDefinedFunction** ". Dieses Cmdlet umfasst die folgenden Parameter: 
  
- **Assembly**
    
- **AssemblyLocation**
    
- **Aktivieren** (standardmäßig auf "false" festgelegt) 
    
- **Beschreibung**
    
Die folgenden Beispiele zeigen, wie die UDF-Definitionen erstellt werden.
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
Nachdem das neue UDF-Verweises erstellt wurde, führen Sie **iisreset aus** , auf dem Server, um den Verweis sofort zu übernehmen. 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Zusätzliche Office Online Server Preview UDF Windows PowerShell-Befehle

Verwenden Sie die folgenden Windows PowerShell-Cmdlets UDFs entwickelt:
  
- **Get-OfficeWebAppsExcelUserDefinedFunction** (ohne erforderliche Parameter) - gibt eine Liste von UDF-Definitionen, die auf der Office Online Server Preview konfiguriert sind. 
    
- **Set-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) - festgelegt Eigenschaften auf vorhandene UDF-Definitionen. 
    
- **Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity-Parameter erforderlich) - entfernt vorhandene UDF-Definitionen. 
    
## <a name="udf-sample"></a>UDF-Beispiel

Die folgenden Dateien stellen eine Beispielarbeitsmappe, die eine UDF-Datei und die binären UDF verwendet:
  
- [BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) – eine Beispielarbeitsmappe, die eine UDF-Datei verwendet.  
- [EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) – die UDF-Binärdatei 
    
## <a name="see-also"></a>Siehe auch

- [Konfigurieren von Excel Online administrativen Einstellungen](https://technet.microsoft.com/en-us/library/jj219698%28v=office.16%29.aspx)  
- [Office Online Server – Vorschau](https://technet.microsoft.com/en-us/library/jj219456%28v=office.16%29.aspx)
    


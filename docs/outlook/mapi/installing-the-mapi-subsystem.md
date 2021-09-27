---
title: Installieren des MAPI-Subsystems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.localizationpriority: high
ms.openlocfilehash: 56aac9386076974cb0bb532af349c7b4243cbdcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630509"
---
# <a name="installing-the-mapi-subsystem"></a>Installieren des MAPI-Subsystems

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Unterstützte Versionen von Windows installieren die MAPI-Stubbibliothek Mapi32.dll im Ordner _\<drive\>_ \Windows\System32. 
  
Die folgenden Windows-Versionen werden unterstützt:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Um das MAPI-Subsystem ordnungsgemäß zu installieren, installieren Sie eine Anwendung mit einem MAPI-basierten Speichersubsystem, z. B. Microsoft Outlook.
  
Informationen zur Installation des MAPI-Subsystems eines Computers finden Sie in der Registrierung. Alle Werte in den Registrierungseinträgen sind Zeichenfolgen. 
  
Installationsprogramme für Nachrichtendienste sind für das Erstellen der Installationsinformationen im folgenden Registrierungsschlüssel verantwortlich: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Nachrichtendientse müssen der Systemregistrierung Einträge hinzufügen. 
  
In der folgenden Tabelle ist zusammengefasst, wie Clients Versionsinformationen für das MAPI-Subsystem auf ihrem Computer abrufen.
  
|**Überprüfen**|**Registrierung**|
|:-----|:-----|
|Verfügbarkeit von MAPI  <br/> |Suchen Sie nach  `MAPIX=1`.  <br/> |
|Verfügbare Version von MAPI  <br/> |Suchen Sie nach einer MAPIXVER-Zeichenfolge in der Form " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Programmierung](mapi-programming-overview.md)


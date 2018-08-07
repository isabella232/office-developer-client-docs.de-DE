---
title: Installieren des MAPI-Subsystems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792693"
---
# <a name="installing-the-mapi-subsystem"></a>Installieren des MAPI-Subsystems

  
  
**Gilt für**: Outlook 
  
Unterstützte Versionen von Windows installieren die MAPI-Stub-Bibliothek „Mapi32.dll“ im Ordner _\<Laufwerk\>_ \Windows\System32. 
  
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


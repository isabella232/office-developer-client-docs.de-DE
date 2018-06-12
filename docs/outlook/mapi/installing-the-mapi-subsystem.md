---
title: Installieren des MAPI-Subsystems
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29fb4c44-1a59-457e-813b-a982bd72891c
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c2e135fc031dd3faf5a4e08c50147dfcf7787b5e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792693"
---
# <a name="installing-the-mapi-subsystem"></a>Installieren des MAPI-Subsystems

  
  
**Betrifft**: Outlook 
  
Unterst�tzte Versionen von Windows installieren die MAPI-Stubbibliothek, Mapi32.dll, im Ordner  _\<Laufwerk\>_ \Windows\System32 folder. 
  
Die folgenden Windows-Versionen werden unterst�tzt:
  
- Windows 7.
    
- Windows Vista.
    
- Windows Server 2008.
    
- Windows Server 2003.
    
- Windows XP.
    
Um das MAPI-Subsystem ordnungsgem�� zu installieren, installieren Sie eine Anwendung mit einem MAPI-basierten Speichersubsystem, z. B. Microsoft Outlook.
  
Informationen zur Installation des MAPI-Subsystems eines Computers finden Sie in der Registrierung. Alle Werte in den Registrierungseintr�gen sind Zeichenfolgen. 
  
Installationsprogramme f�r Nachrichtendienste sind f�r das Erstellen der Installationsinformationen im folgenden Registrierungsschl�ssel verantwortlich: 
  
 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Messaging Subsystem`
  
Nachrichtendientse m�ssen der Systemregistrierung Eintr�ge hinzuf�gen. 
  
In der folgenden Tabelle ist zusammengefasst, wie Clients Versionsinformationen f�r das MAPI-Subsystem auf ihrem Computer abrufen.
  
|**�berpr�fen**|**Registrierung**|
|:-----|:-----|
|Verf�gbarkeit von MAPI  <br/> |Suchen Sie nach  `MAPIX=1`.  <br/> |
|Verf�gbare Version von MAPI  <br/> |Suchen Sie nach einer MAPIXVER-Zeichenfolge in der Form " _x.x.x_".  <br/> |
   
## <a name="see-also"></a>Siehe auch



[�bersicht �ber die MAPI-Programmierung](mapi-programming-overview.md)


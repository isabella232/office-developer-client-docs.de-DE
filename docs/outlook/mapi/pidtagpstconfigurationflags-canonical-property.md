---
title: Kanonische PidTagPstConfigurationFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794844"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Kanonische PidTagPstConfigurationFlags-Eigenschaft
  
**Betrifft**: Outlook 
  
Gibt Konfiguration Flags für eine Tabelle persönlicher Speicher (PST-Datei).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Bezeichner:  <br/> |0x6770  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Persönlicher Speicher-Tabelle (. pst) interne  <br/> |
   
## <a name="remarks"></a>Hinweise

Folgende sind gültige Werte für diese Eigenschaft:
  
PST_CONFIG_UNICODE
  
> Gibt eine Unicode-PST-Datei an. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Wenn Satz aus der Client Kennzeichen an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode, wie Gespräch [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) **ConfigureMsgService** behandelt und überspringt die "dieser Informationsdienst wurde nicht konfiguriert" Warnung. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Teilt **ConfigureMsgService** nicht den Wert der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ändern, obwohl es bereitgestellt wurde. Es wurde in diesem Fall nur für neue PST-Dateien angegeben.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Erfahren Sie mehr Konfigurationscode für das erste anzuzeigende ein Dialogfeld zu bestätigen, dass eine Datei Offlineordnerdatei (OST) wurde gefunden und, je nach Antwort des Benutzers, verwenden Sie entweder den gefundenen Ordner Offline oder aktivieren den Benutzer Offline einen anderen Ordner zu suchen.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Kopiert die OST-Datei mit einem neuen eindeutigen Namen und den aktuellen Namen verwirft. Die vorhandenen OST-Datei auf dem Computer bleibt jedoch nicht mehr in diesem Profil verwendet. Dies tritt normalerweise auf, wenn Microsoft Outlook, eine bestimmte OST-Datei nicht länger ermöglicht und Registrierungsrichtlinien den Benutzer, benennen Sie die Datei nicht zulassen. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


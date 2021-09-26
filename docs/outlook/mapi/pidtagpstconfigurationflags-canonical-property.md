---
title: PidTagPstConfigurationFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eccf22a9e2fc39f4232eb194bef204055ec3ba07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583240"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>PidTagPstConfigurationFlags (kanonische Eigenschaft)
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt Konfigurationsflags für eine persönliche Speichertabelle (PST-Datei) fest.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Kennung:  <br/> |0x6770  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Persönliche Speichertabelle (PST) intern  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Es folgen gültige Werte für diese Eigenschaft:
  
PST_CONFIG_UNICODE
  
> Gibt eine Unicode-PST-Datei an. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Wenn sie von den Clientflags auf die [IMsgServiceAdmin::ConfigureMsgService-Methode](imsgserviceadmin-configuremsgservice.md) festgelegt werden, behandelt **ConfigureMsgService** wie ein [IMsgServiceAdmin::CreateMsgService-Aufruf](imsgserviceadmin-createmsgservice.md) und überspringt die Warnung "Dieser Informationsdienst wurde nicht konfiguriert". 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Weist **ConfigureMsgService** an, den Wert der **Eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) nicht zu ändern, obwohl er angegeben wurde. In diesem Fall wurde es nur für neue PST-Dateien bereitgestellt.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Weist den Konfigurationscode an, zunächst ein Dialogfeld anzuzeigen, um zu bestätigen, ob eine Offlineordnerdatei (OST) gefunden wurde, und abhängig von der Antwort des Benutzers entweder den gefundenen Offlineordner zu verwenden oder dem Benutzer zu ermöglichen, nach einem anderen Offlineordner zu suchen.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Kopiert die OST-Datei mit einem neuen eindeutigen Namen und verwirft den aktuellen Namen. Die vorhandene OST-Datei verbleibt auf dem Computer, wird jedoch nicht mehr in diesem Profil verwendet. Dies geschieht in der Regel, wenn Microsoft Outlook keine bestimmte OST-Datei mehr zulässt und registrierungsrichtlinien dem Benutzer nicht erlauben, die Datei umzubenennen. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: Kanonische Pidtagpstconfigurationflags (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408943"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a>Kanonische Pidtagpstconfigurationflags (-Eigenschaft
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an-Konfigurations Kennzeichen für eine persönliche Speichertabelle (PST-Datei).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_PST_CONFIG_FLAGS  <br/> |
|Kennung:  <br/> |0x6770  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Persönliche Speichertabelle (PST) intern  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Für diese Eigenschaft gelten die folgenden gültigen Werte:
  
PST_CONFIG_UNICODE
  
> Gibt eine Unicode-PST-Datei an. 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
PST_CONFIG_CREATE_NOWARN
  
> Wenn Sie von den Client-Flags auf die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode festgelegt wird, behandelt **ConfigureMsgService** wie ein [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Aufruf und überspringt den "Dieser Informationsdienst wurde nicht konfiguriert" Warnung. 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
PST_CONFIG_PRESERVE_DISPLAY_NAME
  
> Weist **ConfigureMsgService** an, den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft nicht zu ändern, obwohl Sie bereitgestellt wurde. In diesem Fall wurde es nur für neue PST-Dateien bereitgestellt.
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
OST_CONFIG_POLICY_DELAY_IGNORE_OST
  
> Weist den Konfigurationscode an, zunächst ein Dialogfeld anzuzeigen, um zu bestätigen, ob eine Offlineordnerdatei (Ost) gefunden wurde, und je nach Antwort des Benutzers entweder den gefundenen Offlineordner verwenden oder dem Benutzer ermöglichen, nach einem anderen Offlineordner zu suchen.
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
OST_CONFIG_CREATE_NEW_DEFAULT
  
> Kopiert die OST-Datei mit einem neuen eindeutigen Namen und verwirft den aktuellen Namen. Die vorhandene OST-Datei verbleibt auf dem Computer, wird aber in diesem Profil nicht mehr verwendet. Dies ist in der Regel der Fall, wenn Microsoft Outlook eine bestimmte OST-Datei nicht mehr zulässt und Registrierungsrichtlinien dem Benutzer die Umbenennung der Datei nicht gestatten. 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]] 
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


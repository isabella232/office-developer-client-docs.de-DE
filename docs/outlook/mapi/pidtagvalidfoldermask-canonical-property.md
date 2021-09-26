---
title: PidTagValidFolderMask (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d8f501d4692e1e4ef735355f723ad8201e8a001d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599256"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>PidTagValidFolderMask (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher angeben.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Kennung:  <br/> |0x35DF  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Eintragsbezeichner eines Ordners kann ungültig werden, wenn ein Benutzer den Ordner löscht oder wenn der Nachrichtenspeicher beschädigt wird.
  
Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Der Ordner "Allgemeine Ansichten" hat einen gültigen Eintragsbezeichner. Siehe **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Der Ordner "Finder" verfügt über einen gültigen Eintragsbezeichner. Siehe **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Der IpM-Empfangsordner (Interpersonal Message) hat einen gültigen Eintragsbezeichner. Siehe [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Der IPM-Postausgangsordner verfügt über einen gültigen Eintragsbezeichner. Siehe **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Der Ordner "GESENDETE IPM-Elemente" hat einen gültigen Eintragsbezeichner. Siehe **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> Die Unterstruktur des IPM-Ordners verfügt über einen gültigen Eintragsbezeichner. Siehe **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Der Ordner "GELÖSCHTE ELEMENTE" von IPM verfügt über einen gültigen Eintragsbezeichner. Siehe **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Der Ordner "Ansichten" verfügt über einen gültigen Eintragsbezeichner. Siehe **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


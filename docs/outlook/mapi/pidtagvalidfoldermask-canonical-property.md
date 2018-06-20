---
title: Kanonische PidTagValidFolderMask-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795289"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Kanonische PidTagValidFolderMask-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske der Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher angeben.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Bezeichner:  <br/> |0x35DF  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Eintrags-ID für einen Ordner werden ungültig, wenn ein Benutzer auf den Ordner löscht oder der Nachrichtenspeicher beschädigt.
  
Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Die gemeinsamen Ordner "Ansichten" besitzt eine gültige Eingabe-ID. Finden Sie unter **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Der Finder-Ordner verfügt über eine gültige Eingabe-Bezeichner. Finden Sie unter **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Die zwischen Personen angezeigt (IPM) Ordner verfügt über eine gültige Eingabe-Bezeichner. Finden Sie unter [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Der Ordner Postausgang IPM besitzt eine gültige Eingabe-ID. Finden Sie unter **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Ordner Gesendete Objekte IPM verfügt über eine gültige Eingabe-Bezeichner. Finden Sie unter **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> Die IPM Ordner Unterstruktur verfügt über eine gültige Eingabe Bezeichner. Finden Sie unter **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Der Ordner Gelöschte Objekte IPM verfügt über eine gültige Eingabe-Bezeichner. Finden Sie unter **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Ordner "Ansichten" verfügt über eine gültige Eingabe-Bezeichner. Finden Sie unter **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


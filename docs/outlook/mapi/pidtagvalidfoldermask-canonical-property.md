---
title: Kanonische Pidtagvalidfoldermask (-Eigenschaft
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
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360746"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Kanonische Pidtagvalidfoldermask (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die die Gültigkeit der Eintragsbezeichner der Ordner in einem Nachrichtenspeicher kennzeichnen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Kennung:  <br/> |0x35DF  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Eintrags-ID eines Ordners kann ungültig werden, wenn ein Benutzer den Ordner löscht oder wenn der Nachrichtenspeicher beschädigt wird.
  
Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Der Ordner Allgemeine Ansichten hat einen gültigen Eintragsbezeichner. Siehe **PR_COMMON_VIEWS_ENTRYID** ([pidtagcommonviewsentryid (](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Der Finder-Ordner verfügt über eine gültige Eintrags-ID. Siehe **PR_FINDER_ENTRYID** ([pidtagfinderentryid (](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Der Empfänger Ordner für die zwischenmenschlichen Nachrichten (IPM) verfügt über eine gültige Eintrags-ID. Weitere Informationen finden Sie unter [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Der IPM-Ausgangsordner hat einen gültigen Eintragsbezeichner. Siehe **PR_IPM_OUTBOX_ENTRYID** ([pidtagipmoutboxentryid (](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Der Ordner "IPM Sent Items" hat einen gültigen Eintragsbezeichner. Siehe **PR_IPM_SENTMAIL_ENTRYID** ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> Die Unterstruktur des IPM-Ordners verfügt über eine gültige Eintrags-ID. Siehe **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Der Ordner "IPM Deleted Items" hat einen gültigen Eintragsbezeichner. Siehe **PR_IPM_WASTEBASKET_ENTRYID** ([pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Der Ordner views hat eine gültige Eintrags-ID. Siehe **PR_VIEWS_ENTRYID** ([pidtagviewsentryid (](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


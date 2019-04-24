---
title: Kanonische Pidtagcontainercontents (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283128"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Kanonische Pidtagcontainercontents (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Table-Objekt mit eingebetteten Inhalten, das Informationen zu einem Container bereitstellt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Kennung:  <br/> |0x360F  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um den IID_IMAPITable-Schnittstellenbezeichner anzufordern. Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber optional melden können, wenn Sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontentable-Methode aufrufen. For more information, see [Inhalt von Tabellen](contents-tables.md). 
  
Diese Eigenschaft, **PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md)) und **PR_FOLDER_ASSOCIATED_CONTENTS** ([pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md)) ähneln der Verwendung. Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen: 
  
|**Eigenschaft**|**Table**|
|:-----|:-----|
|Pidtagcontainercontents (  <br/> |Inhaltstabelle  <br/> |
|**PR_CONTAINER_HIERARCHY** ([Pidtagcontainerhierarchy (](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Hierarchietabelle  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabelle mit zugeordneten Inhalten  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([Pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md))  <br/> |Attachment-Tabelle  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([Pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md))  <br/> |Empfängertabelle  <br/> |
   
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
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


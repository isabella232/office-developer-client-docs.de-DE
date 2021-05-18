---
title: PidTagContainerContents (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283128"
---
# <a name="pidtagcontainercontents-canonical-property"></a>PidTagContainerContents (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Inhalts-Tabellenobjekt, das Informationen zu einem Container enthält.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Kennung:  <br/> |0x360F  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein. Als Eigenschaft vom Typ PT_OBJECT kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable anfordert. Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::GetContentsTable-Methode](imapicontainer-getcontentstable.md) aufrufen. For more information, see [Inhalt von Tabellen](contents-tables.md). 
  
Diese Eigenschaft, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) und **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) sind in der Verwendung ähnlich. Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen: 
  
|**Eigenschaft**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Inhaltstabelle  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Hierarchietabelle  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabelle "Zugeordnete Inhalte"  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Anlagentabelle  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Empfängertabelle  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


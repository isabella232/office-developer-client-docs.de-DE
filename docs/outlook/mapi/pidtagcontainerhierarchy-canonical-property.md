---
title: PidTagContainerHierarchy (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332858"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>PidTagContainerHierarchy (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Hierarchietabelle-Objekt, das Informationen zu den untergeordneten Containern enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Kennung:  <br/> |0x360E  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein. Als Eigenschaft vom Typ **PT_OBJECT** kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, die den IID_IMAPITable anfordert. Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMAPIContainer::GetHierarchyTable-Methode](imapicontainer-gethierarchytable.md) aufrufen. Weitere Informationen finden Sie unter [Hierarchietabellen](hierarchy-tables.md). 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), und diese Eigenschaft ist in der Verwendung ähnlich. Mehrere MAPI-Eigenschaften bieten Zugriff auf Tabellen: 
  
|**Eigenschaft**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Inhaltstabelle  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Hierarchietabelle  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Tabelle "Zugeordnete Inhalte"  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Anlagentabelle  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Empfängertabelle  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
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


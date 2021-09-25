---
title: PidTagReceiveFolderSettings (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00de2b1cff620f21fe5b8306c9c847785d86325c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574790"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle der Einstellungen für den Empfangsordner eines Nachrichtenspeichers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Kennung:  <br/> |0x3415  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann in [IMAPIProp::CopyTo-Operationen](imapiprop-copyto.md) oder in [IMAPIProp::CopyProps-Operationen](imapiprop-copyprops.md) ausgeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) abgerufen werden. Der Zugriff auf den Inhalt sollte über die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) erfolgen, wobei die Schnittstelle mit bezeichner IID_IMAPITable angefordert wird. Dienstanbieter müssen sie an die [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie aber optional melden oder nicht, wenn sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMsgStore::GetReceiveFolderTable-Methode](imsgstore-getreceivefoldertable.md) aufrufen. Weitere Informationen finden Sie unter ["Ordnertabellen empfangen".](receive-folder-tables.md)
  
Diese Eigenschaft enthält eine Tabelle mit Zuordnungen der Empfangsordner für den Nachrichtenspeicher. Das Aufrufen von **OpenProperty** für diese Eigenschaft entspricht dem Aufrufen von **GetReceiveFolderTable** im Nachrichtenspeicher. 
  
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


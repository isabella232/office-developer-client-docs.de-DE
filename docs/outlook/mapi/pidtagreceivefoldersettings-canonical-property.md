---
title: PidTagReceiveFolderSettings (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571458"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>PidTagReceiveFolderSettings (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle mit einer Nachricht des Speichers erhalten Ordner Settings.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Kennung:  <br/> |0x3415  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann nicht es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden. von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode die Schnittstelle mit der ID IID_IMAPITable anfordern sollte seinen Inhalt zugegriffen werden. Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, jedoch kann positives oder nicht, wenn sie nicht festgelegt ist. 
  
Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode aufrufen. Weitere Informationen finden Sie unter [Ordner Tabellen erhalten](receive-folder-tables.md).
  
Diese Eigenschaft enthält eine Tabelle von Zuordnungen der Ordner für den Nachrichtenspeicher empfangen. Aufrufen von **OpenProperty** für diese Eigenschaft entspricht dem Aufrufen von **GetReceiveFolderTable** für den Informationsspeicher. 
  
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


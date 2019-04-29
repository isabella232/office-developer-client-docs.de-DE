---
title: Kanonische Pidtagreceivefoldersettings (-Eigenschaft
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
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415054"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Kanonische Pidtagreceivefoldersettings (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Tabelle der Einstellungen für den Empfangsordner eines Nachrichtenspeichers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Kennung:  <br/> |0x3415  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |MAPI-Nachrichtenspeicher  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden. Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um die Schnittstelle mit dem Bezeichner IID_IMAPITable anzufordern. Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber optional melden können, wenn Sie nicht festgelegt ist. 
  
Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode aufrufen. Weitere Informationen finden Sie unter [Receive Folder Tables](receive-folder-tables.md).
  
Diese Eigenschaft enthält eine Tabelle mit Zuordnungen der Empfangsordner für den Nachrichtenspeicher. Das **** Aufrufen von OpenProperty für diese Eigenschaft entspricht dem Aufrufen von **GetReceiveFolderTable** im Nachrichtenspeicher. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

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


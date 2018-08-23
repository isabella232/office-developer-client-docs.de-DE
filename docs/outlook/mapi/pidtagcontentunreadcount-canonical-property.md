---
title: PidTagContentUnreadCount (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContentUnreadCount
api_type:
- HeaderDef
ms.assetid: 4fe207e9-a77f-46b9-b51d-d989847a9d02
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b15dd467b7418ea10d384183dc32284924a90212
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581076"
---
# <a name="pidtagcontentunreadcount-canonical-property"></a>PidTagContentUnreadCount (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Anzahl der ungelesenen Nachrichten in einem Ordner enthält, wie Sie mithilfe des Nachrichtenspeichers berechnet. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CONTENT_UNREAD  <br/> |
|Kennung:  <br/> |0x3603  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Ordner  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft von der Nachrichtenspeicher berechnet wird für zwei unterschiedliche, obwohl verbunden, Zwecke. Auf ein MAPI-Folder-Objekt enthält sie die Anzahl der Nachrichten in einem Ordner. In eine Überschriftenzeile in kategorisierten MAPI-Tabellen enthält sie die Anzahl der ungelesenen nicht zugeordneten Nachrichten in der Kategorie, die diese Zeile mit der Spaltenüberschrift entspricht.
  
Diese Eigenschaft enthält die Anzahl der Nachrichten in den Ordner Inhaltstabelle für den das Flag MSGFLAG_READ in der **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))-Eigenschaft nicht festgelegt ist. Die **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))-Eigenschaft enthält die Anzahl der insgesamt Nachrichten für den Ordner. Die **PR_CONTENT_COUNT** und diese Eigenschaft sind für Clients schreibgeschützt. 
  
Einige Clientanwendungen werden die Kopfzeile einer Kategorie unterschiedlich, je nachdem der Wert dieser Eigenschaft an. Ein Client kann beispielsweise eine Kategorie anzeigen, die ungelesene Nachrichten fett enthält. Diese Eigenschaft kann nicht als eine Kategorie und beim Versuch verwendet werden, hierzu Ergebnisse in der MAPI_E_INVALID_PARAMETER-Wert aus der [SortTable](imapitable-sorttable.md) -Methode zurückgegeben wird. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Spezifikationen von Microsoft Exchange Server-Protokoll.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Zulässige Vorgänge für die Hauptobjekte-Tabelle enthält.
    
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


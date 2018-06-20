---
title: Kanonische PidTagStoreEntryIdEmsmdbV1-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 74626b735599a5f1485b26fcb65d907b552b3089
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795214"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Kanonische PidTagStoreEntryIdEmsmdbV1-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält das alte Format von Eintrags-ID des Microsoft Exchange Server 2010 oder Exchange Server 2013-Nachrichtenspeichers (Microsoft Outlook 2002 und früheren Versionen).
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Bezeichner:  <br/> |0x65F60102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Ab Microsoft Outlook 2003, wurden in die Eintrags-IDs, wodurch Vermeidung von zusätzlichen RPCs für Verweise auf die Server-FQDNs integriert werden. Allerdings Dies macht die Eintrags-IDs länger und führt weitere Szenarien, in dem die **CompareEntryIDs** -Methode verwendet werden muss, um festzustellen, ob zwei Eintrag IDs gleichwertig sind. Die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft (PidTagStoreIdEmsbdbV1) greift auf das ältere Format von der Exchange Server-Eintrags-ID, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet werden. Speicherplatz sparen Sie können und auch reduziert die Anzahl der **CompareEntryIDs** -Anrufe zu bestimmen, wann der Eintrag IDs gleichwertig sind erforderlich. Beachten Sie, dass mit älteren Eintrags-IDs Öffnen eines Postfachs einige zusätzliche RPCs anfallen kann, wenn ein Verweis erforderlich ist. 
  
Zugriff auf die Eigenschaft PR_STORE_ENTRYID_EMSMDB_V1 im Cache-Modus müssen Sie mit dem das Kennzeichen MAPI_NO_CACHE mit der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode im Cache umgehen. Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen. Nur Outlook 2003 über Microsoft Outlook 2013 unterstützen die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft. 
  
## <a name="see-also"></a>Siehe auch



[Kanonische PidTagStoreEntryId-Eigenschaft](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


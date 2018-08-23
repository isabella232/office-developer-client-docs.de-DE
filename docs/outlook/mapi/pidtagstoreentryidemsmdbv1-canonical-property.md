---
title: PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 505ea9ba5d7105f20f335035e42286fdab1cb1aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576323"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält das alte Format von Eintrags-ID des Microsoft Exchange Server 2010 oder Exchange Server 2013-Nachrichtenspeichers (Microsoft Outlook 2002 und früheren Versionen).
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Kennung:  <br/> |0x65F60102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ab Microsoft Outlook 2003, wurden in die Eintrags-IDs, wodurch Vermeidung von zusätzlichen RPCs für Verweise auf die Server-FQDNs integriert werden. Allerdings Dies macht die Eintrags-IDs länger und führt weitere Szenarien, in dem die **CompareEntryIDs** -Methode verwendet werden muss, um festzustellen, ob zwei Eintrag IDs gleichwertig sind. Die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft (PidTagStoreIdEmsbdbV1) greift auf das ältere Format von der Exchange Server-Eintrags-ID, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet werden. Speicherplatz sparen Sie können und auch reduziert die Anzahl der **CompareEntryIDs** -Anrufe zu bestimmen, wann der Eintrag IDs gleichwertig sind erforderlich. Beachten Sie, dass mit älteren Eintrags-IDs Öffnen eines Postfachs einige zusätzliche RPCs anfallen kann, wenn ein Verweis erforderlich ist. 
  
Zugriff auf die Eigenschaft PR_STORE_ENTRYID_EMSMDB_V1 im Cache-Modus müssen Sie mit dem das Kennzeichen MAPI_NO_CACHE mit der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode im Cache umgehen. Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen. Nur Outlook 2003 über Microsoft Outlook 2013 unterstützen die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft. 
  
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


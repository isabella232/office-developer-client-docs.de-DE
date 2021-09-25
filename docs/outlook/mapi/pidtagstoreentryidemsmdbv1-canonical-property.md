---
title: PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fe99dced15540813434b3486a46c547528f820e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578956"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält das alte Format (Microsoft Outlook 2002 und frühere Versionen) des Eintragsbezeichners eines Microsoft Exchange Server 2010- oder Exchange Server 2013-Nachrichtenspeichers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Kennung:  <br/> |0x65F60102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ab Microsoft Outlook 2003 wurden die Server-FQDNs in die Eintrags-IDs integriert, wodurch zusätzliche RPCs für Verweise vermieden wurden. Dadurch werden Eintrags-IDs jedoch länger, und es werden weitere Szenarien eingeführt, in denen die **CompareEntryIDs-Methode** verwendet werden muss, um zu bestimmen, ob zwei Eintrags-IDs gleichwertig sind. Die PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1)-Eigenschaft greift auf das ältere Format der Exchange Server Eintrags-ID zu, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet wird. Dies kann Platz sparen und auch die Anzahl der **CompareEntryIDs-Aufrufe** reduzieren, die erforderlich sind, um zu bestimmen, wann Eintrags-IDs gleichwertig sind. Beachten Sie, dass die Verwendung der älteren Eintrags-IDs zum Öffnen eines Postfachs einige zusätzliche RPCs verursachen kann, wenn ein Verweis erforderlich ist. 
  
Um im Cachemodus auf die PR_STORE_ENTRYID_EMSMDB_V1 Eigenschaft zuzugreifen, müssen Sie den Cache mithilfe des MAPI_NO_CACHE Flags mit der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) umgehen. Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen. Nur Outlook 2003 bis Microsoft Outlook 2013 die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft unterstützen. 
  
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


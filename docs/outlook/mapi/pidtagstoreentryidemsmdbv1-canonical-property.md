---
title: Kanonische Pidtagstoreentryidemsmdbv1 (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 40161358-4d41-43cf-83c7-fdd843bec87b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278771"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>Kanonische Pidtagstoreentryidemsmdbv1 (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den alten Stil (Microsoft Outlook 2002 und frühere Versionen) der Eintrags-ID eines Microsoft Exchange Server 2010-oder Exchange Server 2013-Nachrichtenspeichers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Kennung:  <br/> |0x65F60102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beginnend mit Microsoft Outlook 2003 wurden die Server-FQDNs in die Eintrags-IDs integriert, wodurch zusätzliche RPCs für Verweise vermieden wurden. Dadurch werden die Eintrags-IDs jedoch länger und es werden weitere Szenarien eingeführt, in denen die **CompareEntryIDs** -Methode verwendet werden muss, um zu bestimmen, ob zwei Eintrags-IDs äquivalent sind. Die PR_STORE_ENTRYID_EMSMDB_V1 (PidTagStoreIdEmsbdbV1)-Eigenschaft greift auf das ältere Format der Exchange Server-Eintrags-ID zu, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet wird. Dies kann Speicherplatz sparen und auch die Anzahl der **CompareEntryIDs** -Aufrufe reduzieren, die erforderlich sind, um zu bestimmen, wann die Eintrags-IDs äquivalent sind. Beachten Sie, dass bei Verwendung der älteren Eintrags-IDs zum Öffnen eines Postfachs möglicherweise zusätzliche RPCs auftreten, wenn ein Verweis erforderlich ist. 
  
Um im zwischengespeicherten Modus auf die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft zuzugreifen, müssen Sie den Cache mithilfe des MAPI_NO_CACHE-Flags mit der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode umgehen. Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf PR_STORE_ENTRYID zurückgreifen. Die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft wird nur von Outlook 2003 über Microsoft Outlook 2013 unterstützt. 
  
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagstoreentryid (-Eigenschaft](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


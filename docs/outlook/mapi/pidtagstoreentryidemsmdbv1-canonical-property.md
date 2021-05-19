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
ms.openlocfilehash: c8bccbfeb7f04745a66831618deff490bc651b02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415152"
---
# <a name="pidtagstoreentryidemsmdbv1-canonical-property"></a>PidTagStoreEntryIdEmsmdbV1 (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die alte Formatvorlage (Microsoft Outlook 2002 und frühere Versionen) des Eintragsbezeichners eines Microsoft Exchange Server 2010- oder Exchange Server 2013-Nachrichtenspeichers.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_STORE_ENTRYID_EMSMDB_V1  <br/> |
|Kennung:  <br/> |0x65F60102  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |ID-Eigenschaften  <br/> |
   
## <a name="remarks"></a>Hinweise

Ab Microsoft Outlook 2003 wurden die Server-FQDNs in die Eintrags-IDs integriert, wodurch zusätzliche RPCs für Verweise vermieden wurden. Dies führt jedoch zu längeren Eintrags-IDs und führt zu weiteren Szenarien, in denen die **CompareEntryIDs-Methode** verwendet werden muss, um zu ermitteln, ob zwei Eintrags-IDs gleichwertig sind. Die PR_STORE_ENTRYID_EMSMDB_V1 -Eigenschaft (PidTagStoreIdEmsbdbV1) zugrifft auf das ältere Format der Exchange Server-Eintrags-ID, die von Microsoft Outlook 2002 (Microsoft Office XP) und früheren Versionen verwendet wurde. Dies kann Platz sparen und auch die Anzahl der **CompareEntryIDs-Aufrufe** reduzieren, die erforderlich sind, um zu bestimmen, wann Eintrags-IDs gleichwertig sind. Beachten Sie, dass bei Verwendung der älteren Eintrags-IDs zum Öffnen eines Postfachs möglicherweise zusätzliche RPCs erforderlich sind, wenn ein Verweis erforderlich ist. 
  
Um auf die PR_STORE_ENTRYID_EMSMDB_V1 im zwischengespeicherten Modus zu zugreifen, müssen Sie den Cache mithilfe des MAPI_NO_CACHE-Flag mit der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) umgehen. Wenn **PR_STORE_ENTRYID_EMSMDB_V1** nicht verfügbar ist, sollte der Code auf die PR_STORE_ENTRYID. Nur Outlook 2003 bis Microsoft Outlook 2013 unterstützen die PR_STORE_ENTRYID_EMSMDB_V1-Eigenschaft. 
  
## <a name="see-also"></a>Siehe auch



[PidTagStoreEntryId (kanonische Eigenschaft)](pidtagstoreentryid-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


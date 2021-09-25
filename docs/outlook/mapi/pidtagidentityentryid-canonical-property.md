---
title: PidTagIdentityEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5f019d7175896095ff2ec3be75d1fd573a93fee4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600043"
---
# <a name="pidtagidentityentryid-canonical-property"></a>PidTagIdentityEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Eintragsbezeichner für die Identität eines Dienstanbieters, wie er in einem Messagingsystem definiert ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Kennung:  <br/> |0x3E01  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nicht als Eigenschaft für ein Objekt angezeigt, sondern nur als Spalte in einer Statustabelle. Sie ist Teil der Identität des Dienstanbieters, der die Zeile der Statustabelle verfügbar macht. Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann aber auf eine beliebige Darstellung verweisen, die der Anbieter im Messagingsystem definiert. 
  
Diese Eigenschaft wird häufig auf den entsprechenden Adressbucheintragsbezeichner festgelegt. 
  
Ein Dienstanbieter, der eine der Identitätseigenschaften angibt, sollte alle diese eigenschaften zuordnen. Anbieter, die zum gleichen Nachrichtendienst gehören, sollten dieselben Werte für die Identitätseigenschaften verfügbar machen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


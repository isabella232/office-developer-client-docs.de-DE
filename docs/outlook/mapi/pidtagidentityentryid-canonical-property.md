---
title: PidTagIdentityEntryId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityEntryId
api_type:
- HeaderDef
ms.assetid: 61a9d403-e0e5-45c3-8d18-4d53207ab927
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 099df2211e87e253ab1be520378b3a2b2ca7d4c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423335"
---
# <a name="pidtagidentityentryid-canonical-property"></a>PidTagIdentityEntryId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die Eintrags-ID für die Identität eines Dienstanbieters, wie sie in einem Messagingsystem definiert ist. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IDENTITY_ENTRYID  <br/> |
|Kennung:  <br/> |0x3E01  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird nicht als Eigenschaft für ein Objekt, sondern nur als Spalte in einer Statustabelle angezeigt. Sie ist Teil der Identität des Dienstanbieters, der die Zeile "Statustabelle" verfügbar macht. Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann jedoch auf jede Darstellung verweisen, die der Anbieter innerhalb des Messagingsystems definiert. 
  
Diese Proprerty wird häufig auf den entsprechenden Adressbucheintragsbezeichner festgelegt. 
  
Alle Identitätseigenschaften sollten von einem Dienstanbieter eingerichtet werden. Anbieter, die zum gleichen Nachrichtendienst gehören, sollten die gleichen Werte für die Identitätseigenschaften verfügbar machen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


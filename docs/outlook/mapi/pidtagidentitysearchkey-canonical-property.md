---
title: PidTagIdentitySearchKey (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentitySearchKey
api_type:
- HeaderDef
ms.assetid: 5fe55ba7-4ecd-4a43-ab5b-2ef595c2cdd9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12226039457782162eb74a19713fa77936332f80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565144"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>PidTagIdentitySearchKey (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält den Search-Schlüssel für einen Dienstanbieter Identität in einem messaging-System angegeben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x3E05  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-status  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird nicht als eine Eigenschaft für jedes Objekt, sondern nur als eine Spalte in einer Statustabelle angezeigt. Es ist Teil der Identität des Dienstanbieters die Tabellenzeile Status verfügbar zu machen. Identität des Anbieters in der Regel zu ihrer Firma auf dem Server verweist, doch verweisen auf eine beliebige Darstellung, die der Anbieter innerhalb der messaging-System definiert. 
  
Ein Dienstanbieter, die die Eigenschaften Identity Einrichtung sollte alle diese sind. Anbieter, die den Dienst angehören, sollte die gleichen Werte für die Identitätseigenschaften verfügbar machen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


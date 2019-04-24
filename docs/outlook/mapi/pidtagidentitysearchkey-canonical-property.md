---
title: Kanonische Pidtagidentitysearchkey (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5f5f5eaa41d6256bed69b2cd9a91208181d5bda1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346634"
---
# <a name="pidtagidentitysearchkey-canonical-property"></a>Kanonische Pidtagidentitysearchkey (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Suchschlüssel für die Identität eines Dienstanbieters gemäß der Definition in einem Messagingsystem. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_IDENTITY_SEARCH_KEY  <br/> |
|Kennung:  <br/> |0x3E05  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Status  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird nicht als Eigenschaft für ein Objekt, sondern nur als Spalte in einer Statustabelle angezeigt. Sie ist Teil der Identität des Dienstanbieters, der die Zeile der Statustabelle verfügbar macht. Die Identität des Anbieters bezieht sich in der Regel auf sein Konto auf dem Server, kann jedoch auf eine beliebige Darstellung verweisen, die der Anbieter innerhalb des Messagingsystems definiert. 
  
Ein Dienstanbieter, der eine beliebige Identitätseigenschaft bereit liefert, sollte alle Bereitstellung aufweisen. Anbieter, die zum gleichen Nachrichtendienst gehören, sollten dieselben Werte für die Identitätseigenschaften verfügbar machen. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMAPISession::QueryIdentity](imapisession-queryidentity.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


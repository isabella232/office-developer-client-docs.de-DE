---
title: Kanonische PidTagAbProviderId-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 84a2d5517d405ac6deb61f7c4679d6816e802404
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794024"
---
# <a name="pidtagabproviderid-canonical-property"></a>Kanonische PidTagAbProviderId-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält ein Adressbuchanbieter [MAPIUID](mapiuid.md) Struktur. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Bezeichner:  <br/> |0x3615  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Die Struktur **MAPIUID** identifiziert, welche Adressbuchanbieter diesem Container in der Containerhierarchie bereitstellt. Der Wert ist für jeden Anbieter eindeutig. 
  
Adressbuch-Dienstanbieter kann mehrere Bezeichner bereit. Beispielsweise kann ein Anbieter, der zwei verschiedene Container liefert in **PR_AB_PROVIDER_ID** eindeutigen Bezeichnern für jeden Container veröffentlichen. 
  
 **PR_AB_PROVIDER_ID** ist vergleichbar mit der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))-Eigenschaft für Nachrichtenspeicher. Clientanwendungen können **PR_AB_PROVIDER_ID** um verwandte Zeilen in einer Address Book Hierarchie-Tabelle zu finden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[Kanonische PidTagStoreProvider-Eigenschaft](pidtagstoreprovider-canonical-property.md)


[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


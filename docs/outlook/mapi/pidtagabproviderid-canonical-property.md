---
title: PidTagAbProviderId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422243"
---
# <a name="pidtagabproviderid-canonical-property"></a>PidTagAbProviderId (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die [MAPIUID-Struktur](mapiuid.md) eines Adressbuchanbieters. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Kennung:  <br/> |0x3615  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **MAPIUID-Struktur** gibt an, welcher Adressbuchanbieter diesen bestimmten Container in der Containerhierarchie liefert. Der Wert ist für jeden Anbieter eindeutig. 
  
Ein Adressbuchanbieter kann mehrere Bezeichner bereitstellen. Beispielsweise kann ein Anbieter, der zwei verschiedene Container liefert, **PR_AB_PROVIDER_ID** eindeutige Bezeichner für jeden Container veröffentlichen. 
  
 **PR_AB_PROVIDER_ID** entspricht der **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) -Eigenschaft für Nachrichtenspeicher. Clientanwendungen können **PR_AB_PROVIDER_ID** zum Suchen verwandter Zeilen in einer Adressbuchhierarchietabelle verwenden. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[PidTagStoreProvider (kanonische Eigenschaft)](pidtagstoreprovider-canonical-property.md)


[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


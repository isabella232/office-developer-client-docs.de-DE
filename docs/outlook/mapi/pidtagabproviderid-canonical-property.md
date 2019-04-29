---
title: Kanonische Pidtagabproviderid (-Eigenschaft
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
# <a name="pidtagabproviderid-canonical-property"></a>Kanonische Pidtagabproviderid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält die [MAPIUID](mapiuid.md) -Struktur eines Adressbuch Anbieters. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Kennung:  <br/> |0x3615  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **MAPIUID** -Struktur gibt an, welcher Adressbuchanbieter diesen Container in der Containerhierarchie bereitstellt. Der Wert ist für jeden Anbieter eindeutig. 
  
Ein Adressbuchanbieter kann mehr als einen Bezeichner bereitstellen. Beispielsweise kann ein Anbieter, der zwei verschiedene Container bereitstellt, in **PR_AB_PROVIDER_ID** eindeutige Bezeichner für jeden Container veröffentlichen. 
  
 **PR_AB_PROVIDER_ID** ist analog zur **PR_MDB_PROVIDER** ([pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md))-Eigenschaft für Nachrichtenspeicher. Client Anwendungen können **PR_AB_PROVIDER_ID** verwenden, um verwandte Zeilen in einer Adressbuch-Hierarchietabelle zu suchen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header Dateien

Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[Kanonische Pidtagstoreprovider (-Eigenschaft](pidtagstoreprovider-canonical-property.md)


[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


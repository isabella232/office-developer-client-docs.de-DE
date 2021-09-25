---
title: PidTagAbProviderId (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 30569efe44960486940e0b39b44ca43d911a8b76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561040"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **MAPIUID-Struktur** identifiziert, welcher Adressbuchanbieter diesen bestimmten Container in der Containerhierarchie bereitstellt. Der Wert ist für jeden Anbieter eindeutig. 
  
Ein Adressbuchanbieter kann mehrere Bezeichner bereitstellen. Beispielsweise kann ein Anbieter, der zwei verschiedene Container bereitstellt, in **PR_AB_PROVIDER_ID** eindeutigen Bezeichnern für jeden Container veröffentlichen. 
  
 **PR_AB_PROVIDER_ID** entspricht der **Eigenschaft PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) für Nachrichtenspeicher. Clientanwendungen können **PR_AB_PROVIDER_ID** verwenden, um verwandte Zeilen in einer Adressbuchhierarchietabelle zu suchen. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)
  
[Kanonische PidTagStoreProvider-Eigenschaft](pidtagstoreprovider-canonical-property.md)


[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


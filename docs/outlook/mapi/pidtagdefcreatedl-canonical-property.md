---
title: Kanonische Pidtagdefcreatedl (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ff5d35104e9effc27c405b716cb61cf4643677b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359955"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Kanonische Pidtagdefcreatedl (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält den Vorlagen Eintragsbezeichner für eine Standardverteilerliste. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Kennung:  <br/> |0x3611  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Client Anwendungen verwenden diese Eigenschaft, um eine Verteilerliste in einem Container zu erstellen. Die Unterstützung der Eintragserstellung ist für Adressbuchcontainer optional. diejenigen, die es nicht unterstützen, müssen diese Eigenschaft nicht offen legen. 
  
Diese Eigenschaft gibt einen Eintrag an, der in der **PR_CREATE_TEMPLATES** ([pidtagcreatetemplates (](pidtagcreatetemplates-canonical-property.md))-Eigenschaft für Verteilerlisten angezeigt werden kann. Nach dem Abrufen des Bezeichners verwendet der Client diesen bei einem Aufruf der [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode. Der Eintrag stellt die Vorlage für die Standardverteilerliste dar. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


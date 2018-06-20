---
title: Kanonische PidTagDefCreateMailuser-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateMailuser
api_type:
- HeaderDef
ms.assetid: e8293dc9-f2f1-4065-89f4-e734a8db63df
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 33c62b81982aaac3659ad4d41ea2cf5298b42287
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794290"
---
# <a name="pidtagdefcreatemailuser-canonical-property"></a>Kanonische PidTagDefCreateMailuser-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Die Vorlage Eintrags-ID für eine standardmäßige messaging User-Objekt enthält. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_DEF_CREATE_MAILUSER  <br/> |
|Bezeichner:  <br/> |0x3612  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Clientanwendungen mit dieser Eigenschaft können Sie um ein messaging User-Objekt in einem Container zu erstellen. Unterstützung von Eintrag Creation ist optional für Address Book Container. die, die nicht unterstützen sind nicht erforderlich, diese Eigenschaft verfügbar machen. 
  
Diese Eigenschaft gibt einen Eintrag, der angezeigt werden, kann in der Eigenschaft **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) für die messaging-Benutzer. Wenn den Bezeichner erhalten haben, verwendet der Client es in einem Aufruf der [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode. Der Eintrag stellt die Vorlage für den Standard-messaging-Benutzer dar. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


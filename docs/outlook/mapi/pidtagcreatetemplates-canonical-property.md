---
title: PidTagCreateTemplates (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0dea422ab72449272b8940ecc16c22d513bd75eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563707"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Tabellenobjekt, das Eintragsbezeichner für Dialogfeldvorlagen enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Kennung:  <br/> |0x3604  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um zu erfahren, welche Vorlagenobjekte in einem Container erstellt werden können, rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für diese Eigenschaft auf. Das resultierende Objekt ist die einmalige Tabelle, die die Eintragsbezeichner für alle Vorlagen bereitstellt, die Sie innerhalb des Containers erstellen können. 
  
Rufen Sie zum Erstellen der Vorlagenobjekte die **CreateEntry-Methode** des Containerobjekts für die **Spaltenwerte PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaligen Tabelle auf.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


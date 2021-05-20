---
title: PidTagCreateTemplates (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCreateTemplates
api_type:
- HeaderDef
ms.assetid: d2530009-5de3-4872-a0a5-be1389c4206e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438183"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Tabellenobjekt, das Eingabebezeichner für Dialogfeldvorlagen enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Kennung:  <br/> |0x3604  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Hinweise

Um zu erfahren, welche Vorlagenobjekte in einem Container erstellt werden können, rufen Sie die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) für diese Eigenschaft auf. Das resultierende Objekt ist die einmal aufgeführte Tabelle, die die Eintragsbezeichner für alle Vorlagen angibt, die Sie innerhalb des Containers erstellen können. 
  
Rufen Sie zum Erstellen der Vorlagenobjekte die **CreateEntry-Methode** des Containerobjekts in den **Spaltenwerten PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaltabelle auf.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


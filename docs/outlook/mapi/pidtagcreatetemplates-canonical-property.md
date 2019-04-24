---
title: Kanonische Pidtagcreatetemplates (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 08cf1faa0c3cc4cf61e2253b0026361704fdd0e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269937"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>Kanonische Pidtagcreatetemplates (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein eingebettetes Table-Objekt, das Eingabe-IDs für Dialogfeldvorlagen enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Kennung:  <br/> |0x3604  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um zu erfahren, welche Vorlagenobjekte innerhalb eines Containers erstellt werden können, rufen Sie die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode für diese Eigenschaft auf. Das resultierende Objekt ist die einmalige Tabelle, die die Eintragsbezeichner für alle Vorlagen enthält, die Sie innerhalb des Containers erstellen können. 
  
Zum Erstellen der Template-Objekte rufen Sie die createEntry **** -Methode des Container-Objekts für die **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaligen Tabelle auf.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


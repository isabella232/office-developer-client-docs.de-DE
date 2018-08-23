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
ms.openlocfilehash: 28611e442f816e4d091cc6b29e2ee69195a63d09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563359"
---
# <a name="pidtagcreatetemplates-canonical-property"></a>PidTagCreateTemplates (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält eine eingebettete Table-Objekt, das Dialogfeld Feld Vorlage-Eintragsbezeichner enthält. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_CREATE_TEMPLATES  <br/> |
|Kennung:  <br/> |0x3604  <br/> |
|Datentyp:  <br/> |PT_OBJECT  <br/> |
|Bereich:  <br/> |Adressbuch  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Welche Vorlage erhalten Sie Objekte in einem Container erstellt werden können, rufen Sie die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode für diese Eigenschaft. Das resultierende Objekt ist der einmaligen Tabelle mit den Eintrag-IDs für alle Vorlagen, die Sie innerhalb des Containers erstellen können. 
  
Rufen Sie das Containerobjekt **CreateEntry** -Methode zum Erstellen der Vorlagenobjekte auf die Spaltenwerte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) aus der einmaligen Tabelle.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IABContainer::CreateEntry](iabcontainer-createentry.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


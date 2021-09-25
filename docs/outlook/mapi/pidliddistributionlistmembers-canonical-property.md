---
title: PidLidDistributionListMembers (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 946c8b12a2410b63bfaa22d9e6bde6de16167ff9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575183"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Liste der EntryIds der Objekte an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidDLMembers  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008055  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Mitglieder der persönlichen Verteilerliste können andere persönliche Verteilerlisten, in einem Kontakt enthaltene elektronische Adressen, Benutzer der globalen Adressliste oder Verteilerlisten oder einmalige E-Mail-Adressen sein. Das Format jeder EntryId muss entweder eine einmalige EntryId sein, wie in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) angegeben, oder eine umschlossene EntryId. 
  
Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicherstellen, dass seine Gesamtgröße weniger als 15.000 Bytes beträgt.
  
Diese Eigenschaft gibt die Liste der einmaligen EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen. Diese einmaligen EntryIds kapseln Anzeigenamen und E-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.
  
Wenn der Client oder der Server diese Eigenschaft festlegen, muss sie mit dieser Eigenschaft **dispidDLMembers** für jeden Eintrag in der **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) -Eigenschaft synchronisiert werden, es muss ein Eintrag an der gleichen Position in der **dispidDLOneOffMembers** vorhanden sein.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


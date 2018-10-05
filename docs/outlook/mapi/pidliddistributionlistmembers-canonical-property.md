---
title: PidLidDistributionListMembers (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389967"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Liste der EntryIds-Objekte, die die Elemente der persönlichen Verteilerliste entsprechen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidDLMembers  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008055  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Mitglieder der persönlichen Verteilerliste möglicherweise andere persönlichen Verteilerlisten, elektronische Adressen, die in einem Kontakt, Global Address List Benutzer oder Verteilerlisten oder einmaligen e-Mail-Adressen enthalten sind. Das Format der einzelnen EntryId muss es sich um einen einmaligen Eintrags-ID, wie in [[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) angegeben oder eine gepackten EntryId sein. 
  
Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicher, dass die Gesamtgröße der kleiner als 15.000 Bytes.
  
Diese Eigenschaft gibt die Liste der einmaligen EntryIds, die die Elemente der persönlichen Verteilerliste entsprechen. Diese einmaligen EntryIds kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.
  
Wenn der Client oder der Server wird diese Eigenschaft festzulegen, müssen Sie mit dieser Eigenschaft **DispidDLMembers** für jeden Eintrag in der Eigenschaft **DispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) synchronisiert werden, muss ein Eintrag in der derselben Position in der **DispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


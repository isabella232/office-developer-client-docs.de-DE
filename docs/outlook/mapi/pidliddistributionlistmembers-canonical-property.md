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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c27513474048e9805bc29116aa094bc47f8f0cae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793494"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>PidLidDistributionListMembers (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Gibt die Liste der EntryIds-Objekte, die die Elemente der persönlichen Verteilerliste entsprechen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidDLMembers  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008055  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mitglieder der persönlichen Verteilerliste möglicherweise andere persönlichen Verteilerlisten, elektronische Adressen, die in einem Kontakt, Global Address List Benutzer oder Verteilerlisten oder einmaligen e-Mail-Adressen enthalten sind. Das Format der einzelnen EntryId muss es sich um einen einmaligen Eintrags-ID, wie in [[MS-OXCDATA]](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) angegeben oder eine gepackten EntryId sein. 
  
Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicher, dass die Gesamtgröße der kleiner als 15.000 Bytes.
  
Diese Eigenschaft gibt die Liste der einmaligen EntryIds, die die Elemente der persönlichen Verteilerliste entsprechen. Diese einmaligen EntryIds kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.
  
Wenn der Client oder der Server wird diese Eigenschaft festzulegen, müssen Sie mit dieser Eigenschaft **DispidDLMembers** für jeden Eintrag in der Eigenschaft **DispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)) synchronisiert werden, muss ein Eintrag in der derselben Position in der **DispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


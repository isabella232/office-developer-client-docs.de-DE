---
title: Kanonische Pidliddistributionlistmembers (-Eigenschaft
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
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335070"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Kanonische Pidliddistributionlistmembers (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt die Liste der EntryIds der Objekte an, die den Mitgliedern der persönlichen Verteilerliste entsprechen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidDLMembers  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long-ID (Deckel):  <br/> |0x00008055  <br/> |
|Datentyp:  <br/> |PT_MV_BINARY  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Mitglieder der persönlichen Verteilerliste können andere persönliche Verteilerlisten, Elektronische Adressen in einem Kontakt, globale Adresslisten Benutzer oder Verteilerlisten oder einmalige e-Mail-Adressen sein. Das Format jeder Eintrags-Nr. muss eine einmalige Eintrags-oder Eingabe-Nr sein, wie in [[MS-OXCDATA] angegeben,](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) oder eine einGebundene Eintrags-Nr. 
  
Beim Festlegen dieser Eigenschaft muss der Client oder der Server sicherstellen, dass die Gesamtgröße kleiner als 15.000 Byte ist.
  
Diese Eigenschaft gibt die Liste der einmaligen EntryIds an, die den Mitgliedern der persönlichen Verteilerliste entsprechen. Diese einmalige EntryIds Kapseln Anzeigenamen und e-Mail-Adressen der Mitglieder der persönlichen Verteilerliste.
  
Wenn der Client oder der Server diese Eigenschaft festlegen, muss Sie mit dieser Eigenschaft **dispidDLMembers** für jeden Eintrag in der **dispidDLOneOffMembers** ([pidliddistributionlistoneoffmembers (](pidliddistributionlistoneoffmembers-canonical-property.md))-Eigenschaft synchronisiert werden, es muss einen Eintrag in der dieselbe Position in der **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge an, die für Kontakte und persönliche Verteilerlisten zulässig sind.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


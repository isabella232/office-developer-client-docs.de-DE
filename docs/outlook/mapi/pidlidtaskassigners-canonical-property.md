---
title: PidLidTaskAssigners (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskAssigners
api_type:
- COM
ms.assetid: 07500bd0-bcff-4b03-8ed3-80508875e253
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1f72757c8a2104dd1f936d893fa226192981e740
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583709"
---
# <a name="pidlidtaskassigners-canonical-property"></a>PidLidTaskAssigners (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Stapel von Einträgen, die Vorgangsempfänger darstellen. Der letzte Aufgabenempfänger wird oben im Stapel angezeigt.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskMyDelegators  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008117  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der Client eine Aufgabenanforderung empfängt, wird diese Eigenschaft angefügt, deren Struktur in [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)definiert ist, einem Eintrag, der den Absender der Aufgabe darstellt. Wenn der Client eine Ablehnung einer Aufgabe empfängt, entfernt der Client den letzten Aufgabenzuweisungseintrag aus dieser Eigenschaft. Wenn der Client eine Aufgabenantwort sendet, sendet der Client sie an den letzten Aufgabenempfänger, der im Wert dieser Eigenschaft aufgeführt ist.
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Aufgabenzuweisungen und Aufgabenaktualisierungen modellieren 
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


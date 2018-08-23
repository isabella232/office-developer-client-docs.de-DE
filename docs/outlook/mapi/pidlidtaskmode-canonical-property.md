---
title: PidLidTaskMode (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskMode
api_type:
- COM
ms.assetid: 185db683-301a-4d91-a583-6959853fa1ad
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: bc8e4dfe934d516c07d5532ba6a95e51a3cbf962
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578080"
---
# <a name="pidlidtaskmode-canonical-property"></a>PidLidTaskMode (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt den Zuordnungsstatus des Vorgangs.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskMode  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Common  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008518  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert muss eine der folgenden sein:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Die Aufgabe wird nicht zugewiesen.  <br/> |
|0x00000001  <br/> |Die Aufgabe ist in eine Aufgabenanfrage eingebettet.  <br/> |
|0x00000002  <br/> |Die Aufgabe wurde vom Beauftragte für die Aufgabe angenommen.  <br/> |
|0 x 00000003  <br/> |Die Aufgabe wurde vom Beauftragte für die Aufgabe abgelehnt.  <br/> |
|0 x 00000004  <br/> |Die Aufgabe ist in einem Update Aufgabe eingebettet.  <br/> |
|0 x 00000005  <br/> |Die Aufgabe wurde die Aufgabe delegierende Person zugewiesen.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](http://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


---
title: Kanonische PidLidContactItemData-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793482"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Kanonische PidLidContactItemData-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Verwendet, um die Kontaktinformationen anzuzeigen.
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |dispidContactItemData  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008007  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn dieser Parameter angegeben wurde, muss die Eigenschaft sechs Einträge, die jeweils entsprechen einer eingeblendeten Felder in der Benutzeroberfläche der Anwendung verfügen.
  
|**1 beginnenden Index in der mehrwertige Eigenschaft**|**Der Wert muss eine der folgenden sein:**|**Beschreibung**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |Die Anwendung sollte home-Adresse des Kontakts angezeigt werden.  <br/> |
|1  <br/> |0 x 00000002 oder 0 x 00000000  <br/> |Die Anwendung sollte Arbeit des Kontakts angezeigt werden.  <br/> |
|1  <br/> |0 x 00000003  <br/> |Die Anwendung sollte angezeigt werden des Kontakts die Adresse.  <br/> |
|2  <br/> |0x00008080  <br/> |Die Anwendung sollte Email1 angezeigt werden.  <br/> |
|2  <br/> |0x00008090  <br/> |Die Anwendung sollte Email2 angezeigt werden.  <br/> |
|2  <br/> |0x000080A0  <br/> |Die Anwendung sollte Email3 angezeigt werden.  <br/> |
|3,4,5,6  <br/> |PropertyID Telefon Eigenschaften oder eine der Fax-Zahlen, die in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind.  <br/> |Die Anwendung sollte die entsprechende Eigenschaft angezeigt werden.  <br/> |
   
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


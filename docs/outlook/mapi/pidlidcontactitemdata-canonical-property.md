---
title: Kanonische PidLidContactItemData-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f1353f12c7faf067ff983cf1a559796a3b85c72c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575190"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Kanonische PidLidContactItemData-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Wird verwendet, um die Kontaktinformationen anzuzeigen.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidContactItemData  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008007  <br/> |
|Datentyp:  <br/> |PT_MV_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn vorhanden, muss die Eigenschaft sechs Einträge aufweisen, die jeweils einem sichtbaren Feld auf der Benutzeroberfläche der Anwendung entsprechen.
  
|**Ein basierter Index in die mehrwertige Eigenschaft**|**Der Wert muss einer der folgenden Werte sein:**|**Beschreibung**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |Die Anwendung sollte die Privatadresse des Kontakts anzeigen.  <br/> |
|1  <br/> |0x00000002 oder 0x00000000  <br/> |Die Anwendung sollte die Arbeit des Kontakts anzeigen.  <br/> |
|1  <br/> |0x00000003  <br/> |Die Anwendung sollte die andere Adresse des Kontakts anzeigen.  <br/> |
|2  <br/> |0x00008080  <br/> |Die Anwendung sollte Email1 anzeigen.  <br/> |
|2  <br/> |0x00008090  <br/> |Die Anwendung sollte Email2 anzeigen.  <br/> |
|2  <br/> |0x000080A0  <br/> |Die Anwendung sollte Email3 anzeigen.  <br/> |
|3,4,5,6  <br/> |PropertyID einer der Telefoneigenschaften oder einer der Faxnummern, die in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)angegeben sind.  <br/> |Die Anwendung sollte die entsprechende Eigenschaft anzeigen.  <br/> |
   
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


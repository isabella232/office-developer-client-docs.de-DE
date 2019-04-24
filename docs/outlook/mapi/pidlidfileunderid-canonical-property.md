---
title: Kanonische Pidlidfileunderid (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355706"
---
# <a name="pidlidfileunderid-canonical-property"></a>Kanonische Pidlidfileunderid (-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt an, wie der Wert der **dispidFileUnder** ([pidlidfileunder (](pidlidfileunder-canonical-property.md))-Eigenschaft generiert und neu berechnet wird, wenn sich die Eigenschaften anderer Kontaktnamen ändern.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFileUnderId  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Address  <br/> |
|Long-ID (Deckel):  <br/> |0x00008006  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn diese Eigenschaft fehlt oder auf einen Wert festgelegt ist, der nicht in der Tabelle unten oder in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)detailliert ist, kann die Anwendung ihre eigene Logik auswählen, um den Wert der **dispidFileUnder** neu zu berechnen, wenn sich die Eigenschaften anderer Kontaktnamen ändern. 
  
In der folgenden Tabelle wird die Notation <PropertyName> verwendet, um "den Wert von PropertyName" anzugeben. Wenn beispielsweise der Wert der **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))-Eigenschaft "Smith" lautet und der Wert der **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))-Eigenschaft "Ben" lautet, gibt "<PidTagGivenName> <PidTagSurname>" die Zeichenfolge "Ben Smith" an. In der Tabelle gibt "\r" ein Wagenrücklaufzeichen an, "\n" gibt ein Zeilenvorschubzeichen an und <space> stellt ein Leerzeichen dar.
  
|**Wert der **dispidFileUnderId** -Eigenschaft**|**Beschreibung der **dispidFileUnder** -Eigenschaft**|
|:-----|:-----|
|0x00000000  <br/> |Leere PT_UNICODE.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\>Space pidtagmiddlename (\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<\>PidTagGivenName\<Space\>pidtagmiddlename (\>"\<  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>pidtagmiddlename (\>"\<\>\<  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Space\>\<PidTagGivenName Space\>pidtagmiddlename (\>"\<\>\<  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>Space pidtagmiddlename (\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<Space\>\<\>PidTagGivenName Space\>pidtagmiddlename (\r\n PidTagCompanyName"\<\>\<\>\<  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<Space\>\<\<PidTagGivenName\>Space pidtagmiddlename (\>Space\>pidtaggeneration (\>"\<\>\<\<  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<Space\>\<\<pidtagmiddlename (\>Space PidTagSurname\>Space\>pidtaggeneration (\>"\<\>\<\<  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>Space\>pidtagmiddlename (\>Space\>pidtaggeneration ("\<\<\<\<  <br/> |
|0xfffffffd  <br/> |Gibt an, dass die Anwendung beim Anzeigen des Kontakts versuchen sollte, den aktuellen Wert von **dispidFileUnder** und andere Kontakteigenschaften zu verwenden, um eine "beste Übereinstimmung" für **dispidFileUnderId** zu einem der vorherigen Werte in dieser Tabelle zu finden.  <br/> |
|0xfffffffe  <br/> |Gibt an, dass die Anwendung beim Anzeigen des Kontakts die entsprechenden Standardwerte (entsprechend dem Gebietsschema der Sprache) für **dispidFileUnderId** und **dispidFileUnder** aktualisieren soll, um die Auswahl zu erfüllen.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** ist ein vom Benutzer bereitgestellter PT_UNICODE und sollte nicht geändert werden, wenn sich eine andere Kontaktnamens Eigenschaft ändert.  <br/> |
   
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


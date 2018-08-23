---
title: PidLidFileUnderId (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0a4fdb94877fb9491005fc650c206ffefd3f8b94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578416"
---
# <a name="pidlidfileunderid-canonical-property"></a>PidLidFileUnderId (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt an, wie generieren und den Wert der Eigenschaft **DispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) neu berechnen, wenn andere Kontakt benennen Eigenschaften ändern.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidFileUnderId  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Address  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008006  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Kontakt  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn diese Eigenschaft nicht vorhanden ist oder auf einen anderen Wert nicht um einen detaillierten in der folgenden Tabelle oder in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)festlegen, können die Anwendung seine eigene Logik für den Wert der **DispidFileUnder** als andere Kontaktnamen Eigenschaften Änderung neu zu berechnen. 
  
In der folgenden Tabelle, die Notation <PropertyName> wird verwendet, um "den Wert von PropertyName" angeben. Wenn der Wert der Eigenschaft **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) ist "Smith", und der Wert der Eigenschaft **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) "Peter", dann beträgt beispielsweise "<PidTagGivenName> <PidTagSurname>" gibt die Zeichenfolge "Ben Smith". In der Tabelle "\r" gibt ein Wagenrücklaufzeichen, "\n" gibt ein Zeichen Zeilenvorschub und <space> ein Leerzeichen dar.
  
|**Der Wert der **DispidFileUnderId** -Eigenschaft**|**Beschreibung der **DispidFileUnder** -Eigenschaft**|
|:-----|:-----|
|0x00000000  <br/> |Leere PT_UNICODE.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>"  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\<Speicherplatz\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagSurname\>\<Speicherplatz\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<Speicherplatz\>\<PidTagMiddleName\>\<Speicherplatz\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Gibt an, dass, wenn den Kontakt angezeigt werden, die Anwendung sollte den aktuellen Wert der **DispidFileUnder** und andere Kontakten Eigenschaften verwenden, um "beste Übereinstimmung" für **DispidFileUnderId** auf einen der vorherigen Werte in dieser Tabelle zu finden.  <br/> |
|0xFFFFFFFE  <br/> |Gibt an, dass beim Anzeigen des Kontakts die Anwendung wählen Sie die entsprechenden Standardwerte (gemäß dem Gebietsschema) für **DispidFileUnderId** und **DispidFileUnder** die Wahl entsprechend aktualisieren sollten.  <br/> |
|0xFFFFFFFF  <br/> |**DispidFileUnder** ist eine vom Benutzer bereitgestellte PT_UNICODE und sollte nicht geändert werden, wenn eine andere Kontaktnamen-Eigenschaft ändert.  <br/> |
   
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


---
title: PidLidTaskStatus (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386866"
---
# <a name="pidlidtaskstatus-canonical-property"></a>PidLidTaskStatus (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Status des Benutzers Fortschritt für den Vorgang.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskStatus  <br/> |
|-Eigenschaft festgelegt:  <br/> |PSETID_Task  <br/> |
|Long-ID (Abdeckung):  <br/> |0x00008101  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Wert dieser Eigenschaft muss auf einen der folgenden festgelegt werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Der Benutzer wurde Arbeit für die Aufgabe nicht gestartet werden. Wenn dieser Wert festgelegt ist, muss **DispidPercentComplete** ([PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)) 0,0 sein.  <br/> |
|0x00000001  <br/> |Der Benutzer Arbeit für diesen Vorgang wird gerade durchgeführt. Wenn dieser Wert festgelegt ist, muss **DispidPercentComplete** größer als 0,0 und kleiner als 1,0 sein.  <br/> |
|0x00000002  <br/> |Der Benutzer Arbeit für diesen Vorgang ist abgeschlossen. Wenn dieser Wert festgelegt ist, **DispidPercentComplete** muss 1.0, **DispidTaskDateCompleted** ([PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)) muss das aktuelle Datum und **DispidTaskComplete** ([PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)) muss auf TRUE festgelegt sein.  <br/> |
|0 x 00000003  <br/> |Der Benutzer wartet auf jemand.  <br/> |
|0 x 00000004  <br/> |Der Benutzer hat die Arbeit für den Vorgang zurückgestellt.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Mehrere Objekte, die das elektronische Äquivalent von Aufgaben, vorgangszuordnungen und vorgangsaktualisierungen Modell definiert.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Erstellen und Ordner mit Sonderfunktion in einem Postfach suchen.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Konvertiert von Internet-standard-e-Mail-Konventionen in Message-Objekten.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446, RFC2447, und Termine und meeting-Objekte.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und Server.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
## <a name="see-also"></a>Siehe auch



[PidLidPercentComplete (kanonische Eigenschaft)](pidlidpercentcomplete-canonical-property.md)
  
[PidLidTaskDateCompleted (kanonische Eigenschaft)](pidlidtaskdatecompleted-canonical-property.md)
  
[PidLidTaskComplete (kanonische Eigenschaft)](pidlidtaskcomplete-canonical-property.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


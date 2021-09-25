---
title: Kanonische PidLidTaskState-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTaskState
api_type:
- COM
ms.assetid: 06d1f8a3-53e1-4c9a-9703-75de7a11a772
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 083a4105f851c77f16b75575158bd317acabf8d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591710"
---
# <a name="pidlidtaskstate-canonical-property"></a>Kanonische PidLidTaskState-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den aktuellen Zuweisungsstatus des Vorgangs an.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |dispidTaskState  <br/> |
|Eigenschaftensatz:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008113  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Aufgabe  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Der Wert dieser Eigenschaft muss einer der folgenden Werte sein:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0x00000000  <br/> |Diese Aufgabe wurde erstellt, um einer Aufgabe zu entsprechen, die in eine Vorgangsverweigerung eingebettet war, aber nicht lokal gefunden werden konnte.  <br/> |
|0x00000001  <br/> |Die Aufgabe ist nicht zugewiesen.  <br/> |
|0x00000002  <br/> |Die Aufgabe ist die Kopie eines zugewiesenen Vorgangs durch den Zugewiesenen.  <br/> |
|0x00000003  <br/> |Die Aufgabe ist die Kopie des Aufgabenempfängers einer zugewiesenen Aufgabe.  <br/> |
|0x00000004  <br/> |Die Aufgabe ist die Kopie eines abgelehnten Vorgangs durch den Aufgabenempfänger.  <br/> |
   
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Stellt Eigenschaftssatzdefinitionen und Verweise auf verwandte Exchange Server Protokollspezifikationen bereit.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Definiert mehrere Objekte, die das elektronische Äquivalent von Aufgaben, Aufgabenzuweisungen und Aufgabenaktualisierungen modellieren.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Erstellen und Suchen der speziellen Ordner in einem Postfach an.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Konvertiert zwischen IETF RFC2445, RFC2446 und RFC2447 sowie Termin- und Besprechungsobjekten.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Verarbeitet die Reihenfolge und den Fluss für Datenübertragungen zwischen einem Client und einem Server.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


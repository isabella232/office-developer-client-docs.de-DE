---
title: PidTagExtendedFolderFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382659"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>PidTagExtendedFolderFlags (kanonische Eigenschaft)
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erweiterte Flags zu einem Ordner enthält.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Kennung:  <br/> |0x36DA  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist ein binären Stream, der codierte untergeordnete Eigenschaften für den Ordner enthält. Es wird als eine Reihe von variabler Länge Sub-Elemente formatiert. Die ersten 8 Bits des Elements Sub ist ein Feld-ID, die angibt, welche Art von Flag das Sub-Element darstellt. Die zweite 8 Bits ist die Anzahl von Bytes der Daten, die folgen.
  
Mögliche Werte für ID:
  
- Ungültig
    
   Verwenden Sie diesen Wert nicht
    
- ExtendedFlags
    
   Die Daten ist ein hochgestelltes vier Byte-Wert:
    
   |**Bits**|**Beschreibung**|
   |:-----|:-----|
   |0-1  <br/> |Reserviert.  <br/> |
   |2  <br/> |Auf 0 festgelegt, wenn die Anwendung eine Beschreibung der Richtlinie angezeigt werden soll.  <br/> |
   |3 bis 5  <br/> |Reserviert.  <br/> |
   |6 und 7  <br/> |Steuert die Anzeige der Anzahl von Nachrichten in den Ordner.  <br/> 0 – verwenden Sie die Standardeinstellung  <br/> 1 – die Anzahl der ungelesenen Nachrichten verwenden  <br/> 3 - verwenden Sie die Gesamtzahl der Nachrichten  <br/> |
   |8-31  <br/> |Reserviert.  <br/> |
   
Reservierte Artikel können ignoriert werden, aber die vorhandenen Werte beibehalten werden müssen.
    
- SearchFolderID
    
   Das Datenfeld ist ein 16-Byte-Feld. Wenn die Anwendung einen beständigen Suchordner erstellt, muss dieses Feld für den Ordner auf den gleichen Wert wie der **PR_WB_SF_TAG** festgelegt ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binäre Eigenschaft für die Suche Ordner Nachricht.
    
- ToDoFolderVersion
    
   Das Datenfeld ist ein 4-Byte-Feld. Wenn die Anwendung den Suchordner Aufgabe erstellt, muss den Wert dieses Felds für den Ordner der little-Endian-Ganzzahlwert der "0x000c0000" festgelegt:
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Konfigurationsdaten, wie etwa freigegebene Kategorielisten und Arbeitszeiten.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Operationen für das Bearbeiten der Liste einer Suchkonfiguration-Ordner.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md)
- [Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
- [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


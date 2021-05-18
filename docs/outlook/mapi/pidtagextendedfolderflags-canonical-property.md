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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316352"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>PidTagExtendedFolderFlags (kanonische Eigenschaft)
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält erweiterte Flags für einen Ordner.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Kennung:  <br/> |0x36DA  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist ein binärer Datenstrom, der codierte Untereigenschaften für den Ordner enthält. Es ist als eine Reihe von Unterelementen mit variabler Länge formatiert. Die ersten 8 Bits des Unterelements sind ein ID-Feld, das angibt, welche Art von Kennzeichen das Unterelement darstellt. Die zweiten 8 Bit sind die Anzahl der folgenden Bytes an Daten.
  
Mögliche ID-Werte sind:
  
- Ungültig
    
   Verwenden Sie diesen Wert nicht
    
- ExtendedFlags
    
   Die Daten sind ein Vier-Byte-Wert, der wie folgt formatiert ist:
    
   |**Bit**|**Beschreibung**|
   |:-----|:-----|
   |0-1  <br/> |Reserviert.  <br/> |
   |2  <br/> |Auf 0 festgelegt, wenn die Anwendung eine Richtlinienbeschreibung anzeigen soll.  <br/> |
   |3-5  <br/> |Reserviert.  <br/> |
   |6-7  <br/> |Steuert die Anzeige der Anzahl der Nachrichten im Ordner.  <br/> 0 – Verwenden der Standardeinstellung  <br/> 1 – Verwenden der Anzahl ungelesener Nachrichten  <br/> 3 – Verwenden der Gesamtanzahl von Nachrichten  <br/> |
   |8-31  <br/> |Reserviert.  <br/> |
   
Reservierte Elemente können ignoriert werden, vorhandene Werte müssen jedoch beibehalten werden.
    
- SearchFolderID
    
   Das Datenfeld ist ein 16-Byte-Feld. Wenn die Anwendung einen beständigen Suchordner erstellt, muss sie dieses Feld für den Ordner auf denselben Wert wie die **binäre eigenschaft PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)für die Nachricht des Suchordners festlegen.
    
- ToDoFolderVersion
    
   Das Datenfeld ist ein 4-Byte-Feld. Wenn die Anwendung den To-Do-Suchordner erstellt, muss sie den Wert dieses Felds für den Ordner auf den ganzzahligen Kleinwert von " 0x000c0000":
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md)
- [KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
- [Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


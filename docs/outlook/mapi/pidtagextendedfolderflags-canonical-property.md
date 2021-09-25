---
title: PidTagExtendedFolderFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ef34f390a3b58d805ed023862a8621d8932de0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616467"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>PidTagExtendedFolderFlags (kanonische Eigenschaft)
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält erweiterte Flags zu einem Ordner.
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Kennung:  <br/> |0x36DA  <br/> |
|Datentyp:  <br/> |PT_BINARY  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist ein binärer Datenstrom, der codierte Untereigenschaften für den Ordner enthält. Es ist als eine Reihe von Untergeordneten Elementen variabler Länge formatiert. Die ersten 8 Bits des Unterelements sind ein ID-Feld, das angibt, welche Art von Flag das Unterelement darstellt. Bei den zweiten 8 Bits handelt es sich um die Anzahl der folgenden Byte an Daten.
  
Mögliche ID-Werte sind:
  
- Ungültig
    
   Verwenden Sie diesen Wert nicht
    
- ExtendedFlags
    
   Bei den Daten handelt es sich um einen vier-Byte-Wert, der wie folgt formatiert ist:
    
   |**Bit**|**Beschreibung**|
   |:-----|:-----|
   |0-1  <br/> |Reserviert.  <br/> |
   |2  <br/> |Auf 0 festgelegt, wenn die Anwendung eine Richtlinienbeschreibung anzeigen soll.  <br/> |
   |3-5  <br/> |Reserviert.  <br/> |
   |6-7  <br/> |Steuert die Anzeige der Anzahl der Nachrichten im Ordner.  <br/> 0 – Standardeinstellung verwenden  <br/> 1 – Verwenden der Anzahl ungelesener Nachrichten  <br/> 3 – Gesamtanzahl der Nachrichten verwenden  <br/> |
   |8-31  <br/> |Reserviert.  <br/> |
   
Reservierte Elemente können ignoriert werden, vorhandene Werte müssen jedoch beibehalten werden.
    
- SearchFolderID
    
   Das Datenfeld ist ein 16-Byte-Feld. Wenn die Anwendung einen permanenten Suchordner erstellt, muss sie dieses Feld für den Ordner auf denselben Wert wie die binäre Eigenschaft **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)in der Suchordnernachricht festlegen.
    
- ToDoFolderVersion
    
   Das Datenfeld ist ein 4-Byte-Feld. Wenn die Anwendung den Aufgabensucheordner erstellt, muss sie den Wert dieses Felds für den Ordner auf den wert für die kleine endische ganze Zahl von " 0x000c0000" festlegen:
    
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Gibt den Speicherort und die Eigenschaften von Client- und Serverkonfigurationsdaten an, z. B. freigegebene Kategorielisten und Arbeitszeiten.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Gibt die Eigenschaften und Vorgänge zum Bearbeiten einer Suchordnerlistenkonfiguration an.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch

- [MAPI-Eigenschaften](mapi-properties.md)
- [KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
- [Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
- [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


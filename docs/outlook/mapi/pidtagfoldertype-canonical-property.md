---
title: Kanonische PidTagFolderType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2520a7544eb4ba39cd83a7a0aa65b98bd8a67deb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794381"
---
# <a name="pidtagfoldertype-canonical-property"></a>Kanonische PidTagFolderType-Eigenschaft

  
  
**Betrifft**: Outlook 
  
Enthält eine Konstante, die den Ordner angibt. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_FOLDER_TYPE  <br/> |
|Bezeichner:  <br/> |0x3601  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-container  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft kann genau einen der folgenden Werte aufweisen:
  
FOLDER_GENERIC 
  
> Eine generische Ordner, der Nachrichten und andere Ordner enthält.
    
FOLDER_ROOT 
  
> Der Stammordner der Ordner Hierarchietabelle, d. h., einen Ordner, die über keinen übergeordneten Ordner verfügt.
    
FOLDER_SEARCH 
  
> Dieser Ordner enthält die Ergebnisse einer Suche, in Form von Links zu Nachrichten, die Suchkriterien erfüllen.
    
Im Stammverzeichnis des eines Nachrichtenspeichers darf nicht mit dem Stamm der Teilstruktur zwischen Personen Nachricht (IPM) in diesem Speicher verwechselt werden. Das Store-Stammordner, ohne übergeordnetes Objekt ist, wird durch Aufrufen der [IMsgStore::OpenEntry](imsgstore-openentry.md) -Methode mit einem null-Eintrags-ID abgerufen. Stammordner der IPM-Unterstruktur, die ein übergeordnetes Element vorhanden ist, wird mit dem Wert der Eigenschaft **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) für den Anruf **OpenEntry** abgerufen. 
  
MAPI kann nur eine Stammordner pro Nachrichtenspeicher. Dieser Ordner enthält Nachrichten und andere Ordner. Im Stammordner **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))-Eigenschaft enthält die Eintrags-ID des Ordners.
  
Die Informationen in einem Suchergebnisse Ordner in seiner Inhaltstabelle, die enthält dieselben Spalten als Tabelle normalerweise sowie zwei zusätzliche Spalten Ermitteln des Ordners, in dem jede Nachricht wurde gefunden, in erster Linie gespeichert ist: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (Anzeigename, erforderlich), und diese Eigenschaft (Eintrags-ID, optional).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Ordner Vorgänge behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


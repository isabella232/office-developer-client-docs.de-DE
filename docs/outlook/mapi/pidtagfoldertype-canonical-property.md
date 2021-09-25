---
title: Kanonische PidTagFolderType-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6427d6a736896e5103b2b73e0a688ced2760b84b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620240"
---
# <a name="pidtagfoldertype-canonical-property"></a>Kanonische PidTagFolderType-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Konstante, die den Ordnertyp angibt. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_FOLDER_TYPE  <br/> |
|Kennung:  <br/> |0x3601  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |MAPI-Container  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft kann genau einen der folgenden Werte haben:
  
FOLDER_GENERIC 
  
> Ein generischer Ordner, der Nachrichten und andere Ordner enthält.
    
FOLDER_ROOT 
  
> Der Stammordner der Ordnerhierarchietabelle, d. h. ein Ordner ohne übergeordneten Ordner.
    
FOLDER_SEARCH 
  
> Ein Ordner, der die Ergebnisse einer Suche in Form von Links zu Nachrichten enthält, die die Suchkriterien erfüllen.
    
Der Stamm eines Nachrichtenspeichers sollte nicht mit dem Stamm der IPM-Unterstruktur (Interpersonal Message) in diesem Speicher verwechselt werden. Der Stammordner des Speichers, der kein übergeordnetes Element aufweist, wird durch Aufrufen der [IMsgStore::OpenEntry-Methode](imsgstore-openentry.md) mit einem NULL-Eintragsbezeichner abgerufen. Der Stammordner der IPM-Unterstruktur, der über ein übergeordnetes Element verfügt, wird mithilfe des Werts der **Eigenschaft PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) für den **OpenEntry-Aufruf** abgerufen. 
  
MAPI lässt nur einen Stammordner pro Nachrichtenspeicher zu. Dieser Ordner enthält Nachrichten und andere Ordner. Die **eigenschaft PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) des Stammordners enthält den eigenen Eintragsbezeichner des Ordners.
  
Die Informationen in einem Suchergebnisordner werden hauptsächlich in der Inhaltstabelle gespeichert, die dieselben Spalten wie ein typisches Inhaltsverzeichnis enthält, sowie zwei zusätzliche Spalten, die den Ordner identifizieren, in dem jede Nachricht gefunden wurde: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (Anzeigename, erforderlich) und diese Eigenschaft (Eintragsbezeichner, optional).
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordnervorgänge.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)


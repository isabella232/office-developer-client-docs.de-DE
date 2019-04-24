---
title: Kanonische Pidtagfoldertype (-Eigenschaft
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
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316317"
---
# <a name="pidtagfoldertype-canonical-property"></a>Kanonische Pidtagfoldertype (-Eigenschaft

  
  
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
  
> Der Stammordner der Ordner Hierarchietabelle, also ein Ordner, der keinen übergeordneten Ordner hat.
    
FOLDER_SEARCH 
  
> Ein Ordner, der die Ergebnisse einer Suche in Form von Links zu Nachrichten enthält, die Suchkriterien erfüllen.
    
Der Stamm eines Nachrichtenspeichers sollte nicht mit dem Stamm der Unterstruktur der zwischenmenschlichen Nachricht (IPM) in diesem Speicher verwechselt werden. Der Stammordner des Speichers, der über kein übergeordnetes Element verfügt, wird durch Aufrufen der [IMsgStore:: OpenEntry](imsgstore-openentry.md) -Methode mit einer NULL-Eintrags-ID abgerufen. Der Stammordner der IPM-Unterstruktur, der über ein übergeordnetes Element verfügt, wird mithilfe des Werts der **PR_IPM_SUBTREE_ENTRYID** ([pidtagipmsubtreeentryid (](pidtagipmsubtreeentryid-canonical-property.md))-Eigenschaft für den OpenEntry-Aufruf abgerufen. **** 
  
MAPI ermöglicht nur einen Stammordner pro Nachrichtenspeicher. Dieser Ordner enthält Nachrichten und andere Ordner. Die **PR_PARENT_ENTRYID** ([pidtagparententryid (](pidtagparententryid-canonical-property.md))-Eigenschaft des Stammordners enthält die eigene Eintrags-ID des Ordners.
  
Die Informationen in einem Ordner mit Suchergebnissen werden hauptsächlich in der Inhaltstabelle gespeichert, die die gleichen Spalten wie eine typische Inhaltstabelle enthält, sowie zwei zusätzliche Spalten, die den Ordner identifizieren, in dem die einzelnen Nachrichten gefunden wurden: **PR_PARENT_DISPLAY** ([ Pidtagparentdisplay (](pidtagparentdisplay-canonical-property.md)) (Anzeigename, erforderlich) und diese Eigenschaft (Eintrags-ID, optional).
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Behandelt Ordner Vorgänge.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)


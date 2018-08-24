---
title: Status „Uploadhierarchie“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572186"
---
# <a name="upload-hierarchy-state"></a>Status „Uploadhierarchie“

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was geschieht, während die Hierarchie Zustand der Replikation Zustandsautomat hochladen. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Synchronisieren von Zustand](synchronize-state.md) <br/> |
|Diesen Status:  <br/> |[Hochladen der Ordner Zustand](upload-folder-state.md), oder Zustand synchronisieren  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der einem Zustand zu einem anderen ausgehenden muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status Hochladen einer Struktur Ordnerhierarchie, die in einem vorherigen angegeben wurde initiiert synchronisieren Zustand. Outlook bestimmt die Anzahl der Ordner, in denen, die in dieser Hierarchie und initialisiert *cEnt* in **UPHIER**geändert oder erstellt wurden. Outlook zählt auch die Anzahl der hochgeladenen Ordnern mit einem anderen Element *iEnt* an. Um jeden Ordner *cEnt* hochzuladen, verschiebt der Client den lokalen Speicher in den Ordner hochladen Zustand, auf den Upload Hierarchie Status zurückgeben, wenn der Ordner Hochladevorgang abgeschlossen ist. 
  
Nach Ende der Upload Hierarchie Zustand gibt der lokale Speicher auf den Status synchronisieren.
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCHRONISIERUNGSSTATUS](syncstate.md)


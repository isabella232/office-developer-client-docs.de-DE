---
title: Status „Synchronisieren“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795698"
---
# <a name="synchronize-state"></a>Status „Synchronisieren“

  
  
**Betrifft**: Outlook 
  
 In diesem Thema wird beschrieben, was geschieht, während die Synchronize-Zustand des Computers Zustand Replikation. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[SYNC](sync.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Leerlauf](idle-state.md) <br/> |
|Diesen Status:  <br/> |[Hierarchie Downloadstatus](download-hierarchy-state.md), [Synchronisieren Inhalt Zustand](synchronize-contents-state.md), [Hierarchie Zustand hochladen](upload-hierarchy-state.md)oder Leerlauf  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird die Synchronisierung initiiert. Ein lokales Speichers Übergang kann ein Upload oder eine Downloadstatus von hier aus. Beispielsweise ein lokales Speichers kann auf den Upload Hierarchie Status zu eine Ordnerhierarchie auf den Server hochzuladen verschieben oder sie können eine vollständige Synchronisierung durchführen, indem ersten Hochladen der Hierarchie und klicken Sie dann die Hierarchie vom Server herunterladen.
  
Während dieser Zustand initialisiert Outlook die zugeordnete **SYNC** -Datenstruktur durch den Pfad zu dem lokalen Speicher, damit Outlook Änderungen bei der anderen Status sieht. 
  
Der Client legt die [in] Mitglieder der **SYNCHRONISIERUNG**, die Outlook mitteilt, wie anderen Zustände behandelt werden sollen. Beispielsweise kann der Client *UlFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** festgelegt und *Pel* und eine Liste der Ordner an, Outlook, dass nur diese Ordner Eintragsbezeichner wird hochgeladen werden. Wenn dieser Status beendet wird, wird der lokale Speicher in den Leerlauf zurückgesetzt. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


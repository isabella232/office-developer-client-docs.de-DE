---
title: Status „Uploadordner“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795797"
---
# <a name="upload-folder-state"></a>Status „Uploadordner“

  
  
**Betrifft**: Outlook 
  
 In diesem Thema wird beschrieben, was geschieht, während der Upload Ordner Zustand des Computers Zustand Replikation. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|State-ID:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Verwandte-Datenstruktur:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Hochladen der Hierarchie Zustand](upload-hierarchy-state.md) <br/> |
|Diesen Status:  <br/> |Hochladen der Hierarchie Zustand  <br/> |
   
> [!NOTE]
> Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat. Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben. 
  
## <a name="description"></a>Beschreibung

Dieser Status wird initiiert, Hochladen eines Ordners in einer Hierarchie, die in einem vorherigen Upload Hierarchie Zustand angegeben wurde. Während dieser Status wird Outlook das Folder-Objekt (sofern es nicht gelöscht) und die Kennzeichen, die den Zustand des Ordners (neue, verschoben, geändert oder gelöscht) als Teil der Datenstruktur des entsprechenden **UPFLD** . Der Client lädt dann diese Informationen an den Server hoch. 
  
Wenn der Hochladevorgang erfolgreich ist, wird der Client *UlFlags* in **UPFLD** auf **UPF_OK**. Outlook löscht dann internen Informationen über die Anforderung an den Ordner hochladen. 
  
Nach Ende der Ordner Upload gibt der lokale Speicher in den Upload Hierarchie Zustand zurück. Basierend auf der **[UPHIER](uphier.md)** -Struktur, die auf den vorstehenden Upload Hierarchie Status entspricht, bestimmt Outlook, ob den nächsten Ordner hochladen fort und zur Vorbereitung der nächsten Upload Ordner Status. 
  
> [!NOTE]
> Wenn der Client nur ein Ordner hochladen muss, kann der Client die Replikation über das [Synchronisieren von Zustand](synchronize-state.md) initiieren, ohne den Upload Hierarchie Zustand. Der Client legt bestimmte Mitglieder der **[SYNCHRONISIERUNG](sync.md)** – *UlFlags* **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und *Feid* auf den Ordner ID – anzuweisen, Outlook, nur einen Ordner hochgeladen werden soll. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


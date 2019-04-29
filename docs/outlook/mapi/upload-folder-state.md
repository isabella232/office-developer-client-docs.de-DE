---
title: Ordner Status hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419569"
---
# <a name="upload-folder-state"></a>Ordner Status hochladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Upload-Ordner Status des Replikationsstatus Computers passiert. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Status-ID:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Zugehörige Datenstruktur:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Aus folgendem Zustand:  <br/> |[Hierarchie Status hochladen](upload-hierarchy-state.md) <br/> |
|Zu folgendem Status:  <br/> |Hierarchie Status hochladen  <br/> |
   
> [!NOTE]
> Der Replikationsstatus Computer ist ein deterministischer Statuscomputer. Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen eines Ordners in einer Hierarchie, der in einem vorangehenden Upload-Hierarchie Status angegeben wurde. In diesem Zustand stellt Outlook das Folder-Objekt (falls es nicht gelöscht wurde) und die Flags bereit, die den Status des Ordners (neu, verschoben, geändert oder gelöscht) als Teil der entsprechenden **UPFLD** -Datenstruktur angeben. Der Client lädt diese Informationen dann auf den Server hoch. 
  
Wenn der Upload erfolgreich ist, legt der Client *ulFlags* in **UPFLD** auf **UPF_OK**fest. Outlook löscht dann die internen Informationen zu der Anforderung, den Ordner hochzuladen. 
  
Wenn der Ordner Upload beendet wird, wird der lokale Speicher zum Upload-Hierarchie Status zurückgegeben. Basierend auf der **[uphier](uphier.md)** -Struktur, die dem vorangehenden Upload-Hierarchie Status entspricht, bestimmt Outlook, ob das Hochladen des nächsten Ordners fortgesetzt und der nächste Upload-Ordner Status vorbereitet werden soll. 
  
> [!NOTE]
> Wenn der Client nur einen Ordner hochladen muss, kann der Client die Replikation über den [Status Synchronize](synchronize-state.md) initiieren, ohne den Upload-Hierarchie Status einzugeben. Der Client legt bestimmte Synchronisierungs **[](sync.md)** Mitglieder – *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und *Feid* auf die ID des Ordners – fest, um Outlook mitzuteilen, dass nur ein Ordner hochgeladen wird. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


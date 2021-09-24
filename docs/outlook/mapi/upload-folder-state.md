---
title: Hochladen Ordnerstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb9708b63f72533745b3b6e18c96816e1fa4f229
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549777"
---
# <a name="upload-folder-state"></a>Hochladen Ordnerstatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Uploadordnerstatus des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPFLD](upfld.md)** <br/> |
|Aus diesem Zustand:  <br/> |[Hochladen Hierarchiestatus](upload-hierarchy-state.md) <br/> |
|In diesem Zustand:  <br/> |Hochladen Hierarchiestatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Bundesland in einen anderen wechselt, muss schließlich von letzterem zum ersten Zurückkehren zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Zustand initiiert das Hochladen eines Ordners in einer Hierarchie, die in einem vorherigen Uploadhierarchiestatus angegeben wurde. In diesem Zustand stellt Outlook das Ordnerobjekt (falls es nicht gelöscht wurde) und die Flags bereit, die den Status des Ordners (neu, verschoben, geändert oder gelöscht) als Teil der entsprechenden **UPFLD-Datenstruktur** angeben. Der Client lädt diese Informationen dann auf den Server hoch. 
  
Wenn der Upload erfolgreich ist, legt der Client  *ulFlags*  in **UPFLD** auf **UPF_OK** fest. Outlook löscht dann die internen Informationen zu der Anforderung, den Ordner hochzuladen. 
  
Wenn der Ordnerupload beendet ist, kehrt der lokale Speicher in den Uploadhierarchiestatus zurück. Basierend auf der **[UPHIER-Struktur,](uphier.md)** die dem vorherigen Uploadhierarchiestatus entspricht, bestimmt Outlook, ob mit dem Hochladen des nächsten Ordners fortgefahren und der nächste Uploadordnerstatus vorbereitet werden soll. 
  
> [!NOTE]
> Wenn der Client nur einen Ordner hochladen muss, kann der Client die Replikation über den [Synchronisierungsstatus](synchronize-state.md) initiieren, ohne in den Uploadhierarchiestatus zu wechseln. Der Client legt bestimmte Elemente von **[SYNC](sync.md)** fest – *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und *feid* auf die ID des Ordners – um Outlook mitzuteilen, dass nur ein Ordner hochgeladen wird. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


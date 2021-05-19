---
title: Status des Ordners hochladen
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
# <a name="upload-folder-state"></a>Status des Ordners hochladen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 In diesem Thema wird beschrieben, was während des Status des Uploadordners des Replikationsstatuscomputers geschieht. 
  
## <a name="quick-info"></a>QuickInfo

|||
|:-----|:-----|
|Statusbezeichner:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|Verwandte Datenstruktur:  <br/> |**[UPFLD](upfld.md)** <br/> |
|In diesem Zustand:  <br/> |[Uploadhierarchiestatus](upload-hierarchy-state.md) <br/> |
|In diesem Zustand:  <br/> |Uploadhierarchiestatus  <br/> |
   
> [!NOTE]
> Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat. Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren. 
  
## <a name="description"></a>Beschreibung

Dieser Status initiiert das Hochladen eines Ordners in einer Hierarchie, die in einem vorherigen Uploadhierarchiestatus angegeben wurde. In diesem Zustand stellt Outlook das Folder-Objekt (wenn es nicht gelöscht wurde) und die Flags, die den Status des Ordners (neu, verschoben, geändert oder gelöscht) als Teil der entsprechenden **UPFLD-Datenstruktur** angibt. Der Client lädt diese Informationen dann auf den Server hoch. 
  
Wenn der Upload erfolgreich war, legt der Client *ulFlags* in **UPFLD** auf **UPF_OK.** Anschließend werden die internen Informationen zu der Anforderung zum Hochladen des Ordners von Outlook geräumt. 
  
Wenn der Ordnerupload endet, kehrt der lokale Speicher zum Status der Uploadhierarchie zurück. Basierend auf der **[UPHIER-Struktur,](uphier.md)** die dem vorherigen Uploadhierarchiestatus entspricht, bestimmt Outlook, ob mit dem Hochladen des nächsten Ordners und der Vorbereitung auf den nächsten Uploadordnerstatus fortzufahren ist. 
  
> [!NOTE]
> Wenn der Client nur einen Ordner hochladen muss, kann [](synchronize-state.md) der Client die Replikation über den Synchronisierungsstatus initiieren, ohne den Uploadhierarchiestatus zu betreten. Der Client legt bestimmte Mitglieder von **[SYNC](sync.md)** fest –  *ulFlags*  auf **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und  *feid*  auf die ORDNER-ID – um Outlook zu informieren, dass nur ein Ordner hochgeladen wird. 
  
## <a name="see-also"></a>Siehe auch



[Informationen über die Replikations-API](about-the-replication-api.md)
  
[MAPI-Konstanten](mapi-constants.md)
  
[Informationen über den Replikationszustandsautomaten](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)


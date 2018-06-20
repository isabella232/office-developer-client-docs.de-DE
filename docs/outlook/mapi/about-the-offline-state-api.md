---
title: Über die Offline State-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791246"
---
# <a name="about-the-offline-state-api"></a>Über die Offline State-API

  
  
**Betrifft**: Outlook 
  
Die Offline Zustand-API unterstützt Rückrufe, der angibt, Änderungen in den Status der Verbindung des Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 – beispielsweise verhindern in Outlook 2013 oder Outlook 2010 online zu offline. Die API verwendet ein globales offline-Objekt in Outlook 2013 oder Outlook 2010, um eine solche Änderung für einen bestimmten Benutzerkontoprofil verfolgen. Die Benachrichtigung ist die einzige unterstützte Form der Rückruf an. Wie Clients dieser API, e-Mail-Anbieter, die über eine solche Verbindung Zustandsänderungen benachrichtigt werden möchten, die folgenden Schritte aus:
  
1. Implementieren Sie **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Öffnen Sie ein vorhandenes offline-Objekt für ein bestimmtes Profil **[HrOpenOfflineObj](hropenofflineobj.md)** verwenden. 
    
3. Ermitteln Sie, ob das Objekt die Möglichkeit der Bereitstellung von online oder offline Benachrichtigungen mithilfe von **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** hat. 
    
4. Registrieren Sie das Objekt für online oder offline Benachrichtigungen **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** verwenden. E-Mail-Anbieter können nun Benachrichtigungen erhalten, dass Outlook 2013 oder Outlook 2010 senden **IMAPIOfflineNotify**verwenden. 
    
5. Entfernen Sie beim Herunterfahren Registrierung für online und offline Benachrichtigungen **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** verwenden. 
    
> [!NOTE]
> Im Allgemeinen Outlook 2013 und Outlook 2010 können von einem Client von online/offline Änderungen sowie weitere Änderungen benachrichtigt, aber die Offline Zustand-API unterstützt nur Benachrichtigungen für Online-/offline geändert wird. Der Client sollte alle anderen Benachrichtigungen ignoriert werden. Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** und **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Ein Beispiel für ein Client, der State-API verwendet, finden Sie unter [Informationen zu the Beispiel Offline State-Add-in](about-the-sample-offline-state-add-in.md). Das Beispiel Offline Zustand-Add-in ist ein COM-add-in, die Status-API zum Überwachen und Ändern des Verbindungsstatus verwendet.
  
Diese API bietet folgende Funktionen:
  
Definitionen:
  
- [MAPI-Konstanten](mapi-constants.md)
    
Datentypen:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Funktionen:
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Schnittstellen:
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    


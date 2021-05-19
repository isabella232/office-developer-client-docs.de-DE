---
title: Informationen zur Offlinestatus-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: 'Letzte �nderung: Montag, 25. Juni 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410483"
---
# <a name="about-the-offline-state-api"></a>Informationen zur Offlinestatus-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Offlinestatus-API unterstützt Rückrufe, die Änderungen im Verbindungsstatus eines Benutzers in Microsoft Outlook 2013 und Microsoft Outlook 2010 anzeigen, z. B. von der Onlineverwendung in Outlook 2013 oder Outlook 2010 bis zum Offlinemodus. Die API verwendet ein globales Offlineobjekt in Outlook 2013 oder Outlook 2010, um solche Änderungen für ein bestimmtes Benutzerkontoprofil nachverfolgt. Benachrichtigung ist die einzige unterstützte Form des Rückrufs. Als Clients dieser API gehen E-Mail-Anbieter, die über solche Verbindungsstatusänderungen benachrichtigt werden möchten, wie folgt vor:
  
1. Implementieren **[sie IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Öffnen Sie ein vorhandenes Offlineobjekt für ein bestimmtes Profil mithilfe **[von HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Ermitteln Sie, ob das Objekt über die Möglichkeit verfügt, Online- oder Offlinebenachrichtigungen mithilfe von **[IMAPIOffline::GetCapabilities zur Verfügung zu stellen.](imapioffline-getcapabilities.md)** 
    
4. Registrieren Sie das Objekt für Online- oder Offlinebenachrichtigungen mithilfe **[von IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. E-Mail-Anbieter können nun Benachrichtigungen empfangen, die Outlook 2013 oder Outlook 2010 senden, indem **sie IMAPIOfflineNotify verwenden.** 
    
5. Entfernen Sie beim Herunterfahren die Registrierung für Online- und Offlinebenachrichtigungen mithilfe **[von IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Im Allgemeinen können Outlook 2013 und Outlook 2010 einen Client über Online-/Offlineänderungen sowie andere Änderungen benachrichtigen, aber die Offlinestatus-API unterstützt nur Benachrichtigungen für Online-/Offlineänderungen. Der Client sollte alle anderen Benachrichtigungen ignorieren. Weitere Informationen finden Sie unter **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Ein Beispiel für einen Client, der die Offlinestatus-API verwendet, finden Sie unter [Informationen zum Beispiel-Offlinestatus-Add-In](about-the-sample-offline-state-add-in.md). Das Beispiel-Offlinestatus-Add-In ist ein COM-Add-In, das die Offlinestatus-API verwendet, um den Verbindungsstatus zu überwachen und zu ändern.
  
Diese API bietet Folgendes:
  
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
    

